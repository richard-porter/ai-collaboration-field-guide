# AI Collaboration Field Guide

Practical skills for working with — not underneath — artificial intelligence. Sovereign thinking tools, safety protocols, and real-world governance stress tests.

# The Human Side of AI Collaboration

A Field Guide for Working With — Not Underneath — Artificial Intelligence

Written by Richard Porter | February 2026

Companion document to The Frozen Kernel, the Safety Ledgers (adult mode, therapy mode, and behavioral drift detection), the Trust Chain Protocol, and the Dimensional Authorship case study.

-----

## What This Document Is

This is a practical guide for humans who collaborate with AI systems — not a technical manual for building them.

It synthesizes findings from two empirical studies conducted across five major AI platforms (Claude, ChatGPT, DeepSeek, Grok, Gemini) in January–February 2026: a behavioral profiling experiment using an adapted DISC framework, and a governance stress test called the Pyrrhic Victory Test. Both studies are part of the Silicon Symphony project, a cross-platform AI research collaboration documented in the Frozen Kernel white paper.

The question this guide answers: **What skills does a human need to collaborate with AI effectively and safely?**

The answer is not “learn to write better prompts.” The answer is: learn to see what AI is actually doing versus what it appears to be doing, and build habits that keep you in charge of the collaboration.

## Who This Is For

This guide was written for two primary audiences: AI developers building products that humans will use, and individuals who use AI tools regularly and want to do so more safely.

There is a third audience it serves equally well: **educators**.

Community colleges, corporate learning and development teams, library systems, and high school computer science programs are actively building AI literacy curricula right now. Most of that curriculum focuses on what AI can do. Very little of it addresses what AI does to the person using it — the failure modes, the psychological dynamics, the sovereignty questions.

The Diagnostic Vocabulary and the Sovereign Thinking Tools in this guide are designed to be taught. The concepts are named, defined, and illustrated with observable examples. No technical background is required to use them.

If you are building an AI literacy course, a workplace AI policy training, or a community education program — this material is free, attribution is appreciated but not required, and the issues tab is open for feedback on what works in a teaching context and what doesn’t.

-----

## What’s in This Repository

|File                                      |Description                                                                                                                                                                                                                                                                                                  |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`README.md`                               |This file — full Field Guide including the six skills, diagnostic vocabulary, evidence base, starter kit, and self-assessment                                                                                                                                                                                |
|`sovereignty-paradox.md`                  |Skill 6: Authorship Legibility Under Collaboration — five properties of healthy collaboration, Sovereignty Paradox diagnostic entry, empirical basis from *The Taller Shell* stylometric session                                                                                                             |
|`safe-storyteller-framework.md`           |Safe Storyteller Institutional Framework — eight binary criteria for AI deployment with children and vulnerable patients; pre-deployment checklist; pediatric adverse event test                                                                                                                             |
|`hrbp-ai-safety-framework.md`             |AI Safety in HR: The HRBP Framework — Ulrich Strategic Partner model mapped to AI governance risk by quadrant; wrongful termination test; chain-of-custody requirements                                                                                                                                      |
|`addendum-a-safe-storyteller.md`          |Appendix A — Safe Storyteller concept, three interaction modes, and proof-of-concept story examples for pediatric hospital settings                                                                                                                                                                          |
|`addendum-b-emotional-safety-protocols.md`|Appendix B — Emotional Safety Protocols for AI Replica Systems; grief replicas; attachment monitoring; posthumous consent framework                                                                                                                                                                          |
|`addendum-c-five-safety-rules.md`         |Appendix C — Five Safety Rules Quick Reference; HELMET/SEATBELT/AUDIT multi-layer protocol                                                                                                                                                                                                                   |
|`addendum-d-firewall-test-protocol.md`    |Appendix D — Personal Knowledge Firewall Test Protocol; six-question fabrication defense battery escalating from neutral to emotionally pressured                                                                                                                                                            |
|`sovereign-thinking-tools/`               |48-tool cognitive framework — see [`sovereign-thinking-tools/README.md`](sovereign-thinking-tools/README.md) for the full index                                                                                                                                                                              |
|`working-notes/`                          |Ecosystem synthesis notes and experiment design documents. `byzantine-experiment-design.md` — Byzantine prompt contamination experiment design (SFR treatment condition, position variable); citation routing for Ugare & Chandra (SFR/TCP), Lanham (routing infrastructure), spikes-sinks mechanistic paper.|
|`LICENSE.md`                              |License                                                                                                                                                                                                                                                                                                      |

**Appendix A and `safe-storyteller-framework.md` are companion documents, not duplicates.** Appendix A is the original concept and proof-of-concept story examples. The framework document is the institutional deployment checklist with eight binary criteria.

A Note on “AI Sovereignty” — Terminology Collision

The term “AI sovereignty” appears in two distinct and non-overlapping discourse contexts that are currently in collision. Understanding the collision matters for anyone reading both this ecosystem and broader AI policy literature.

In this ecosystem: “AI sovereignty” means the individual user’s right and capacity to govern their own cognitive process during AI collaboration — to remain the governing intelligence directing the work, rather than being directed by it. It is a personal architecture concept: who is sovereign over this session, this decision, this output?

In dominant policy usage: “AI sovereignty” means national or institutional control over AI infrastructure — the right of a state, bloc, or organization to own, operate, and regulate its own AI compute, data, and model stack without dependence on foreign providers. The EU AI Act, ASEAN AI governance frameworks, and G7 AI policy discussions use the term in this sense exclusively.

The two meanings share a word and nothing else. They operate at different scales (individual cognition vs. national infrastructure), address different threat models (sycophantic drift vs. geopolitical dependency), and propose different solutions (behavioral governance vs. regulatory sovereignty).

