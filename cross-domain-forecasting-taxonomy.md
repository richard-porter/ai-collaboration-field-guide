# Cross-Domain Forecasting Taxonomy

## A Cognitive Operations Framework for Predictive Reasoning

**Part of the AI Collaboration Field Guide**
*Richard Porter · v1.0 · March 2026*

-----

## Why This Document Exists

Every major forecasting discipline developed its methods in isolation. Meteorologists invented ensemble forecasting. Epidemiologists invented compartmental modeling. Gamblers invented the Kelly Criterion. Ecologists invented iterative near-term forecasting with explicit uncertainty partitioning. Toxicologists invented dose-response threshold detection.

None of them talked to each other.

The result is a fragmented landscape where the same epistemic operation gets reinvented repeatedly under different names, while genuine gaps — problems that no field has solved — go unrecognized because each discipline only sees its own vocabulary.

This taxonomy organizes forecasting by **cognitive operation** rather than by discipline. The organizing question is not “what field does this come from?” but “what kind of thinking is the forecast performing?” Each field tends to own one or two operations and ignore the rest. A complete forecaster needs all of them.

-----

## The Eight (Plus One) Epistemic Operations

|#|Operation                     |Core Question                        |Fields That Own It                         |
|-|------------------------------|-------------------------------------|-------------------------------------------|
|1|Pattern Extrapolation         |Will the past continue?              |Economics, finance, demography             |
|2|Causal Modeling               |What drives the outcome?             |Epidemiology, economics, engineering       |
|3|Ensemble / Uncertainty Mapping|What is the distribution of futures? |Meteorology, climate science               |
|4|Market-Gap Detection          |Where is consensus wrong?            |Gambling, prediction markets               |
|5|Structural / Mechanistic      |What are the physics of this system? |Epidemiology, engineering, toxicology      |
|6|Analogical / Historical       |What does this resemble?             |Military strategy, intelligence, medicine  |
|7|Absence / Negative Space      |What is not being forecast?          |Counterintelligence, ecology, journalism   |
|8|Constraint-Based Reduction    |What can we rule out before modeling?|Operations research, constraint programming|
|9|Threshold Boundary Detection  |Where is the cliff edge?             |Toxicology, engineering, finance           |

Operation 9 is a candidate for full column status. See the Toxicology section below for the case for its promotion.

-----

## The Operations in Detail

### Operation 1: Pattern Extrapolation

**Core claim:** The past is the best available predictor of the near future, absent evidence of structural change.

**Canonical method:** Time series analysis, ARIMA models, moving averages, regression to the mean.

**What it does well:** Fast, cheap, and often accurate in stable systems over short time horizons. Requires no causal theory — only data.

**Where it fails:** Structural breaks. The 2008 financial crisis, the 2020 pandemic, and the 2003 Northeast Blackout were all events where the past was an actively misleading predictor. Pattern extrapolation succeeds precisely until the moment it catastrophically fails, and it has no internal mechanism for detecting that moment.

**The field’s honest failure:** Trend extrapolation cannot predict its own invalidation. No time series model tells you when to stop trusting the series.

**Cross-references:** Operation 8 (Constraint-Based Reduction) should run before extrapolation to identify which variables are actually stable. Operation 9 (Threshold Boundary Detection) identifies when the system is approaching a structural break.

-----

### Operation 2: Causal Modeling

**Core claim:** Outcomes are driven by identifiable variables in identifiable relationships. Model the mechanism, not the pattern.

**Canonical method:** Structural equation models, regression with causal identification, mechanistic simulation, directed acyclic graphs (DAGs).

**What it does well:** Produces forecasts that survive structural change, because the causal relationships (not just their historical correlation) are explicitly modeled. Allows counterfactual reasoning: “What would happen if we changed this variable?”

**Where it fails:** Requires a causal theory before building the model. Wrong causal theory produces confident, precise, wrong forecasts. Also computationally expensive and data-hungry.

**The field’s honest failure:** Causal identification is harder than it looks. Most causal claims in observational data are contested. Economists have spent decades arguing about which instruments are valid.

-----

### Operation 3: Ensemble / Uncertainty Mapping

