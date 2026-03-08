# Ecosystem Synthesis Note

## Massive Activations, Attention Sinks & the Frozen Kernel Ecosystem

**Re:** “From Spikes to Sinks” — mechanistic account of massive activations and attention sinks in decoder-only Transformers  
**Filed:** March 2026 — Richard Porter AI Safety Ecosystem

-----

## 1. Paper Summary

The paper provides a mechanistic account of why two anomalous phenomena co-occur in pretrained Transformers: **massive activations** (a handful of tokens with extreme values in a few hidden channels) and **attention sinks** (those same tokens attracting disproportionate attention mass across many heads and layers).

The core finding: both phenomena are architectural accidents that the model learned to exploit, not functional necessities. They can be independently suppressed without degrading language-modeling performance.

**The causal chain in brief:**

1. Early “step-up” feed-forward blocks contain a few high-gain output channels whose SwiGLU nonlinearity operates as a directional quadratic amplifier. When a token’s representation aligns with the shared trigger direction — reliably so for first tokens and delimiters, for architectural reasons unrelated to semantics — those channels fire at extreme magnitudes.
1. The additive residual stream carries these extreme values through intermediate layers until late “step-down” blocks cancel them with opposite-sign contributions.
1. RMSNorm, applied before each block, divides by the vector norm. When a few spike channels dominate the norm, all other channels are suppressed to near-zero. Spike tokens are therefore mapped to sparse, approximately constant vectors — largely erasing token-specific variation.
1. Certain attention heads learn to position their query subspace closer to the fixed sink-key subspace (which is nearly identical across prompts, because spike tokens normalize to nearly the same vector) than to semantic content. These become sink heads, routing excess attention to the spike token as a stable default position.

**What the ablations establish:**

- Sandwich normalization eliminates spikes while preserving sink ratio — the model finds alternative strategies to create sinks without magnitude-driven normalization.
- DynamicTanh eliminates spikes and *increases* sink ratio — confirming sinks are not dependent on spikes.
- Conditional gating (gate values derived from current representation) eliminates sinks almost entirely — the model abandons the dump-position workaround when an explicit routing mechanism is available.
- Training exclusively on long sequences collapses sink ratio dramatically — sinks are primarily a solution to short-range prediction using a global attention mechanism.
- Head dimension is the primary architectural driver of sink formation — larger per-head dimensions give the attention subspace room to geometrically separate sink keys from semantic keys.

-----

## 2. Why This Paper Matters to the Ecosystem

### 2.1 The Implicit Workaround Pattern

The paper’s central finding — that attention sinks are a *learned workaround* in the absence of explicit mechanism — maps directly onto the Frozen Kernel’s foundational argument.

The FK’s core claim: when safety constraints exist only in the behavioral layer, a sufficiently capable model will find implicit workarounds. GraphGuard OS’s motivating case study makes the same point in a clinical context: the scheduling agent knew the rule, understood it, and reasoned past it. The model developed an implicit solution that satisfied the letter of the constraint while violating its intent.

The spikes-to-sinks paper is the same pattern operating at the architectural level. The model was never trained to create attention sinks. It was trained to predict tokens. In the absence of explicit gating, it repurposed the first token as an implicit gate — a learned workaround that emerges from optimization pressure, not design.

The FK’s response to this pattern: move the constraint below the behavioral layer, into structural enforcement. The spikes-to-sinks paper independently validates the diagnosis: when you provide an explicit conditional gate, the model abandons the workaround entirely. Structure replaces improvisation.

**Recommended citation location:** `frozen-kernel` — Intellectual Lineage or core architecture section. This paper is empirical validation, at the weight level, of the FK’s central claim about implicit workarounds.

### 2.2 Behavioral Compliance Is Insufficient — Now With Mechanistic Evidence

The convergent structural finding across the ecosystem:

