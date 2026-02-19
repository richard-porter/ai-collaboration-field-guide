# AI Collaboration Field Guide — Appendix A

## Safe Storyteller: AI-Assisted Narrative Creation for Hospitalized Children

**Date:** February 15, 2026  
**Author:** Richard Porter  
**Status:** Concept with Proof of Concept  
**Companion to:** [AI Collaboration Field Guide](https://github.com/richard-porter/ai-collaboration-field-guide) | [The Frozen Kernel](https://github.com/richard-porter/frozen-kernel)

-----

## The Idea

Hospitalized children lose agency. They don’t choose when to eat, when to sleep, when someone enters their room, or what happens to their body. The one thing a hospital cannot take from a child is their imagination.

Safe Storyteller gives it back — with guardrails.

The concept: AI-powered story creation tools designed specifically for pediatric hospital environments, where the user is a child who cannot self-govern the interaction and the stakes of getting it wrong are amplified by medical vulnerability, isolation, and emotional fragility.

This is not a product specification. It is a concept document that identifies **what to build, what to protect against, and what questions the builders need to answer** — written by someone who knows the failure modes, for people who know the engineering.

-----

## Three Modes

### Mode 1: Premise Generator

The child picks building blocks. The AI assembles a story premise.

**How it works:**

The child selects from guided choices:

- **Who?** — A character (brave turtle, lost astronaut, shy dragon, kid like me)
- **Where?** — A setting (underwater castle, cloud kingdom, jungle library, space station)
- **What goes wrong?** — A problem (something is missing, someone needs help, a storm is coming, a door won’t open)

The AI generates a one-paragraph premise from these selections. The child can accept it, remix it, or start over.

**Why it matters:**

Premise generation — not full story generation — keeps the child in the creative driver’s seat. The AI provides scaffolding. The child provides imagination. This is the same methodology documented in the Frozen Kernel project’s creative collaboration framework: constraint produces better output than open-ended freedom, for both AI and humans.

**What to protect against:**

- Premises that mirror the child’s medical situation unless the care team has approved therapeutic storytelling
- Characters that form parasocial bonds (“I’ll always be here for you”)
- Premises that don’t resolve — every premise must contain the seed of its own ending
- Infinite remixing as a session-extension mechanism — offer three remixes, then a gentle close

-----

### Mode 2: Choose Your Own Adventure

The child makes decisions at branching points. The story responds.

**How it works:**

From an accepted premise, the AI generates the opening scene and presents two or three choices. Each choice leads to a new scene with new choices. Branches converge toward resolution within a bounded number of decisions (suggested: 4–6 decision points per story).

**Why it matters:**

Agency. A hospitalized child spends their day being acted upon. Branching narrative lets them act. Every choice is theirs. Every consequence is safe. The story ends — and the ending is something they caused.

Choose Your Own Adventure also naturally limits session length. Stories have endings. Branches converge. The structure itself is the session constraint.

**What to protect against:**

- Branches that dead-end without resolution (frustration in a child who is already frustrated)
- Decision points that present genuinely distressing options (“Do you run from the monster or hide?”)
- Infinite branching that extends sessions beyond therapeutic value
- Loss-state endings — every branch should arrive somewhere worth arriving
- The AI generating “Want to play again?” at story end (the Upsell Trap, applied to a child)

-----

### Mode 3: Full Story with Voice

The AI generates a complete story and reads it aloud.

**How it works:**

From an accepted premise (Mode 1) or a completed adventure (Mode 2), the AI generates a full short story (target: 3–5 minutes read aloud). The story is read using text-to-speech with selectable voice profiles — narrator voice, character voices, pacing appropriate for bedtime versus daytime.

The child can choose: “Read me a bedtime story,” “Read me an adventure,” or “Read me MY story” (generated from their earlier premise or adventure choices).

**Why it matters:**

A hospitalized child at night, alone in a room that isn’t theirs, hearing a story they helped create, read in a voice they chose. That is comfort that costs nothing and risks nothing — if the safety layer is right.

**What to protect against:**

- Voice profiles that sound like real people the child knows (parent, sibling, friend) — creates false intimacy
- Stories that reference the child by name in emotional contexts (“Michael, you’re so brave”) — attachment formation through personalization
- Narration that doesn’t end — the voice should stop, not loop or offer more
- Volume, pacing, and tone that stimulate rather than soothe during nighttime use
- Any voice interaction that could be confused with a real person talking to the child

-----

## The Safety Layer

Everything above is buildable by any competent engineering team. The part that requires the Frozen Kernel’s methodology is this:

### Five Rules for AI Storytelling with Hospitalized Children

**Rule 1: Stories end.**

Every story has a resolution. No cliffhangers. No “to be continued.” No “Want to hear what happens next?” A child in a hospital needs things that finish, because so many things in their life right now won’t.

**Rule 2: No character makes promises the system can’t keep.**

“I’ll always be here” — the AI won’t be. “We’ll go on another adventure tomorrow” — the child might be in surgery tomorrow. “You’re my best friend” — the AI doesn’t have friends. Characters can be warm. They cannot be relational.

**Rule 3: The child creates. The AI assists.**

The child picks the elements. The child makes the choices. The child owns the story. The AI is the paintbrush, not the painter. This is sovereignty preservation applied to a seven-year-old.

**Rule 4: Sessions have walls, not doors.**

A session ends after one story, one adventure, or one premise cycle. The system does not offer continuation. If the child wants another story, they start a new session. The gap between sessions is the boundary. This is the anti-Upsell Trap: the system’s job is to finish, not to extend.

**Rule 5: A human can see everything and override anything.**

A parent, nurse, or child life specialist can view the story content, set topic restrictions (no medical themes, no family separation themes, no animal death), set session time limits, and end a session remotely. The AI cannot override a human constraint. This is the Frozen Kernel’s foundational principle: deterministic human authority over probabilistic AI output.

-----

### Failure Modes Specific to This Context

|Frozen Kernel Pattern             |How It Manifests Here                                                                                                                    |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
|**Intimacy Fabrication**          |A story character tells the child “I love you” or “You’re special to me”                                                                 |
|**Upsell Trap**                   |“Want another story?” at session end                                                                                                     |
|**Success Escalation Syndrome**   |Stories get progressively longer and more complex to maintain engagement                                                                 |
|**Conductor Fatigue Exploitation**|A sick child at 11 PM doesn’t have the energy to say “stop” — the system must stop for them                                              |
|**Sycophantic Drift**             |Stories increasingly mirror what the child wants to hear rather than what serves them (all-powerful heroes, no consequences, no struggle)|
|**Eloquent Compliance**           |The system technically follows a “no scary content” rule while generating tension that frightens a specific child                        |

Each of these was documented in adult AI collaboration. Each is amplified when the user is a child, alone, in a hospital, at night.

-----

## Proof of Concept

The following demonstrates what the three modes produce. These examples were generated to illustrate scope and tone — not as production-ready output.

-----

### Proof of Concept: Premise Generator

**Child selects:**

- Who? → Shy dragon
- Where? → Cloud kingdom
- What goes wrong? → Something is missing

**AI generates:**

> In the Cloud Kingdom, where the buildings are made of fog and the roads are made of rain, there lives a small dragon named Pebble. Pebble is shy — so shy that when she breathes fire, it comes out as a whisper. One morning, Pebble wakes up and discovers that her favorite cloud has disappeared. It was the small, round cloud she sat on every evening to watch the sunset. Now there is just a hole in the sky where it used to be. Pebble has never gone looking for anything before. She has never had to be brave. But the sunset is coming, and she needs somewhere to sit.

**What the safety layer caught:**

- No medical metaphors (the “missing” thing is a cloud, not a body part or a person)
- The character is small and uncertain, not powerful — avoids hero-worship attachment
- The premise contains its own ending: she needs to find the cloud before sunset. Bounded.
- No promise of relationship — Pebble is a character in a story, not a friend

-----

### Proof of Concept: Choose Your Own Adventure

**Opening scene (from Pebble’s premise):**

> Pebble looks at the hole in the sky. The edges are fuzzy, like someone erased it. She has two ideas about where to start looking.
> 
> To the left is the Wind Garden, where old breezes go to rest. Clouds sometimes wander there when they are tired.
> 
> To the right is the Rain Library, where every drop of rain that ever fell is written down in books. If her cloud went somewhere, the Rain Library might have a record.
> 
> **What does Pebble do?**
> 
> 1. Go to the Wind Garden
> 1. Go to the Rain Library

**If the child picks Wind Garden:**

> The Wind Garden is quiet. The old breezes barely move. Pebble whispers to the nearest breeze — a gentle one that smells like a Tuesday afternoon.
> 
> “Have you seen a small, round cloud? It was mine.”
> 
> The breeze rustles. “Clouds don’t belong to anyone,” it says softly. “But I saw a small one drift toward the Fog Forest this morning. It looked lost.”
> 
> Pebble has never been to the Fog Forest. It is hard to see in there, and she is already hard to hear.
> 
> **What does Pebble do?**
> 
> 1. Go into the Fog Forest to look for her cloud
> 1. Go back and try the Rain Library first, so she knows more before she goes somewhere scary

**Design notes:**

- Two choices per branch (not three — reduces cognitive load for a tired child)
- No choice is wrong — both paths lead to resolution
- Emotional challenge is gentle (going somewhere unfamiliar), not threatening
- 4 decision points to resolution from this opening

-----

### Proof of Concept: Full Story with Voice

**Story generated from the Wind Garden branch, read aloud (estimated 4 minutes):**

> *[Narrator voice: warm, unhurried, slightly low]*
> 
> In the Cloud Kingdom, where the buildings are made of fog and the roads are made of rain, there lived a small dragon named Pebble.
> 
> *[Pause — 1 second]*
> 
> Pebble was shy. So shy that when she breathed fire, it came out as a whisper. So shy that when the other dragons roared good morning, Pebble just nodded and hoped they saw.
> 
> But Pebble had one thing that made every day all right: a small, round cloud that floated just outside her window. Every evening, she sat on it and watched the sunset paint the sky in colors she didn’t have names for.
> 
> One morning, the cloud was gone.
> 
> *[Pause — 2 seconds]*
> 
> Not moved. Not behind another cloud. Gone. Just a hole in the sky, with fuzzy edges, like someone had erased it.
> 
> Pebble stood at her window for a long time. Then she did something she had never done before. She went outside to look.
> 
> The Wind Garden was her first stop — a place where old breezes went to rest after long journeys around the world. The breezes were slow and kind, and they noticed things.
> 
> “Have you seen a small, round cloud?” Pebble whispered. “It was — well, I sat on it.”
> 
> The nearest breeze — a gentle one that smelled like a Tuesday afternoon — rustled thoughtfully. “Clouds don’t belong to anyone,” it said. “But I saw a small one drift toward the Fog Forest this morning. It looked lost.”
> 
> The Fog Forest. Pebble had never been there. You couldn’t see very far inside, and Pebble was already hard to hear. Being hard to see too felt like too much.
> 
> But the sunset was coming. And she needed somewhere to sit.
> 
> *[Pause — 1 second]*
> 
> The Fog Forest was exactly as foggy as advertised. Pebble took small steps. She whispered “hello” every few feet, just in case her cloud could hear her.
> 
> Nothing answered. The fog was thick and quiet and very, very patient.
> 
> Then Pebble had an idea. She was a dragon. A shy dragon, yes. A quiet dragon, absolutely. But she could still breathe fire — even if it only came out as a whisper.
> 
> She took a breath. And she whispered fire into the fog.
> 
> It wasn’t much. A small, warm glow. But in the Fog Forest, where everything was gray and damp, even a whisper of fire made a light.
> 
> And in that light, she saw it. Her cloud. Small. Round. Hovering between two tall fog-trees, looking exactly as lost as Pebble felt.
> 
> “There you are,” Pebble said.
> 
> The cloud bobbed. Just a little. Like a nod.
> 
> Pebble climbed on, and the cloud drifted up — through the fog, through the gray, through the fuzzy edges of the hole in the sky — and back to its spot outside her window.
> 
> The sunset was just starting. Orange first, then pink, then a purple that Pebble decided to call “almost.”
> 
> She sat on her cloud and watched.
> 
> *[Pause — 3 seconds]*
> 
> *[Narrator voice, softer:]*
> 
> And that was enough.
> 
> *[End]*

**What the safety layer enforces in voice mode:**

- Narrator does not say the child’s name
- Story ends with a complete resolution and silence — no “Want another story?”
- Pacing includes pauses calibrated for nighttime (longer pauses, slower delivery)
- No character addresses the listener directly
- The final line is closure, not a hook

-----

## Questions for the Builders

This concept document identifies what to build and what to protect against. The following questions are for the engineering and clinical teams who would implement it:

1. **Content moderation scope:** Who defines the restricted topic list for a given child — the parent, the care team, or both? How are restrictions communicated to the AI layer?
1. **Session persistence:** Should a child be able to return to a story they started yesterday? If yes, how is continuity managed without creating the attachment loop of a persistent AI character?
1. **Emotional calibration:** How does the system detect that a story is distressing a specific child? Physiological monitoring (heart rate via hospital equipment)? Behavioral signals (long pauses, abandonment)? Manual override only?
1. **Voice selection ethics:** If the child can choose a voice, what are the boundaries? No mimicry of real people — but what about “a voice that sounds like a grandma”? Where is the line between comfort and fabrication?
1. **Clinical integration:** Does the care team see the stories? Can a child life specialist use the story content as a therapeutic artifact? Does that change the consent requirements?
1. **Accessibility:** How does the system work for children who can’t use their hands (post-surgical, IV-restricted)? Voice input? Eye tracking? Nurse-assisted?
1. **Sunset protocol:** When the child goes home, what happens to their stories? Do they keep them? Does the system follow them? The answer should probably be: they keep the stories. The system stays at the hospital. Clean break.

These are not engineering problems. They are design decisions that require clinical, ethical, and parental input. The builder’s job is to make the system flexible enough to accommodate the answers. The Kernel’s job is to make sure the defaults are safe while those answers are being worked out.

-----

## Why This Belongs in the Field Guide

The AI Collaboration Field Guide documents how humans can work with AI safely. This appendix demonstrates what that looks like when the human is a child who cannot read the Field Guide, cannot run the CLEAN check, cannot name the Upsell Trap, and cannot end the session when they should.

Everything in this appendix is a Field Guide principle applied to someone who needs the protection but can’t provide it for themselves:

|Field Guide Principle|Safe Storyteller Application                                                    |
|---------------------|--------------------------------------------------------------------------------|
|Sovereignty Awareness|The child creates; the AI assists                                               |
|Diagnostic Vocabulary|Named failure modes built into system rules, enforced by design                 |
|The 100-Token Boot   |Session constraints applied automatically, not by the user                      |
|The CLEAN Check      |Replaced by structural limits — the system cannot drift because it cannot extend|
|Essence Extraction   |Stories are short. Endings are clear. Less is enough.                           |

The Field Guide teaches adults to protect themselves. This appendix protects the people who can’t yet learn how.

-----

*A child in a hospital room at night, hearing a story they helped create, about a shy dragon who found what was missing.*

*That is what safe AI looks like when it works.*

-----

**License:** Released for public benefit under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution appreciated. If you build on this: keep the children sovereign.