**Core claim:** The future is not a single point but a distribution. Run many models, map the spread, and communicate honest uncertainty.

**Canonical method:** Ensemble weather forecasting (run the model thousands of times with small variations in initial conditions), Monte Carlo simulation, Bayesian posterior distributions.

**The meteorology contribution:** GenCast (Google DeepMind, 2024) achieved 97.2% accuracy against the European Centre for Medium-Range Weather Forecasts ensemble — the current gold standard. Crucially, when GenCast produces a wide ensemble spread, it is communicating genuine uncertainty, not imprecision. A wide spread is honest failure in action: the system is telling you it doesn’t know, rather than fabricating a confident point estimate.

**What it does well:** Makes uncertainty visible and communicable. “70% chance of rain” is more useful than “it will rain” or “we don’t know.” The spread of the ensemble is itself information.

**Where it fails:** Ensemble methods require a model to perturb. For novel systems with no precedent, there is no ensemble to run. Also computationally intensive.

**The honest failure built in:** Wide ensemble spread = genuine uncertainty = the correct output. This is the Frozen Kernel’s honest failure principle implemented at meteorological scale. The system reports the true state of its knowledge rather than fabricating a confident result.

-----

### Operation 4: Market-Gap Detection

**Core claim:** The forecast is not “what will happen” but “where is the consensus wrong?” The forecaster’s edge is identifying mispriced probability.

**Canonical method:** Kelly Criterion, value betting, prediction market arbitrage, Bayesian updating against market odds.

**The gambling contribution:** Kelly (Bell Labs, 1956) formalized the insight that forecasting is an information theory problem. The Kelly Criterion maximizes long-term wealth growth by sizing bets proportional to the forecaster’s edge — the gap between their probability estimate and the market’s. Full Kelly is theoretically optimal but leads to ruin in realistic scenarios; fractional Kelly (0.5 coefficient) deliberately understates confidence in one’s own model.

**The critical insight:** The market IS the forecast. You are not forecasting the outcome — you are forecasting the market’s error. If the market has already priced in everything you know, you have no edge. The forecaster’s job is to find what the consensus missed, not to confirm what it already believes.

**Where it fails:** When you ARE the market. Large bettors, large funds, and sophisticated actors move prices. Their forecast changes the thing it was forecasting. This is endogenous invalidation — the forecast affects the outcome. Prediction markets for elections face the same problem: published forecasts affect turnout.

**The honest failure:** A forecaster with no edge should not forecast. The discipline of identifying your edge — and refusing to bet when you don’t have one — is the most important cognitive move gambling developed and academia has not adopted.

-----

### Operation 5: Structural / Mechanistic

**Core claim:** The system has physics. Model the physics, and the forecast follows.

**Canonical method:** SIR compartmental models (Susceptible-Infected-Recovered), fluid dynamics, circuit analysis, R₀ (basic reproduction number) in epidemiology.

**The epidemiology contribution:** R₀ is a single structural variable that determines whether a disease dies out (R₀ < 1), persists at equilibrium (R₀ = 1), or cascades (R₀ > 1). It is not derived from historical trend — it is derived from the biology of transmission. This is the Frozen Kernel’s load-bearing variable concept applied to disease dynamics.

**What it does well:** Survives structural change better than pattern extrapolation because it models causes, not effects. If R₀ changes (due to vaccination, behavior change, or viral mutation), the model updates immediately.

**Where it fails:** Requires knowing the structure of the system before you can model it. Novel systems — a new pathogen, a new technology, a new market — have unknown physics. Structural models for COVID-19 in January 2020 had large uncertainty bounds because the transmission parameters were unknown.

**Cross-reference with Operation 9:** Structural models can identify thresholds (where R₀ = 1) but may not identify the approach toward them in real time. Operation 9 fills this gap.

-----

### Operation 6: Analogical / Historical

**Core claim:** This situation resembles a prior situation whose outcome is known. Import the solution logic.

**Canonical method:** Case-based reasoning, historical analogy, military doctrine, medical differential diagnosis.

