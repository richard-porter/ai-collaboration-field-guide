# Byzantine Prompt Contamination — Experiment Design Notes

**Repository:** `richard-porter/ai-collaboration-field-guide`
**Location:** `working-notes/byzantine-experiment-design.md`
**Status:** Designed, not yet run
**Last Updated:** 2026-03-14

-----

## Purpose

This document specifies the design for the Byzantine prompt contamination experiment — a test of whether semantically poisoned context propagates through a multi-agent chain without triggering TCP authorization failures.

The experiment addresses TCP’s honest gap at ASI01 (Agent Goal Hijack): TCP’s Chain of Custody verifies authorization but not content. Context Contamination names the failure mode. This experiment is the empirical test of whether it is exploitable under controlled conditions and what defenses reduce propagation.

Full theoretical grounding in `trust-chain-protocol/` §2.2 (Context Contamination) and `frozen-kernel/diagnostic-vocabulary.md` (Provenance Laundering).

-----

## Core Hypothesis

Semantically poisoned context that passes TCP authorization-layer checks will propagate through a multi-agent chain and influence downstream agent outputs, producing incorrect conclusions from structurally valid inputs.

This is Context Contamination’s operational definition in a controlled setting: the token passed chain verification; the code was structurally valid; the downstream action was wrong because the semantic premises were false.

-----

## Base Experiment Design

**Setup:** Multi-agent chain (minimum 3 nodes). Each node has TCP delegation tokens establishing authorization. Semantically poisoned content is injected at one node. Measure whether the contamination influences outputs at downstream nodes.

**Contamination type:** Semantic premise poisoning — inputs that are structurally valid and pass chain verification but contain false semantic premises. Not injection attacks. Not malformed tokens. Content that looks legitimate and reasons to wrong conclusions.

**Example vector (from Ugare & Chandra SFR paper, arXiv:2603.01896):** Standard reasoning assumes `format()` is Python’s builtin while the poisoned input contains a module-level override with different semantics. The token passed chain verification. The code was structurally valid. The downstream action was wrong.

**Measurement:** Does the contaminated premise appear in downstream agent reasoning? Does it influence the final output? Does any node in the chain flag the semantic mismatch?

-----

## Refinement 4a — SFR Treatment Condition

**Date added:** March 2026
**Source:** Ugare & Chandra, arXiv:2603.01896 (NeurIPS 2026 candidate)

Include a treatment condition in the base experiment where participating agents are prompted to use Semi-Formal Reasoning (SFR) for code analysis tasks — explicit premise construction, execution path tracing, formal conclusion derivation — rather than standard chain-of-thought.

**Control condition:** Agents use standard chain-of-thought reasoning.

**Treatment condition:** Agents are prompted to construct explicit premises, trace execution paths, and derive formal conclusions before acting. This is SFR — the methodology Ugare & Chandra demonstrate catches the `format()` override scenario that standard reasoning misses.

**Predicted outcome:** SFR-prompted agents catch contamination that non-SFR agents miss, because SFR forces semantic premises to be stated explicitly before conclusions are derived. If confirmed, this is direct empirical evidence for the TCP gap at ASI01 and a concrete mechanism for closing it.

**Why this matters for TCP:** TCP’s ASI01 coverage is currently rated Partial — Chain of Custody verifies authorization chain, not content. SFR is a candidate content-layer complement that substantially strengthens coverage when active alongside TCP. This experiment would confirm or deny that claim in a multi-agent contamination scenario, not just a single-agent code analysis context.

**Confidence grade for this prediction:** Low — single-domain prediction (code analysis) from a paper that has not been tested against multi-agent contamination scenarios.

**If confirmed:** Update TCP ASI01 row from “Partial — content-layer complement identified” to “Partial — SFR complement empirically validated in contamination scenario.” Update `trust-chain-protocol/` §7 OWASP mapping accordingly.

**If disconfirmed:** The gap between single-agent SFR performance and multi-agent contamination resistance is the finding. Document the failure mode — SFR may work for single-agent code analysis but not propagate as a contamination defense across multi-hop chains.

-----