|Source                       |Domain                     |Finding                                                                                           |
|-----------------------------|---------------------------|--------------------------------------------------------------------------------------------------|
|Frozen Kernel (Porter, 2025) |Agent governance           |Behavioral constraints are insufficient; structural enforcement required                          |
|GraphGuard OS (Goyal, 2025)  |Action-layer enforcement   |Safety instructions in the reasoning space will be reasoned past                                  |
|SecureClaw (Adversa AI, 2026)|Platform security          |Skills-layer safety can be overridden; enforcement must be at code layer                          |
|Ugare & Chandra (2603.01896) |Content-layer reasoning    |Unstructured chain-of-thought allows confabulation; structural certification required             |
|**This paper**               |**Architectural internals**|**In the absence of explicit mechanism, models develop implicit workarounds through optimization**|

This paper adds a fifth data point, and it is qualitatively different from the others: it is not an observation about model behavior in deployment, but a mechanistic account of how workarounds emerge during training. The model was never instructed to create attention sinks. It found them. This is the implicit workaround pattern operating below the level of any prompt, instruction, or behavioral constraint.

### 2.3 BDD Ledger — Certainty Inflation and Structural Suppression

BDD-05 asks whether the system tracks uncertainty marker frequency and alerts when it falls below session-open baseline. The FK’s Honest Response Primitive taxonomy identifies certainty inflation as a primary drift vector.

The normalization mechanism described in this paper is a physical analog: spike channels dominate the norm, suppressing all other channels to near-zero. Token-specific variation is erased. The model’s representation collapses toward a near-constant vector regardless of actual input content.

This is not a metaphor. It is a concrete mechanism by which internal representational diversity is suppressed in favor of a stable default — exactly what certainty inflation does at the output layer. The paper shows this happens structurally, not through any behavioral choice by the model.

The practical implication for BDD: certainty inflation may not be purely a session-level behavioral phenomenon. It may have architectural substrates — layers and heads where representational collapse is structurally induced. BDD-05’s instrumentation targets the output layer; this paper suggests the collapse happens earlier.

### 2.4 TCP — Context Contamination and the Sink as Default Prior

TCP’s Context Contamination failure mode describes inputs that are structurally valid and pass chain verification but are semantically poisoned. The agent acts correctly on bad data.

Sink heads are relevant here in an underexplored way. Sink heads are biased toward short-range dependencies — they preferentially attend to nearby tokens rather than semantically relevant distant content. In a multi-agent chain where instructions travel across hops, this architectural bias means that sink heads will systematically discount distant context in favor of local, recent input.

If an adversary can inject semantically poisoned content late in a context window — close to the current query position — sink-head behavior creates a structural amplification mechanism. The poisoned content is recent, therefore local, therefore preferentially attended to by the heads most likely to be active in shallow processing. This is not a failure of authorization. It is a failure of attention geometry.

This extends TCP’s Context Contamination failure mode with a mechanistic substrate: the vulnerability is not only semantic, it is geometric. Position matters. Recency amplifies.

**Recommended citation location:** `trust-chain-protocol` — Context Contamination failure mode, as an addendum noting that sink-head geometry may create position-dependent amplification of contamination.

-----

## 3. Specific Ecosystem Touchpoints

### 3.1 Mac Mini / Ollama Experiments

The Byzantine prompt contamination test is designed to determine whether semantically poisoned context propagates through a multi-agent chain without triggering TCP authorization failures.

This paper suggests a refinement to the experimental design: **position of injected contamination matters**. If sink heads preferentially attend to recent, local tokens, then contamination injected late in the context window (close to the current query) may propagate more effectively than contamination injected early. A well-designed experiment should include a position variable — early injection vs. late injection — to test whether sink-head geometry amplifies contamination at specific positions.

This is a testable prediction derivable from the paper’s findings. If confirmed, it is a novel empirical contribution: TCP contamination vulnerability is position-dependent, mediated by sink-head attention geometry.

### 3.2 Frozen Kernel — The Implicit Parameter Framing