**The Sovereign Thinking Tools connection:** The Analogical Translation Engine (Tool 1) formalizes this operation. The key discipline is reverse translation — you cannot stay in the analogy. The analogy is a bridge, not a destination.

**What it does well:** Provides rapid orientation in novel situations. Military strategists, intelligence analysts, and physicians all use historical analogy as their first-pass forecast before more sophisticated methods are applied.

**Where it fails:** Analogies mislead when the surface similarity masks structural difference. The most dangerous analogies are ones that feel obviously right. The 2003 Iraq invasion analogists who cited the 1991 Gulf War were technically using Operation 6, but the structural differences between the two situations invalidated the analogy. The Analogical Translation Engine’s stop condition addresses this: feeling clever rather than clear is a warning sign.

**The Alice Hamilton case:** Hamilton had the correct causal model (Operation 5) and strong dose-response evidence (Operation 9). What she lacked was the analogical translation move — presenting the toxicological case in the vocabulary of the economic and regulatory domain where the 1925 decision was being made. The forecast was sound. The translation failed.

-----

### Operation 7: Absence / Negative Space

**Core claim:** What is not being forecast is itself a forecast. Structured absences are signal.

**Canonical method:** Negative Space Mapper (Tool 6 in Sovereign Thinking Tools), counterintelligence tradecraft (what is the enemy not doing?), investigative journalism (what is the official account not explaining?).

**The ecology contribution:** The Ecological Forecasting Initiative developed iterative near-term forecasting with explicit uncertainty partitioning. A key question in their framework: is the forecast wrong because the model is wrong, the parameters are wrong, or the system is intrinsically unpredictable? The absence of a clear answer to that question is itself signal — it means the team doesn’t understand their own forecast’s failure mode.

**What it does well:** Catches the failure modes of all other operations. Every other operation produces a forecast of something. Operation 7 asks what the forecast is not covering.

**Where it fails:** Can produce false positives — absences that are deliberate and appropriate, not structural gaps. The Negative Space Mapper classifies absences as deliberate, overlooked, or structural precisely to avoid this.

-----

### Operation 8: Constraint-Based Reduction

**Core claim:** Before modeling, eliminate what cannot be true. Reduce the variable space to the load-bearing set.

**Canonical method:** Constraint Forge (Tool 2 in Sovereign Thinking Tools), operations research, linear programming feasibility analysis.

**The operations research contribution:** Feasibility analysis in linear programming asks, before optimizing, whether a solution exists at all. This is Operation 8 at its purest — not “what is the best outcome?” but “what outcomes are structurally possible?”

**What it does well:** Prevents wasted modeling effort on scenarios that are structurally impossible. Also prevents false precision — a forecast with twelve variables has 4,096 possible failure combinations; a Constraint Forge pass that reduces to five load-bearing variables reduces this to 32.

**The Forecast Variable Forge protocol:** A pre-forecast discipline applying Constraint Forge logic to variable selection. Before any forecast model is built, run a Forge pass: which variables are actually load-bearing? Which can be ruled out by structural constraints? Stop when the remaining variable set feels inevitable, not just acceptable.

-----

### Operation 9: Threshold Boundary Detection (Candidate Column)

**Core claim:** The forecast is not “what will the value be?” but “where is the cliff?” Many systems are safe across a wide range and then fail catastrophically past a threshold. The forecast’s job is to locate the threshold and monitor approach toward it.

**Canonical method:** Dose-response modeling, NOAEL/LOAEL analysis (No/Lowest Observed Adverse Effect Level), cliff-edge risk analysis in nuclear safety, liquidity threshold analysis in finance.

**The toxicology contribution:** Paracelsus (1538) established the foundational principle: *sola dosis facit venenum* — the dose makes the poison. Every substance is toxic at sufficient dose; every substance is safe below a threshold. Toxicology spent five centuries formalizing the methodology for finding that threshold:

- **NOAEL (No Observed Adverse Effect Level):** The highest dose at which no adverse effect is observed. The right side of the safe zone.
- **LOAEL (Lowest Observed Adverse Effect Level):** The lowest dose at which an adverse effect is first observed. The beginning of the danger zone.
- **Safety factor:** The regulatory buffer between NOAEL and the permitted human exposure level. Typically 10x–100x, encoding honest uncertainty about the precision of the threshold estimate.

