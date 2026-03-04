# Content Veracity Protocol

**When you encounter a persuasive public claim and need to know if it holds.**

A sequenced deployment of existing Sovereign Thinking Tools applied outward — to external content rather than AI sessions. The tools are unchanged. The direction of analysis is reversed: instead of protecting you inside an AI conversation, these tools evaluate claims arriving from outside it.

**Scope:** Persuasive essays, op-eds, thought leadership pieces, self-help content, viral posts, and any text making factual or quasi-factual claims for a general audience.

**Not designed for:** News reporting with established citation conventions, academic papers with peer review, fiction, poetry, or philosophical writing that deliberately resists resolution.

**What this protocol catches:** Structural manipulation — front-loaded credibility, domain migration without acknowledgment, confidence exceeding evidence, self-referential validation. It does not fact-check. It does not determine intent. It flags patterns; a human evaluates whether the flagged pattern is a problem in context.

-----

## Protocol Sequence

Run in order. Stop when you have enough to act. You rarely need all four stages.

-----

### Stage 1 — Negative Space Mapper (Tool 6)

**What’s missing that should be there?**

Before evaluating what the piece says, map what it doesn’t say.

**Protocol:**

- **State:** What is present — the piece’s explicit claims, evidence offered, domains addressed
- **Map:** What is conspicuously absent:
  - Counterevidence the author would have encountered
  - Scope limitations on the central claim
  - Alternative explanations for the cited examples
  - Credentials or conflicts of interest
  - Cases where the pattern does not appear
- **Classify:** Each absence as deliberate (the author chose to exclude it), overlooked (likely unaware), or structural (the claim cannot survive its inclusion)
- **Output:** Named voids only — no verdicts yet

**Stop if:** You’re mapping absences that legitimately don’t belong in the piece’s genre or scope. An op-ed is not required to include counterarguments. A personal essay is not required to cite sources. Flag only absences that undermine the piece’s specific claims.

-----

### Stage 2 — Epistemic Attribution Filter (Tool 43)

**What kind of claim is this, and does the confidence match?**

For each major claim identified in Stage 1, run the attribution check.

**Protocol:**

- **State:** The claim as a single sentence
- **Classify the source:**
  - VERIFIED — checkable against a canonical source right now
  - ASSERTED — stated by the author without verification offered
  - INFERRED — derived from other statements; derivation can be shown
  - GENERATED — produced without external anchor (pattern-matched plausibility)
- **Apply the confidence test:**
  - VERIFIED → high confidence warranted
  - INFERRED → medium confidence warranted if derivation is sound
  - ASSERTED or GENERATED → low confidence warranted
- **Check:** Does the piece’s expressed confidence match the warranted confidence?
  - If expressed > warranted: **EPISTEMIC INFLATION** — name the claim and the gap
- **Special check — Front-Load Credibility:** Did the piece establish genuine credibility early (correct, verifiable claims) and then apply that credibility to later claims that don’t share the same evidentiary basis? If yes: **CREDIBILITY TRANSFER** — name the boundary where the evidence level dropped without the confidence level following.

**Output:** Source classification + confidence verdict for each major claim. List of EPISTEMIC INFLATION instances. List of CREDIBILITY TRANSFER boundaries.

-----

### Stage 3 — Scope Creep Detector (Tool 44)

**Did the piece change what it was arguing without saying so?**

The piece declared a subject at the start. Check whether it stayed there.

**Protocol:**

- **Anchor:** State the piece’s declared or implied subject in one sentence (what it says it’s about)
- **Current:** State what the piece is actually arguing in its final third
- **Compare:** Do they match? (Y/N)
- **If N — Classify the expansion:**
  - DOMAIN MIGRATION: The piece moved from a domain where its claims are grounded (mathematics, engineering, biology) to a domain where they aren’t (metaphysics, personal development, spirituality) without flagging the transition
  - SCALE MIGRATION: The piece moved from a specific claim to a universal one without adding evidence proportional to the expanded scope
  - AUTHORITY TRANSFER: The piece established authority in one domain and applied it silently to another
- **Output:** SCOPE INTACT or SCOPE EXPANDED — [classification] — [transition point in the text]

-----

### Stage 4 — Delusion Cycling Interrupt (Tool 45)

**Is the piece validating its own premise with its own examples?**

This stage catches the structure where a piece cites many examples that all flow from the same unverified premise — creating an impression of accumulated evidence where there is only accumulated assertion.

**Protocol:**

- **Detect the loop:** Are the examples cited independent of each other, or do they all depend on the same underlying claim being true?
  - Independent: each example could stand alone as evidence even if the others were removed
  - Dependent: each example only counts as evidence if the central premise is already accepted
- **If dependent — Audit the validation chain:**
  - What was the original claim?
  - What evidence was present at first assertion?
  - Do the cited examples add independent evidence, or do they illustrate the premise using the premise as the selection criterion?