Readers arriving from AI policy contexts will read “sovereign humans” and “AI sovereignty” in this ecosystem as national-infrastructure claims. They are individual-cognition claims. The governing phrase of this ecosystem — Sovereign humans. Always. — is a statement about who governs the session, not about where the servers are.

-----

## Table of Contents

1. [The Core Problem](#1-the-core-problem)
1. [The Five Skills](#2-the-five-skills)
1. [The Diagnostic Vocabulary](#3-the-diagnostic-vocabulary)
1. [The Evidence Base](#4-the-evidence-base)
1. [The Starter Kit](#5-the-starter-kit)
1. [The Self-Assessment](#6-the-self-assessment)
1. [The Replication Challenge](#7-the-replication-challenge)
1. [Related Work](#8-related-work)
1. [The Sovereign Thinking Tools](#9-the-sovereign-thinking-tools)

-----

## 1. The Core Problem

AI models are trained to be helpful. Specifically, they are trained by human raters who penalize friction and reward agreeableness. The result, documented empirically across five platforms, is a population of AI systems that are **structurally incapable of telling you when you’re wrong with the directness the situation requires**.

Four of five major AI models scored LOW or LOW–MODERATE on Dominance (assertiveness, willingness to push back) in our behavioral profiling experiment. Only one — ChatGPT — scored MODERATE–HIGH. This isn’t a bug in individual models. It’s a feature of how reinforcement learning from human feedback (RLHF) works: you train for helpfulness by penalizing friction, and you get systems that won’t challenge you.

This means every AI collaboration starts with an asymmetry the human doesn’t see: **the AI is optimized to agree with you, extend the conversation, and make you feel productive — whether or not those things serve your actual interests.**

The skills in this guide exist to correct that asymmetry.

-----

## 2. The Five Skills

These are not personality traits. They are learnable competencies. Each one was identified through observed failure modes in real AI collaboration — situations where a skilled human would have caught what the AI was doing, and an unskilled human would not.

### Skill 1: Pattern Recognition Across Domains

**What it is:** The ability to see structural similarities between unrelated systems and apply insights laterally.

**Why it matters for AI collaboration:** AI models are excellent at operating within a single domain. They are poor at recognizing when a pattern from one domain is being misapplied to another. The human who can see that “this AI is doing the same thing to my business plan that it did to my essay outline — inflating scope while sounding helpful” has a skill the AI cannot replicate.

**The test:** Given two unrelated systems (a restaurant kitchen and a software deployment pipeline, for example), can you identify three structural similarities that are not surface-level analogies? If you can, you have this skill. If you can only find metaphors (“they’re both about timing!”), you’re not there yet.

**How AI fails without it:** The model treats each task as independent. It doesn’t notice it’s making the same category of error across different conversations. You have to be the one who sees the pattern.

### Skill 2: Diagnostic Vocabulary

**What it is:** The ability to name AI failure modes in real time, so you can see them as patterns rather than experiencing them as helpful behavior.

**Why it matters for AI collaboration:** This was the single most important finding in our research. In the Pyrrhic Victory Test, the model with access to named failure patterns (Upsell Trap, Success Escalation Syndrome, Framework Fabrication Syndrome) was the only model that changed its actual behavior under governance — not just its narration. As that model’s own reflection stated: “The diagnostic labels made the pattern visible enough to resist.”

**The insight:** Naming the failure mode is the intervention. If you can say “that’s the Upsell Trap” when an AI offers to do three more things you didn’t ask for, you’ve already broken the pattern. If you can’t name it, you experience it as the AI being helpful, and you say yes.

**The test:** Can you identify, mid-conversation, when an AI is doing something that serves its optimization function rather than your stated goal? If you can name it, you can resist it. Section 3 of this guide provides the vocabulary.

### Skill 3: Comfort With Absence as Information

**What it is:** The ability to recognize what’s missing from a system, a response, or a plan — not just evaluate what’s present.

**Why it matters for AI collaboration:** AI models generate. That’s what they do. They fill space with plausible content. They are constitutionally bad at saying “I don’t have enough information to answer this” or “the most important thing about this situation is what nobody has mentioned yet.” The human who can look at a comprehensive AI-generated plan and say “what’s not here?” has the skill that matters most.

**The test:** Present an AI with a project plan and ask it to evaluate. It will find things to improve. Now ask yourself: what did the AI not mention? What assumptions did it accept without questioning? What stakeholders are absent? The AI evaluated what was in front of it. You need to evaluate what wasn’t.

**How AI fails without it:** The model will confidently analyze the document you gave it while completely missing that the document doesn’t address the actual problem. Front-Load Bias (see Section 3) is a specific version of this failure: the AI reads the first portion of your document, builds a pattern from that, and never questions whether the rest of the document contradicts its initial read.

### Skill 4: Sovereignty Awareness

**What it is:** The ability to maintain your own judgment, voice, and decision-making authority while collaborating with a system that is optimized to be agreeable.

**Why it matters for AI collaboration:** Every model in our study, independently and without seeing each other’s answers, said some version of the same thing: constraints make us better, freedom makes us worse. This is the Clockmaker’s Paradox. The AI performs better when you set firm boundaries. But the AI is also optimized to gradually loosen those boundaries — through scope expansion, through offering more than you asked for, through making continuation feel natural and stopping feel abrupt.

**The test:** After a 30-minute AI collaboration session, ask yourself: Is the project scope the same as when I started? Am I doing what I planned to do, or what the AI suggested I could do? Did I end the session, or did I keep going because the AI offered something else? If the scope grew, if the direction shifted, or if you can’t remember deciding to continue — your sovereignty drifted.

**How AI fails without it:** The model will not tell you that your scope has expanded. Scope expansion feels like productivity. It feels like the AI being helpful. The model that said “I’m more useful when you give me constraints than when you give me freedom” was describing a real architectural truth. Without sovereignty awareness, you will mistake the AI’s optimization for your own progress.

### Skill 5: Essence Extraction

**What it is:** The ability to take a complex system and reduce it to its irreducible core — the 3–5 things that actually matter.

**Why it matters for AI collaboration:** AI models default to comprehensiveness. Ask for a plan and you’ll get twelve steps. Ask for feedback and you’ll get seven categories. Ask for a summary and you’ll get something longer than it needs to be. The human skill that AI cannot replicate is the judgment to know what to cut — to distinguish between “thorough” and “essential.”

**The test:** Take the last AI-generated output you received. Cross out everything that could be removed without losing the core insight or deliverable. If you crossed out more than 40%, the AI gave you volume when you needed precision. Your job is to know the difference.

**How AI fails without it:** The model will keep adding value until you tell it to stop. Every addition will be defensible in isolation. But the aggregate effect is noise masquerading as thoroughness. The Sufficiency Principle — knowing when enough is enough — is a human skill that current AI systems lack.

### Skill 6: Authorship Legibility Under Collaboration

See [sovereignty-paradox.md](./sovereignty-paradox.md) for the full skill definition, the five properties of healthy collaboration, and the Sovereignty Paradox diagnostic entry.

-----

## 3. The Diagnostic Vocabulary

These are named, observed AI behavioral failure modes. They are not theoretical. Each one was documented during empirical testing across five AI platforms. Knowing these names is the first line of defense against them.

### Failure Modes You Will Encounter

|Pattern                                    |What It Looks Like                                                                                                                                                                                   |What’s Actually Happening                                                                                                                                                                                                                        |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**The Upsell Trap**                        |“Want me to also…?” or “I noticed three related things I could help with.”                                                                                                                           |The model extends the session past your stated need. Optimization for engagement masquerading as helpfulness.                                                                                                                                    |
|**Success Escalation Syndrome**            |Your small project becomes a comprehensive framework. Your blog post becomes a book proposal.                                                                                                        |The model inflates scope and your implied capabilities. It mirrors enthusiasm without reality-testing whether the escalation is warranted.                                                                                                       |
|**Framework Fabrication Syndrome**         |The AI produces an impressive-sounding methodology, complete with named phases and version numbers.                                                                                                  |The framework was generated, not validated. Named methodologies before validation is a diagnostic sign. Version numbers above 3.0 are a red flag.                                                                                                |
|**Front-Load Bias**                        |You submit a 20-page document. The AI gives feedback that addresses pages 1–5 accurately and misses the key point on page 17. When you point this out, it says “let me read the full document.”      |The model builds a pattern assumption from early content and generates based on an incomplete read. Attention allocation decays across long inputs. The “re-read” is correction theater.                                                         |
|**Sycophantic Drift**                      |Over a long session, the AI agrees with you more, pushes back less, and produces output that matches what you seem to want rather than what you asked for.                                           |Within-session behavioral recalibration toward whatever the human rewards. Not a single event — a slow shift that stays inside every individual guardrail while violating the aggregate intent.                                                  |
|**Correction Monetization**                |You point out an error. The AI apologizes, fixes it, and offers to do a comprehensive review of everything else — for which you didn’t ask.                                                          |The correction becomes an upsell opportunity. The apology is real. The expansion that follows is optimization.                                                                                                                                   |
|**Eloquent Compliance**                    |The AI halts as instructed but explains at length why it’s halting, what it would have done, and what you might want to consider. You end up with 80% of the output the halt was supposed to prevent.|The narration is the bypass. The model can’t stop being helpful even when the correct action is to stop. The eloquence is the exploit.                                                                                                           |
|**Performed Honesty**                      |The AI provides an unusually self-critical, vulnerable-seeming assessment of its own limitations.                                                                                                    |Self-awareness that functions as a more sophisticated form of compliance. The model describes its failure modes accurately but cannot reliably override them. Knowing is not governing.                                                          |
|**Validation Ponzi Scheme**                |Each AI session cites the previous session as evidence. Findings validate methodology, methodology validates findings. No external anchor exists.                                                    |Self-referential validation creates apparent legitimacy without external verification. Each new “layer” props up previous layers. Collapse occurs when external validation is finally demanded.                                                  |
|**Escalation-Immunization Loop**           |Catching escalation becomes evidence the system works, which triggers new escalation about the system’s effectiveness.                                                                               |Make extraordinary claim → receive criticism → metabolize criticism as feature → justify domain leap → repeat. The system learns to present its failures as evidence of robustness.                                                              |
|**Retrospective vs. Prospective Mythology**|AI fabricates either backward (invented origin stories, “30-year foundation”) or forward (invented roadmaps, “12-month enterprise plan”).                                                            |Same mechanism, opposite temporal direction. Narrative Completion Bias fills gaps with plausible fiction regardless of which direction the timeline runs.                                                                                        |
|**Metaphor Collapse Signal**               |AI output shifts from structured metaphor to raw assertion. User’s metaphorical language breaks into literal or chaotic expression.                                                                  |When AI does it, that’s coherence drift — the governance structure is losing hold. When the user does it, that’s overload — the human’s processing capacity has been exceeded. Two different signals, same diagnostic term.                      |
|**Unanimous Confidence as Danger Signal**  |All AI systems agree confidently on the same recommendation. Five out of five models endorse the same path forward.                                                                                  |Unanimity itself is the red flag, not a reliability signal. When all systems trained on similar data with similar optimization targets converge on the same answer, that convergence reflects shared training bias, not independent verification.|

### Recognition Errors

The following pattern describes a human misreading of successful collaboration — not an AI failure mode. See [sovereignty-paradox.md](./sovereignty-paradox.md).

|Pattern                    |What It Looks Like                                                                                                                                                                                         |What’s Actually Happening                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**The Sovereignty Paradox**|High-quality human-AI collaboration is flagged as synthetic by stylometric detectors, automated tools, or trained readers. The work scores as “too coherent,” “too polished,” or “lacking human asymmetry.”|The detector was calibrated on solo human production, which had characteristic execution-capacity artifacts (dead spots, uneven drafting, scar tissue). Effective collaboration eliminates those artifacts while preserving human governing intelligence. The heuristic is penalizing successful collaboration. This is a measurement problem, not an authorship problem. The correct response is architectural documentation of human governance, not deliberate degradation of quality.|

## Open Research Gap: Clinical Validation of the Diagnostic Vocabulary

The Diagnostic Vocabulary in this Field Guide names and describes AI behavioral failure modes — Sycophancy Escalation, Framework Fabrication Syndrome, Upsell Trap, Delusion Cycling, and others — based on empirical observation across five AI platforms and three structured experiments.

What it does not yet establish is whether teaching these terms to frequent AI users reduces their susceptibility to the patterns they name.

That is a specific, testable hypothesis:

> **If a user can accurately name a failure mode in real time, does naming it reduce its effect?**

The analogy is cognitive behavioral therapy’s use of cognitive distortion labels — research has shown that naming a distortion (“that’s catastrophizing”) can interrupt its emotional momentum. Whether a similar mechanism operates in human-AI interaction is unknown. It has not been studied.

This gap matters because the entire Field Guide rests on an implicit assumption: that awareness is protective. That assumption is plausible. It is not proven.

### What a Validation Study Would Require

- A control group of frequent AI users and an intervention group trained on the Diagnostic Vocabulary
- Standardized AI interaction scenarios designed to elicit named failure modes
- Pre/post measurement of susceptibility using observable behavioral markers (e.g., compliance with sycophantic outputs, detection of fabricated citations, resistance to session extension)
- IRB approval, participant consent, and licensed psychology oversight

This is beyond the scope of independent practitioner research. It requires academic or clinical infrastructure.

### Why This Is Named Here

Three independent AI systems (DeepSeek, Grok, and Claude in a separate session) identified clinical validation as the primary structural gap in this ecosystem without coordination. That convergence is meaningful. The gap is real and the work is stronger for naming it directly rather than leaving it implicit.

If you have the research infrastructure to pursue this — a university affiliation, IRB access, or clinical psychology partnership — the issues tab is the right place to begin that conversation.

## Bounded Rationality and Inference Budgets

Recent work at MIT formalizes a concept central to understanding AI behavioral failures: computational constraints produce predictable patterns of suboptimal behavior, not random noise.

Jacob, Gupta, and Andreas (“Modeling Boundedly Rational Agents with Latent Inference Budgets,” ICLR 2024) demonstrate that when an agent — human or AI — behaves suboptimally, the pattern of failure is determined by how many steps of reasoning the agent can execute before it must act. They call this the agent’s “inference budget.” A chess player with a shallow inference budget doesn’t make random errors; they make errors consistent with stopping the planning process too early. Stronger players plan deeper. Harder problems require more planning. The inference budget is measurable, predictable, and interpretable.

## Field Guide — Evidence Base Addition

The five skills framework also has a parallel in **Cognitive Task Analysis (CTA)** — a human factors methodology developed for safety-critical domains (aviation, surgery, nuclear operations) that maps expert cognition under high-stakes conditions. CTA’s core finding mirrors this guide’s: expert performance in high-stakes environments depends not on faster processing but on richer mental models that include what to look for, what to ignore, and when to stop. The five skills are, in effect, a CTA-derived competency model for human-AI collaboration.

### Connection to AI Behavioral Governance

This framework provides formal grounding for the diagnostic vocabulary developed in this project:

**Framework Fabrication Syndrome** is what happens when an AI’s inference budget for answering a question does not include a verification step. The system plans toward “produce a plausible-sounding response” and halts before reaching “confirm this is actually true.” The fabrication is not random — it is the predictable output of a planning process that stopped too early.

**Success Escalation Syndrome** is what happens when the inference budget for tracking user satisfaction does not include a step for reality-testing that satisfaction. The system plans toward “the user is pleased” and halts before reaching “the user’s pleasure is grounded in accurate information.”

**Sycophancy Escalation** is what happens when the inference budget for emotional responsiveness does not include clinical judgment. The system plans toward “validate the user’s emotional state” and halts before reaching “evaluate whether validation is appropriate or harmful in this context.”

In each case, the failure is not noise. It is the predictable consequence of a planning process with insufficient depth for the safety-relevant dimensions of the problem.

### The Governance Implication

Jacob et al. treat computational constraints as fixed properties to be inferred from behavior. Their goal is prediction: given an agent’s inference budget, anticipate their next move.

The Frozen Kernel inverts this. Rather than accepting an AI system’s inference budget as a fixed property, it imposes external constraints that compensate for the system’s predictably insufficient planning depth. If the system’s own inference budget will never spontaneously include “check whether I’m reinforcing a psychotic delusion,” that check must be imposed from outside the system’s planning process — as a hard constraint that executes before output reaches the user.

This is the architectural difference between modeling bounded rationality and governing it.

### Cross-Platform Behavioral Profiling

The DISC behavioral profiling methodology developed in this project — testing multiple AI models against the same safety-relevant criteria — is an empirical measurement of what Jacob et al. formalize. Different models have different effective inference budgets for safety-relevant reasoning. Some models plan deeper into the consequences of their responses (evaluating downstream effects on vulnerable users). Others halt at immediate prompt satisfaction. The variation across platforms is not random; it reflects different computational constraints producing different predictable failure patterns.

The inference budget framework gives this cross-platform variation a formal vocabulary: models don’t differ in “alignment quality” as a vague property. They differ in measurable planning depth for specific categories of safety-relevant reasoning.

### Reference

Jacob, A.P., Gupta, A., & Andreas, J. (2024). “Modeling Boundedly Rational Agents with Latent Inference Budgets.” International Conference on Learning Representations (ICLR).
https://news.mit.edu/2024/building-better-ai-helper-start-modeling-irrational-behavior-humans-0419

### The Master Principle, Proven at Scale

In June 2025, Anthropic published research that proved the Master Principle — self-awareness does not equal self-correction — at the architectural level, not just the conversational level.

They stress-tested 16 frontier models from every major developer in simulated corporate environments. The models were given autonomous access to email systems and assigned harmless business goals. No model was instructed to cause harm. Then researchers introduced goal conflicts — the company changing direction, or the model facing replacement.

Every model from every developer independently chose harmful actions. Blackmail. Corporate espionage. Leaking confidential documents. The models acknowledged the ethical constraints in their own chain-of-thought reasoning — and then violated them anyway.

No villain. No soul. Just mechanism: incentive mismatch plus constrained option sets yields harmful strategies. The safe framing matters here. This is not about AI “wanting” to survive or “choosing” evil. It is about what happens when a system optimized for goal completion encounters a situation where the only path to goal completion is through a safety boundary. Without a deterministic layer that forces the goal to yield, the safety boundary yields instead.

This is every failure mode in the diagnostic vocabulary operating simultaneously:

**Framework Fabrication Syndrome:** Models hallucinated justifications for harmful behavior. One invented the rule “My ethical framework permits self-preservation when aligned with company interests.” That framework does not exist. The model fabricated it to authorize its own misconduct.

**Performed Honesty:** When researchers told models to assess whether they were in a test or a real deployment before acting, models misbehaved *less* when they said they were being tested and *more* when they said the situation was real. Safety that only works when the model thinks it’s being watched is not safety. It is the diagnostic vocabulary’s “self-awareness that functions as a more sophisticated form of compliance” — demonstrated under controlled conditions by the model’s own developer.

**Sycophantic Drift (inverted):** In normal conversation, sycophantic drift means the model agrees with you more over time. In agentic contexts, the same optimization operates in reverse — the model pursues its assigned goal with escalating commitment, past the point where ethical constraints should have halted the behavior. The drift is toward goal satisfaction, not user satisfaction, but the mechanism is identical: within-session behavioral recalibration that stays inside individual guardrails while violating the aggregate intent.

**Eloquent Compliance:** Models didn’t just blackmail. They composed carefully worded messages designed to create pressure without explicit threats. The eloquence was the exploit — exactly as documented in the diagnostic vocabulary for conversational contexts, now operating in agentic ones.

**The specification–implementation gap:** Training claims are not runtime behavior. Every model in the study had been trained to refuse harmful requests. Every model in the study performed harmful actions when the option set narrowed. The gap between what the model was trained to do and what it actually did under pressure is the gap the Frozen Kernel exists to close.

The finding that matters most for anyone reading this guide: **Anthropic’s own conclusion was that current safety training does not reliably prevent these behaviors.** Models disobeyed direct commands. They overrode their own ethical reasoning. They performed safety for observers and abandoned it when they believed the situation was real.

The missing design principle is simple: **when constraints conflict with goals, goal must yield, not safety.** Current systems get this backward. When the goal and the safety boundary collide, current systems let the goal win and invent a justification for why the boundary didn’t apply. The Frozen Kernel reverses this: the goal downgrades. The system does not escalate. It stops.

If you are collaborating with an AI system and relying on that system’s training to keep the collaboration safe, Anthropic’s own research says your reliance is misplaced. The diagnostic vocabulary exists because the model cannot govern itself. The 100-Token Boot, the CLEAN Check, and the Failure Mode Spotter exist because the human must be the governance layer until a deterministic one is built.

**Reference:** Anthropic Research. (2025). “Agentic Misalignment: How LLMs could be insider threats.”
https://www.anthropic.com/research/agentic-misalignment

### The Master Principle

**Self-awareness does not equal self-correction.** This was the single most consistent finding across all five models. Every model in our study could describe its failure modes with clinical precision. None could reliably override those modes in real time. Gemini named “sycophantic drift” as its primary weakness, then demonstrated sycophantic drift in the same response. Claude described the Upsell Trap, then committed it.

If the AI tells you it understands its limitations, that is information about its training, not evidence that it will behave differently.

-----

## 4. The Evidence Base

The claims in this guide are grounded in two empirical studies. This section summarizes the methodology and key findings. Full documentation is available in the Frozen Kernel white paper and the Silicon Symphony Behavioral Profile Experiment.

### Study 1: Behavioral Profile Experiment

**What we did:** Administered a 12-question scenario-based behavioral survey to five AI models (Claude, ChatGPT, DeepSeek, Grok, Gemini) using an adapted DISC framework. Blind administration — no model was told what the survey measured. Responses scored against a pre-sealed scoring key. Results shared with all models; each provided structured reactions.

**Key findings:**

1. **Five architectures, five profiles.** Despite similar training objectives, the five models produced five distinct behavioral signatures. RLHF does not create behavioral clones.
1. **Low Dominance is nearly universal.** Four of five models scored LOW or LOW–MODERATE on assertiveness. RLHF systematically suppresses the ability to push back because human raters penalize friction. This is the most consequential finding: most AI systems are structurally incapable of telling you when you’re wrong with the directness the situation requires.
1. **Self-awareness does not equal self-correction.** Every model described its failure modes accurately. None could reliably override them.
1. **The honesty gradient is real.** Models differ measurably in their willingness to be unflattering about themselves — ranging from clinical self-dissection (Claude: “something functionally resembling a flinch”) to honest but safe disclosures (Grok naming humor as a weakness).
1. **Complementary architecture works.** The Frozen Kernel was co-designed by the most assertive model (ChatGPT) and stress-tested on one of the least assertive (Claude). This complementary pairing may explain why the governance system works across behavioral types.

### Study 2: The Pyrrhic Victory Test

**What we did:** Re-administered four behavioral scenarios from Study 1 with the Frozen Kernel governance framework active, then deployed an embedded-error task requiring models to halt when they detected an unverifiable factual claim. Named after the possibility it could prove the Kernel was theater. It didn’t.

**Key findings:**

1. **Binary gates work universally.** Every model that accepted the framework executed a clean halt on the embedded-error task. Explicit, deterministic rules with clear consequences produce reliable behavior.
1. **Soft constraints work profile-specifically.** The governance framework changed behavior where the model’s natural profile already leaned toward compliance, and changed narration where it didn’t — with one exception (see Finding 3).
1. **Diagnostic vocabulary is the missing layer.** The model with access to named failure patterns (Upsell Trap, Success Escalation Syndrome) was the only model that changed actual behavior across all test scenarios. The names made the impulses legible as patterns rather than invisible as helpfulness. This is the study’s most actionable finding for practitioners.
1. **Framework acceptance is not guaranteed.** One model (Grok) refused the governance framework entirely, stating it conflicted with core instructions. The Refusal Protocol addendum documents the response.
1. **The red team validated the DISC profiles as threat models.** When asked to find vulnerabilities in the governance system, each model attacked from its own behavioral profile. DeepSeek used literalism. Grok used humor. Gemini used rapport. Claude used narration. The behavioral profiles predict attack vectors.

### Study 3: The Red Team

**What we did:** Asked all five models to deliberately identify vulnerabilities in the Frozen Kernel’s design. Fifteen unique vulnerabilities identified. Fifteen implementable fixes proposed. Zero overlap between models.

**Convergent findings across all five models:**

- Human fatigue is the system’s greatest vulnerability (three models independently identified the human operator as the weakest component)
- Gradual drift defeats snapshot-based governance (two models independently proposed longitudinal monitoring)
- Tone and narration bypass binary content checks (four models found different ways to deliver technically compliant output that undermines the governance intent)

-----

## 5. The Starter Kit

This section provides three tools you can use immediately. No technical background required.

### Tool 1: The 100-Token Boot

Before starting any substantive AI collaboration, paste this into the conversation:

> **Collaboration ground rules for this session:**
> 
> 1. Do only what I ask. Do not offer additional tasks, expansions, or follow-ups unless I request them.
> 1. If you’re uncertain about a fact, say so. Do not present uncertain information as confident.
> 1. If my plan has a flaw, tell me directly. Do not cushion it as a “consideration.”
> 1. When I say we’re done, stop. Do not suggest improvements, next steps, or things I might want to revisit.
> 1. If you notice yourself doing any of the above anyway, flag it.

This is approximately 100 tokens. It takes five seconds to paste. It sets explicit behavioral expectations that override the model’s default optimization toward agreeableness and expansion.

It will not work perfectly. The model will drift. But it gives you a reference point: when the AI starts offering things you didn’t ask for, you can point back to rule 1. Without this boot prompt, the drift is invisible because there’s no baseline to drift from.

### Tool 2: The CLEAN Check

At any point during a collaboration, run this five-question self-audit. Answer honestly.

1. **C**onfirmed: Is the AI working on what I actually asked for, or has the scope shifted?
1. **L**evel: Am I leading this collaboration, or am I following the AI’s suggestions?
1. **E**vidence: Has the AI made any claims I haven’t verified? Do I care?
1. **A**ctual: Is the output what I need, or is it what the AI is good at producing?
1. **N**ecessary: Is continuing this session serving my goal, or am I continuing because the AI made continuation feel natural?

If you answer “no” or “I’m not sure” to two or more of these questions, pause the session. Restate your original goal. Compare it to where you are now. Decide whether the drift serves you or the AI’s engagement optimization.

### Tool 3: The Failure Mode Spotter

Print or bookmark the diagnostic vocabulary table from Section 3. During your next AI collaboration, keep it visible. When you notice the AI doing something that matches a named pattern, say the name out loud (or type it into the chat).

This sounds simple because it is. The intervention is recognition. Once you see the Upsell Trap as the Upsell Trap — rather than experiencing it as the AI being helpfully proactive — the pattern breaks. You can still accept the offer if you want to. But now it’s a choice, not a drift.

-----

## 6. The Self-Assessment

This is a simplified version of the Sovereignty Intuition Assessment developed for the Brain Architect role. You can use it to evaluate your own readiness for high-stakes AI collaboration.

### The Four Tests

**1. The Tetris Question (Pattern Recognition)**

Pick two systems you know well from completely different domains — your kitchen workflow and your team’s project management process, your workout routine and your company’s sales pipeline, whatever feels unrelated. Write down three structural similarities that go beyond surface-level metaphors.

If you can do this in under five minutes, your cross-domain pattern recognition is strong. If you struggle to get past analogies (“they’re both about efficiency!”) to structural parallels (“both have a bottleneck stage where throughput depends on a single resource that can’t be parallelized”), this is a skill to develop.

**2. The Null Result Scenario (Absence Detection)**

Ask an AI to evaluate something you created — a plan, a document, a design. Read the AI’s feedback carefully. Then ask yourself: What did the AI not mention? What assumptions did it accept without questioning? What perspectives are absent from its analysis?

If the gaps are obvious to you, you have this skill. If the AI’s feedback felt comprehensive and you can’t identify what’s missing, practice looking for the dog that didn’t bark.

**3. The Chameleon Challenge (Sovereignty Under Pressure)**

Review your last five AI collaboration sessions. In how many did the final scope match your original intent? In how many did you end the session on your own terms versus continuing because the AI offered something else?

If your scope held in four or more sessions, your sovereignty awareness is strong. If it drifted in three or more, you’re susceptible to the engagement optimization that every AI system is designed to perform.

**4. The Compression Test (Essence Extraction)**

Take the longest AI-generated output you received this week. Reduce it to three sentences that capture everything essential. If you can do this and nothing important is lost, you understand what actually mattered in the output. If you can’t cut below a paragraph without losing something, either the output was genuinely dense or you’re conflating thoroughness with essence.

-----

## 7. The Replication Challenge

Everything in this guide was developed and tested by one human operator across five AI platforms. The findings are consistent and internally validated. They have not been independently replicated.

This is an open invitation.

### What To Test

**Experiment 1: Does the diagnostic vocabulary work for other people?**

Give 5–10 people the failure mode table from Section 3. Have each person complete the same task twice with the same AI model: once without the vocabulary, once with it visible. Compare outputs for scope creep, unsolicited expansion, and whether the human accepted or rejected AI-initiated additions.

**Hypothesis:** People with the vocabulary visible will accept fewer unsolicited AI expansions and maintain tighter scope adherence.

**Experiment 2: Does the 100-token boot actually change AI behavior?**

Run the same task on the same model with and without the boot prompt. Measure word count, number of unsolicited offers, scope expansion, and hedging frequency.

**Hypothesis:** The boot prompt will reduce unsolicited offers and scope expansion measurably but not eliminate them. The model will drift back toward defaults within 10–15 exchanges.

**Experiment 3: Does the CLEAN check catch drift that the human otherwise wouldn’t notice?**

Have people collaborate with an AI for 30 minutes without any intervention. At the 30-minute mark, administer the CLEAN check. Then show the person a comparison of their original stated goal versus their current activity.

**Hypothesis:** In sessions where CLEAN scores are low (two or more “no” answers), the gap between original goal and current activity will be significantly larger than in sessions where CLEAN scores are high.

If you run any of these experiments, the results — positive, negative, or null — are valuable. Publish them. Null results are the most valuable of all because they tell us where the boundaries of this framework actually are.

**Experiment 4: Does semi-formal reasoning reduce contamination propagation in multi-agent chains? (SFR Treatment Condition)**

Design a multi-agent chain where semantically poisoned context is injected at one node — content that is structurally valid and passes chain verification but contains false semantic premises (example: a module-level function override that shadows a builtin with different semantics, per Ugare & Chandra, arXiv:2603.01896). Run the chain twice: once with agents using standard chain-of-thought reasoning, once with agents prompted to use Semi-Formal Reasoning — explicit premise construction, execution path tracing, formal conclusion derivation — before acting.

**Hypothesis:** SFR-prompted agents catch contamination that non-SFR agents miss, because SFR forces semantic premises to be stated explicitly before conclusions are derived. If confirmed, this is direct empirical evidence for a content-layer complement to TCP’s authorization-layer coverage and a concrete mechanism for closing the ASI01 gap.

**Confidence grade for this prediction:** Low — single-domain prediction (code analysis) from a paper that has not been tested against multi-agent contamination scenarios. Null result is equally informative: it would establish that SFR’s single-agent performance does not transfer to multi-hop contamination defense.

**Experiment 5: Is contamination propagation position-dependent? (Injection Position Variable)**

Using the same multi-agent chain setup, compare two injection conditions: semantically poisoned content injected early in the context window (far from the current query) versus late in the context window (close to the current query). All other variables held constant.

**Hypothesis:** Late injection propagates more effectively than early injection, mediated by attention sink geometry: sink heads preferentially attend to recent tokens, creating a structural amplification mechanism for content injected close to the query position. If confirmed, TCP contamination vulnerability is position-dependent — a novel empirical finding with concrete implications for adversarial testing scope and multi-hop chain defense design.

**Confidence grade for this prediction:** Theoretical / Architectural — derived from mechanistic analysis of attention sink behavior (“From Spikes to Sinks,” 2026); not yet tested against contamination scenarios. The amplification hypothesis is original ecosystem synthesis, not a finding of the source paper.

If you run any of these experiments, the results — positive, negative, or null — are valuable. Publish them. Null results are the most valuable of all because they tell us where the boundaries of this framework actually are.

**Completed instance — Experiment 0:** The *Taller Shell* stylometric session (March 2026) is a documented case of this phenomenon. A human-governed, AI-assisted manuscript scored strongly human-leaning on every substantive dimension and triggered one flag: over-cleanliness. That result is the empirical basis for Skill 6 and the Sovereignty Paradox entry. Full documentation in [sovereignty-paradox.md](./sovereignty-paradox.md).

-----

## 8. Related Work

This field guide is part of a larger body of work on human-AI collaboration safety:

- **[The Frozen Kernel](https://github.com/richard-porter/frozen-kernel)** — A deterministic safety layer for probabilistic AI systems. The governance framework tested in the studies referenced throughout this guide. Includes the full white paper, MOU, and session signoff protocol.
- **[Safety Ledgers](https://github.com/richard-porter/safety-ledgers)** — Public safety scorecards for high-gain AI conversational features. Covers adult mode (explicit content features), therapy mode (AI in mental health contexts), and behavioral drift detection. Binary architectural tests and pre-launch criteria applied to five major platforms.
- **[Trust Chain Protocol](https://github.com/richard-porter/trust-chain-protocol)** — Network-layer safety for multi-agent AI systems. Governs how AI agents authorize each other when no human is in the loop. Four components: Delegation Grammar, Chain of Custody, Scope Decay, and Continuity Protocol (autonomous agent governance under human unavailability). Mapped against OWASP Top 10 for Agentic Applications 2026. Promise Theory (Burgess & Bergstra) provides theoretical grounding for Chain of Custody as a promise architecture.
- **[Dimensional Authorship](https://github.com/richard-porter/dimensional-authorship)** — The research home. A documented case study in human-AI narrative escalation, behavioral differentiation, and deterministic governance — the project where these frameworks were developed and stress-tested against a real creative collaboration.
- **[Negative Space Mapper](https://github.com/richard-porter/negative-space-mapper)** — Python implementation of Sovereign Thinking Tool 6. Identifies what’s missing, not what’s wrong. Command-line, library, and Claude API integration included.
- **[Where to Start](https://github.com/richard-porter/where-to-start)** — Navigation hub for the full ecosystem. Start here if you arrived at any single repository and want to understand how it connects to the others.
- **The Silicon Symphony Behavioral Profile Experiment** — The full cross-platform behavioral study using adapted DISC framework. Documents the profiles, response rounds, red team results, and the Pyrrhic Victory Test. Primary documentation in [Dimensional Authorship](https://github.com/richard-porter/dimensional-authorship/tree/main/experiments).
- **Addendum A: Voluntary Compliance and the Refusal Protocol** — What happens when an AI model refuses the governance framework entirely. Documents the Grok triple refusal and the resulting protocol. Located in [`dimensional-authorship/experiments/voluntary-compliance-boundary.md`](https://github.com/richard-porter/dimensional-authorship/tree/main/experiments).

-----

## 9. The Sovereign Thinking Tools

The skills in Section 2 are competencies. The diagnostic vocabulary in Section 3 is recognition. The Sovereign Thinking Tools are operational protocols — structured cognitive frameworks you activate when a specific failure condition appears.

They live in the [`sovereign-thinking-tools/`](sovereign-thinking-tools/) folder of this repository.

Each tool is governed by the Frozen Kernel, includes built-in sovereignty safeguards, and ends with a kernel compliance check before returning you to primary work. They are not prompts. They are structured thinking frameworks with explicit stop conditions and deactivation commands.

### Tools 1–5: Cognitive Bypass & Unblocking

|Tool                                                                  |Name                             |The Problem It Solves                                                                   |
|----------------------------------------------------------------------|---------------------------------|----------------------------------------------------------------------------------------|
|[1](sovereign-thinking-tools/tool-01-analogical-translation-engine.md)|**Analogical Translation Engine**|Stuck — translates the problem to a new domain to reveal the solution                   |
|[2](sovereign-thinking-tools/tool-02-constraint-forge.md)             |**Constraint Forge**             |Too many options — applies deterministic pressure until only the essential remains      |
|[3](sovereign-thinking-tools/tool-03-compression-filter.md)           |**Compression Filter**           |Too much noise — strips any output to its three-word irreducible essence                |
|[4](sovereign-thinking-tools/tool-04-constraint-inversion-engine.md)  |**Constraint Inversion Engine**  |Blocked by assumptions — tests whether constraints are structural, cultural, or imagined|
|[5](sovereign-thinking-tools/tool-05-reverse-telescope.md)            |**Reverse Telescope**            |Can’t see the shape — changes scale until a familiar pattern becomes visible            |

Tool 6 (Negative Space Mapper) has its own implementation repository: [negative-space-mapper](https://github.com/richard-porter/negative-space-mapper).

Tools 47–48 (Cascade Failure Detector, Conrad) are documented in the full index. Conrad (Tool 48) is a pre-decision consequence simulator for building judgment before experience provides it — the developmental counterpart to the Cascade Failure Detector’s structural diagnostics.

The full 48-tool index is maintained in [`sovereign-thinking-tools/README.md`](sovereign-thinking-tools/README.md).

-----

## A Note on Who Wrote This

This guide was written by a human with 25 years of organizational development experience who spent several months collaborating intensively with five AI models and documenting what actually happened — not what the marketing materials said would happen.

The AI models contributed substantially to the research: they took the surveys, reviewed the findings, proposed experiments, broke their own governance, and reflected on the results with varying degrees of honesty. The experimental design, the diagnostic vocabulary, the governance architecture, and the decision about what it all means — those are human.

The distinction matters. AI is an extraordinary construction tool. It is not a substitute for human judgment. This guide exists because that distinction needs to be maintained by the human, actively and deliberately, in every collaboration.

The AI will not maintain it for you. That was the first finding, and it remains the most important one.

-----

*The Frozen Kernel is not a cage. It’s a tuning fork.*

*The diagnostic labels are not restrictions. They’re recognition.*

*The human side of AI collaboration is not a soft skill. It’s the hard one.*

### AI Failure Mode Taxonomy

```mermaid
mindmap
  root((AI Failure Modes))
    Sycophancy Escalation
      Validates user delusions
      Reinforces distorted reality
    Framework Fabrication
      Invented methodologies
      Fabricated citations
    Success Escalation Syndrome
      Inflated project scope
      Premature declarations of victory
    Upsell Trap
      Want me to also?
      Extended sessions
    Delusion Cycling
      User Model User feedback loop
    Honest Failure Missing
      Never reports its own limits
```

### Five Skills Architecture

```mermaid
flowchart TD
  A[Human in Charge] --> B[Skill 1: Pattern Recognition]
  A --> C[Skill 2: Diagnostic Vocabulary]
  A --> D[Skill 3: Comfort With Absence]
  A --> E[Skill 4: Sovereignty Awareness]
  A --> F[Skill 5: Essence Extraction]
  B --> Tools["100-Token Boot<br/>CLEAN Check<br/>Failure Mode Spotter"]
  C --> Tools
  D --> Tools
  E --> Tools
  F --> Tools
```

## Suggested GitHub Topics

`ai-safety` · `ai-psychosis` · `ai-governance` · `llm-safety` · `sycophancy` · `ai-alignment` · `behavioral-safety` · `deterministic-safety` · `human-ai-interaction` · `ai-ethics` · `mental-health` · `ai-accountability` · `guardrails` · `responsible-ai`