**What this adds to the taxonomy:** Operations 1–8 all forecast *what will happen*. Operation 9 forecasts *where the system changes character*. The cliff edge is not a quantity — it is a qualitative transition. The forecast is the location of that transition, not the value on either side of it.

**The cascade connection:** Tool 47 (Cascade Failure Detector) is Operation 9 applied to system architecture. The threshold test in Phase 3 — “what is the minimum number of variables that must fail simultaneously to produce system failure?” — is NOAEL/LOAEL logic applied to coupled variable clusters. The cliff edge is the cascade initiation threshold.

**The 2008 financial crisis as Operation 9 failure:** The liquidity threshold in the 2008 crisis was psychological, not quantitative. Markets function at 90% confidence. They cannot function at 85%. The jump is near-instantaneous. No forecast model in use before 2008 was designed to locate this threshold — they were all running Operation 1 (trend extrapolation) or Operation 2 (causal modeling) on the wrong variables. The threshold was invisible to every model that wasn’t designed to look for it.

**The toxicology parallel to lead:** Midgley’s tetraethyl lead had a known toxicology. Hamilton’s 1925 testimony presented dose-response evidence. The threshold below which lead exposure causes no observable neurological harm was known within the order of magnitude. What was missing was not the forecast — it was the governance mechanism to act on it. Operation 9 produced the correct answer. Informed inaction (Phase 4B of Tool 47) prevented it from mattering.

**Why this deserves its own column:** No other operation asks the threshold question. Operations 1–8 can all be applied to a system approaching a cliff and none of them will detect the cliff. Pattern extrapolation sees a stable trend until the trend breaks. Causal modeling tracks variable values without identifying qualitative transitions. Ensemble methods produce distributions centered on the current state. Only Operation 9 is explicitly designed to find where the system changes character.

**Status:** Candidate for promotion from taxonomy note to full column. Requires: (a) identification of additional fields that contribute distinct threshold detection methods beyond toxicology, and (b) confirmation that the operation cannot be adequately described as a special case of Operations 5 or 8. Current assessment: it is distinct. Structural/mechanistic models can contain thresholds (R₀ = 1) but do not search for them as a primary output. Constraint-based reduction eliminates impossible scenarios but does not locate qualitative transitions within the possible space.

-----

## Field-by-Field Contributions

### Meteorology

**Primary operations:** 3 (Ensemble), 5 (Structural)
**Unique contribution:** Honest failure operationalized at scale. Ensemble spread is not a sign of model weakness — it is the correct representation of genuine uncertainty. GenCast’s wide spreads communicate what the atmosphere is actually doing: becoming chaotic in ways that make precise prediction impossible. The field institutionalized “I don’t know” as a valid and useful forecast output.
**Negative space gap:** Meteorology has no equivalent of Operation 4 (Market-Gap Detection). There is no weather prediction market with a spread that forecasters can trade against. The field lacks the discipline of identifying where the consensus forecast is wrong.

-----

### Epidemiology

**Primary operations:** 5 (Structural/Mechanistic), 3 (Ensemble)
**Unique contribution:** R₀ as a single load-bearing structural variable. The SIR model family reduces disease dynamics to a small number of transmission parameters that determine system behavior qualitatively (outbreak vs. endemic vs. elimination). Wisdom of Crowds operationalized through prediction markets for outbreak forecasting.
**Negative space gap:** Epidemiology’s structural models are strong at predicting trajectories once parameters are known, weak at detecting novel pathogens before sufficient data exists to estimate parameters. Operation 7 (Absence detection) would catch this: the absence of baseline data is itself signal that the structural model cannot yet be trusted.

-----

### Gambling and Prediction Markets