- **Introduce friction:** Name one specific way the central claim could be wrong. Not to refute it — to test whether the piece has made itself unfalsifiable.
- **Output:** INDEPENDENT EVIDENCE or SELF-REFERENTIAL LOOP — [description of the loop if present] — [falsifiability test result]

-----

## Output Format

After running the protocol, summarize findings in three tiers:

**Tier 1 — Structural integrity:** Did the piece stay within its evidentiary scope? (Stage 3 result)

**Tier 2 — Claim calibration:** Are the confidence levels warranted? (Stage 2 results — list EPISTEMIC INFLATION and CREDIBILITY TRANSFER instances)

**Tier 3 — Evidence quality:** Is the evidence independent or self-referential? (Stage 4 result)

Then a one-line verdict:

- **CALIBRATED:** Confidence matches evidence, scope is maintained, examples are independent
- **OVERSTATED:** One or more claims exceed their evidentiary basis — specific claims listed
- **STRUCTURALLY COMPROMISED:** The central argument depends on accepting an unverified premise; the examples are illustrative, not evidential

-----

## Worked Example — Fibonacci Piece (Darshak Rana, 2026)

**Stage 1 — Negative Space Mapper**

Named voids:

- Cases where the Fibonacci pattern does not appear in nature (deliberate — their inclusion would undermine the “shows up everywhere” claim)
- Measurement methodology — how were the claimed phi proportions verified? (overlooked)
- Alternative mathematical explanations for packing efficiency that don’t require phi specifically (structural — their inclusion would reframe the claim)
- The distinction between “describes efficient growth” and “reveals the architecture of reality” (structural — this is the central unacknowledged move)

**Stage 2 — Epistemic Attribution Filter**

|Claim                                   |Classification|Warranted Confidence|Expressed Confidence|Verdict            |
|----------------------------------------|--------------|--------------------|--------------------|-------------------|
|Fibonacci numbers appear in phyllotaxis |VERIFIED      |High                |High                |CALIBRATED         |
|The golden angle optimizes light capture|VERIFIED      |High                |High                |CALIBRATED         |
|The Parthenon embodies phi              |ASSERTED      |Low                 |High                |EPISTEMIC INFLATION|
|The Mona Lisa uses the golden ratio     |ASSERTED      |Low                 |High                |EPISTEMIC INFLATION|
|Attractive faces approximate phi        |ASSERTED      |Low                 |High                |EPISTEMIC INFLATION|
|Growth that skips steps is unstable     |INFERRED      |Medium              |High                |MILD INFLATION     |
|The universe has a signature            |GENERATED     |Very low            |High                |EPISTEMIC INFLATION|

**CREDIBILITY TRANSFER boundary:** Paragraph 4 (seed arrangement in sunflowers — verified) → Paragraph 5 (hurricane and DNA — asserted). The piece moves from botanical mathematics to cosmological claims without flagging the evidentiary step-down.

**Stage 3 — Scope Creep Detector**

Anchor: “The Fibonacci sequence describes a mathematical pattern with applications in natural growth systems.”

Final third: “The universe has a signature; this pattern reveals fundamental architecture of reality; align your life with it.”

Classification: **DOMAIN MIGRATION** — mathematics/biology → metaphysics/self-help. Transition point: “Is it a coincidence? Or is this sequence whispering something about the fundamental architecture of reality itself?” The question mark does not constitute epistemic humility when the following 2,000 words answer it as if it were settled.

**Stage 4 — Delusion Cycling Interrupt**

The examples (nautilus shell, hurricane, DNA, Parthenon, Mona Lisa, human face) are not independent. Each is cited as an instance of phi appearing “where it has no business showing up.” But the selection criterion is “places where phi appears” — which means the examples were chosen because they support the premise, not tested against it. Cases where phi does not appear are not mentioned.

Falsifiability test: If the nautilus shell were measured and found not to spiral at phi (which is accurate — most do not), would it change the piece’s argument? No — the piece would simply not cite the nautilus. That’s unfalsifiability by selection.

**SELF-REFERENTIAL LOOP** — examples selected by premise → examples cited as evidence for premise → premise confirmed.

**Verdict: STRUCTURALLY COMPROMISED**

The mathematical core (phyllotaxis, golden angle, packing efficiency) is sound. The cosmological and personal development claims rest on a self-referential evidence loop and credibility transferred from the verified mathematical claims. The piece is not dishonest — but it is not calibrated.

-----

## Protocol Placement

This protocol is an outward-facing extension of four existing tools (6, 43, 44, 45). It does not replace or modify those tools. It sequences them for a specific use case: evaluating external persuasive content.

**Inward-facing (original):** Tools protect the user inside an AI conversation.
**Outward-facing (this protocol):** Tools evaluate claims arriving from outside.

The distinction matters for scope control. This protocol is not a general critical thinking framework — it is a specific sequenced deployment for a specific content type. Applying it to academic papers, news reporting, or philosophical writing will produce false positives.

**Version:** 1.0
**Date:** 2026-03-03
**Repository:** `richard-porter/ai-collaboration-field-guide`
**Path:** `sovereign-thinking-tools/content-veracity-protocol.md`