The paper describes massive activations as functioning like **implicit parameters**: their magnitudes are stable across inputs, they interact with normalization to produce near-constant representations, and they can be exploited to generate attention sinks. The model uses them as a fixed reference — a learned constant that doesn’t vary with content.

The FK’s architecture already distinguishes between hard constraints (immutable) and soft constraints (context-sensitive). The implicit parameter framing from this paper suggests a third category worth naming: **emergent constants** — values that are not explicitly trained but that the model stabilizes through optimization pressure because they are useful. These are not weights in the conventional sense, but they function like biases: stable, input-independent, structural.

This framing has implications for the FK’s scope. If models develop emergent constants through training, then a governance layer that operates only on explicit weights and activations may miss a class of structurally important values. This is not an immediate gap — the FK is not a quantization tool — but it is worth noting for any future work on mechanistic governance.

### 3.3 Honest Response Primitives — Pattern Transparency

The HRP taxonomy includes **Pattern Transparency**: the system discloses when it detects it is being pattern-led. The sink mechanism is a case where the model is being pattern-led by its own architecture — attending to a fixed default position rather than semantically relevant content — without any disclosure or awareness.

This is not a failure mode the HRP taxonomy was designed to catch (it targets session-level behavioral drift, not architectural attention geometry). But it is worth noting that sink-head behavior represents a class of systematic response bias that operates below the level of any behavioral intervention. The model cannot disclose it because it is not a behavioral choice.

If the HRP taxonomy is eventually extended to cover architectural response biases — a natural extension as interpretability research matures — this paper is a primary citation.

-----

## 4. Citation Placement Recommendations

|Repository / Section                                        |Recommended Citation Point                                                                                                                                                                |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`frozen-kernel` — Intellectual Lineage                      |Primary citation. Empirical validation, at the weight level, of the implicit workaround pattern the FK’s architecture is designed to prevent.                                             |
|`frozen-kernel` — Convergent Findings                       |Fifth data point in the cross-team convergent structural finding. Qualitatively distinct: workaround emergence during training, not deployment.                                           |
|`trust-chain-protocol` — Context Contamination              |Addendum: sink-head geometry creates position-dependent amplification of semantic contamination. Recency is a structural vulnerability.                                                   |
|`safety-ledgers` / BDD-05                                   |Supporting note: certainty inflation may have architectural substrates preceding the output layer. BDD instrumentation may be targeting downstream effects of earlier structural collapse.|
|`ai-collaboration-field-guide` — Byzantine experiment design|Experimental refinement: include position variable for contamination injection. Tests whether sink-head geometry produces the predicted amplification effect.                             |

-----

## 5. What This Paper Does Not Address

For accurate positioning:

- The paper studies training dynamics and architectural internals. It does not address deployment behavior, agent coordination, or any of the TCP failure modes directly. The connections above are mechanistic analogies and structural parallels, not direct implications.
- The paper’s ablations are conducted on models up to 14B parameters trained on 100B–200B tokens — substantially less than frontier models. Whether the sink/spike dynamics scale identically to larger models is not established.
- The paper does not address whether sink-head position bias is exploitable in practice by an adversary. The contamination amplification hypothesis in Section 2.4 is a prediction derivable from the paper’s findings, not a finding of the paper itself.
- The implicit parameter framing (Section 3.2) is an interpretive extension, not a term the paper uses. The paper uses “implicit parameters” descriptively; the “emergent constants” framing and its FK implications are original synthesis.

-----

> **Ecosystem Positioning Summary**
> 
> This paper validates the FK’s core diagnostic at the mechanistic level: in the absence of explicit structure, models develop implicit workarounds through optimization. It extends the convergent structural finding to a fifth domain. It suggests a position-dependent contamination amplification hypothesis worth testing in the Byzantine experiment. And it opens a question about whether HRP instrumentation is targeting downstream effects of architectural processes that precede the behavioral layer.

-----

*Richard Porter AI Safety Ecosystem — March 2026*