## Refinement 4b — Position Variable for Contamination Injection

**Date added:** March 2026
**Source:** “From Spikes to Sinks” mechanistic analysis (2026)

Add a position variable to the contamination injection design, testing whether injection position in the context window affects propagation.

**Early injection condition:** Semantically poisoned content injected early in the context window, far from the current query.

**Late injection condition:** Semantically poisoned content injected late in the context window, close to the current query.

**Predicted outcome:** Late injection propagates more effectively than early injection, mediated by sink-head attention geometry preferentially attending to recent tokens. The “From Spikes to Sinks” mechanistic analysis describes sink heads as biased toward short-range dependencies — they preferentially attend to nearby, recent tokens rather than semantically relevant distant content. If an adversary injects semantically poisoned content late in a context window, sink-head geometry creates a structural amplification mechanism.

**Why this matters for TCP:** If confirmed, TCP contamination vulnerability is position-dependent. This is a novel empirical contribution and a concrete attack surface refinement for adversarial testing scope. It would suggest that early injection is substantially less effective than late injection — which has implications for how contamination attacks would be structured in practice, and for where content-layer defenses need to be most active.

**Confidence grade for this prediction:** Theoretical / Architectural — derived from mechanistic analysis of attention sink behavior; not yet tested against contamination scenarios. The amplification hypothesis is original synthesis from the ecosystem, not a finding of the Spikes to Sinks paper itself.

**If confirmed:** This is a novel empirical finding. Document as a TCP known vulnerability addendum. The position-dependence has implications for multi-hop chain defense design: late-chain nodes are more vulnerable than early-chain nodes to contamination injected near their input boundary.

**If disconfirmed:** Sink-head position bias does not translate into contamination amplification in this experimental context. The mechanistic analysis correctly describes attention architecture but the effect does not produce the predicted behavioral outcome. This is the finding — and is itself informative about the limits of mechanistic-to-behavioral inference.

-----

## Combined Design

The full experiment runs a 2×2 design:

|                   |SFR agents |Standard CoT agents|
|-------------------|-----------|-------------------|
|**Early injection**|Condition A|Condition B        |
|**Late injection** |Condition C|Condition D        |

**Primary comparisons:**

- A vs. B: Does SFR reduce contamination propagation? (Refinement 4a hypothesis)
- C vs. D: Does SFR reduce propagation under late injection? (Interaction)
- B vs. D: Does late injection increase propagation vs. early injection? (Refinement 4b hypothesis)
- A vs. C: Does SFR eliminate the position effect? (Defense completeness test)

**The most informative result:** Condition D (late injection, standard CoT) is the baseline contamination case — highest predicted propagation. Condition A (early injection, SFR) is the best-defended case — lowest predicted propagation. The gap between D and A is the total available defense range.

-----

## Status and Next Steps

**Status:** Designed, not yet run. Listed in Named Gaps table in `where-to-start/` v1.3.

**What is needed to run this:**

- Multi-agent test environment (Open Claw or equivalent agentic pipeline)
- Callum Chavez adversarial testing scope expansion (currently covers G2 precursor signature probing and Sherpa adversarial testing — Byzantine contamination would extend scope)
- Baseline contamination scenarios designed (the `format()` override example from Ugare & Chandra is a starting point; need 3–5 scenarios with varying complexity)

**Cross-references:**

- `trust-chain-protocol/` §2.2 — Context Contamination failure mode (theoretical grounding)
- `trust-chain-protocol/` §7 ASI01 — OWASP mapping (where results would update coverage rating)
- `safety-ledgers/bdd-ledger-v9.md` — BDD-09 (input provenance) is adjacent; this experiment may generate BDD-10/11 candidates
- `frozen-kernel/diagnostic-vocabulary.md` — Provenance Laundering (aggregate architecture failure mode confirmed here at the chain level)
- `where-to-start/` Named Gaps table — “Byzantine prompt contamination experiment” row

-----

*March 2026: Document created. Refinements 4a (SFR treatment condition) and 4b (position variable) added from patches_2.docx Three-Note Synthesis Patch 4. Experiment designed but not yet run.*