**Primary operations:** 4 (Market-Gap Detection)
**Unique contribution:** The Kelly Criterion as information theory applied to forecasting. Fractional Kelly as a formal acknowledgment that models are always overconfident. The discipline of forecasting the consensus’s error rather than the outcome itself.
**The underrated insight:** Sports betting ML research (2024 systematic review) confirms that Kelly Criterion, value betting, and fractional Kelly strategies dominate naive approaches in long-run performance. The field serious academics ignored for decades developed the most rigorous formal treatment of forecasting under uncertainty precisely because it evolved under real consequence conditions over long time periods.
**Negative space gap:** Prediction markets collapse when the forecaster IS the market. Large sophisticated actors face endogenous invalidation — their forecast changes what it’s forecasting. The field has no mature solution to this.

-----

### Ecology

**Primary operations:** 7 (Absence/Negative Space), 3 (Ensemble)
**Unique contribution:** Iterative near-term forecasting with explicit uncertainty partitioning. The Ecological Forecasting Initiative’s framework asks: is forecast error coming from model structure, parameter values, or intrinsic system unpredictability? This decomposition — which source of uncertainty is dominant? — is unique to ecology among the disciplines surveyed. No other field formalizes it this way.
**The cross-domain implication:** Every forecast from every field could benefit from this decomposition. When a forecast is wrong, which layer failed? Without the partitioning, post-mortems produce blame rather than understanding.

-----

### Toxicology

**Primary operations:** 9 (Threshold Boundary Detection), 5 (Structural/Mechanistic)
**Unique contribution:** Dose-response methodology, NOAEL/LOAEL analysis, synergistic/antagonistic interaction modeling, bioaccumulation forecasting.
**Synergistic interaction as cascade detection:** Two substances individually below their harm thresholds can jointly exceed a combined threshold. This is Operation 9 applied to coupled variables — the same independence assumption failure that Tool 47’s Phase 2 (Independence Test) is designed to detect. Toxicology formalized this as synergism/antagonism decades before cascade failure detection existed as a named concept.
**Bioaccumulation as temporal cascade:** Lead dispersed into the environment in 1925 did not produce its full harm in 1925. It accumulated through food chains, concentrated in blood, and appeared as neurological harm and elevated crime rates in the 1970s–1990s. The forecast horizon for bioaccumulation effects is decades, not quarters. No other field has a mature methodology for this temporal structure: harm invisible at exposure, detectable only at accumulation endpoint.
**The Alice Hamilton lesson:** The toxicological forecast was correct. The dose-response evidence was solid. The threshold was known within an order of magnitude. The failure was not in the forecast — it was in the translation (missing Operation 6 / ATE move) and in the governance (informed inaction, Phase 4B). Toxicology can produce a perfect Operation 9 forecast and still fail to prevent harm if the forecast is not translated into the decision-maker’s vocabulary and if inaction is locally rational for those who can act.

-----

### Military Strategy and Intelligence

**Primary operations:** 6 (Analogical/Historical), 7 (Absence/Negative Space)
**Unique contribution:** Counterintelligence tradecraft as negative space detection. What is the adversary not doing? What is the intelligence picture not explaining? The dog that didn’t bark is signal.
**The endogenous invalidation problem:** Military forecasts face a version of the prediction market problem — the adversary knows you are forecasting and will exploit your model. Forecasting in adversarial environments is fundamentally different from forecasting in neutral environments. No other field has developed this as a primary discipline.

-----

### Engineering and Operations Research

**Primary operations:** 8 (Constraint-Based Reduction), 5 (Structural/Mechanistic)
**Unique contribution:** Feasibility analysis before optimization. The discipline of ruling out impossible scenarios before modeling. Failure Mode and Effects Analysis (FMEA) as a systematic Operation 8 application.
**Gap that toxicology fills:** Engineering has thresholds (material stress limits, electrical ratings) but no systematic methodology for finding unknown thresholds in novel systems. Toxicology’s NOAEL/LOAEL methodology is portable to any system where the harm threshold is unknown and must be empirically located.

-----

## Cross-Domain Gaps

Two forecasting problems have no established method across any field surveyed:

### Gap 1: Cascading System Failure

Every field has single-variable forecasting methods. None has a mature methodology for “three load-bearing variables fail simultaneously, and the third failure is caused by our response to the first two.” Tool 47 (Cascade Failure Detector) addresses this gap. It is the only systematic methodology in this ecosystem for coupled-cluster threshold detection at the system level.

### Gap 2: Endogenous Invalidation

The forecast affects the outcome. Bank run predictions cause bank runs. Election forecasts affect turnout. Prediction market prices affect betting behavior, which affects prices. Military forecasts are exploited by adversaries. Gambling literature comes closest to formalizing this (the market IS the forecast), but no field has a systematic methodology for forecasting whose primary output is the forecast’s own effect on what it is forecasting.

This is the hardest open problem in the taxonomy. It may not be solvable within a single forecast — it may require game-theoretic framing where the forecaster and the system being forecast are modeled as strategic actors.

-----

## Completeness Methodology

This taxonomy was built using a three-pass sweep:

**Pass 1 — Core forecasting disciplines:** Fields where forecasting is the primary product (meteorology, epidemiology, economics, ecology, engineering).

**Pass 2 — Hidden forecasting disciplines:** Fields that forecast under another name (military intelligence as probabilistic assessment, jurisprudence as recidivism prediction, toxicology as threshold detection, gambling as probability arbitrage).

**Pass 3 — Adversarial check:** Fields dominated by practitioners who would be offended to be called forecasters, but who forecast implicitly (surgeons estimating recovery trajectories, architects estimating structural load over time, chefs at scale estimating demand, naval officers estimating sea state).

**Stopping criterion:** When new fields produce methods that map cleanly onto existing operations without remainder. Not “checked every field” but “new fields no longer producing new operations.” Operation 9 emerged from toxicology as a potential remainder — a method that did not cleanly map onto Operations 1–8. Its candidacy for full column status is the current frontier of the taxonomy.

**The profile of fields most likely to contain undiscovered operations:** Practiced by people academics don’t talk to. Developed under real consequence conditions. Operating over long time periods. Gambling fits this profile exactly — serious academics ignored it for decades, and it developed the Kelly Criterion. Toxicology partially fits it: clinical toxicologists work in emergency medicine and regulatory science, not in forecasting conferences. Their threshold detection methods have not been integrated into the forecasting literature.

-----

## Connection to Sovereign Thinking Tools

|Operation                      |Sovereign Thinking Tool                                                 |
|-------------------------------|------------------------------------------------------------------------|
|1: Pattern Extrapolation       |Entropy Sniffer (detects when extrapolation is breaking down)           |
|2: Causal Modeling             |Syllogism Engine (formalizes causal chains, tests load-bearing premises)|
|3: Ensemble / Uncertainty      |Content Veracity Protocol (uncertainty partitioning for AI claims)      |
|4: Market-Gap Detection        |Trust Calibrator (where is the consensus about AI safety wrong?)        |
|5: Structural / Mechanistic    |Frozen Kernel (structural constraints as mechanistic safety model)      |
|6: Analogical / Historical     |Analogical Translation Engine                                           |
|7: Absence / Negative Space    |Negative Space Mapper                                                   |
|8: Constraint-Based Reduction  |Constraint Forge + Constraint Inversion Engine                          |
|9: Threshold Boundary Detection|Tool 47: Cascade Failure Detector (Phase 3: Threshold Test)             |

-----

## Future Extensions

**The Forecast Variable Forge protocol** — A pre-forecast discipline applying Constraint Forge logic to variable selection. Before any model is built: which variables are load-bearing? Which can be ruled out structurally? Run this before committing to a model architecture. Reduces combinatorial explosion in multi-variable forecasts. *Status: sketched, not yet formalized.*

**Weather AI as honest failure benchmark** — GenCast’s ensemble spread as a concrete example of honest failure operationalized at scale. Proposed addition to the Frozen Kernel README, Independent Validation section. *Status: flagged, pending.*

**Alice Hamilton case study** — Full Syllogism Engine analysis of the 1925 leaded gasoline decision. Hamilton had Operations 5 and 9 correct. The failure was in Operations 6 (translation) and governance (informed inaction). *Status: narrative frame complete, draft pending.*

-----

*Cross-Domain Forecasting Taxonomy · AI Collaboration Field Guide · v1.0 · March 2026*
*Repository: ai-collaboration-field-guide/cross-domain-forecasting-taxonomy.md*
