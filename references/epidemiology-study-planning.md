# Epidemiology Study Planning

## Contents

1. Purpose
2. Reconstruct the study model
3. Think in estimands
4. Build the analysis inventory
5. Classify analysis roles
6. Prioritize results
7. Interpret sensitivity and bias-probe analyses
8. Handle effect modification and subgroup findings
9. Handle participant characteristics
10. Handle null and discordant evidence
11. Handle high-dimensional results
12. Compress analyses into scientific claims
13. Plan Methods and Discussion
14. Plan model and adjustment detail for slides
15. Epidemiology audit
16. Short examples

## 1. Purpose

Use this guide for cohort, case-control, cross-sectional, registry, pharmacoepidemiology, survival, longitudinal, causal-inference, and related population-based clinical research.

The goal is not to teach an epidemiology textbook. The goal is to understand enough of the study to select and sequence evidence correctly for a presentation.

## 2. Reconstruct the study model

Before selecting results, identify as many of these as the source supports:

- research question;
- target population and actual study population;
- study design;
- exposure or intervention;
- comparator or reference group;
- outcome;
- time zero or index date;
- exposure assessment window;
- follow-up window;
- sampling, matching, or eligibility structure;
- effect measure;
- primary analysis;
- adjustment/confounding strategy;
- time-varying structure when relevant;
- primary and secondary estimands;
- major limitations explicitly discussed by the source.

If a field is unclear, mark it as unclear rather than guessing.

## 3. Think in estimands

Ask: what contrast is this study trying to estimate, in whom, over what time period, and on what scale?

Distinguish carefully among incidence, prevalence, risk, odds, rate, hazard, mean difference, longitudinal change, prediction, mediation, and interaction.

Do not equate:

- odds ratio with risk ratio;
- hazard ratio with absolute risk;
- association with causation;
- two subgroup p-values with an interaction;
- a within-person estimate with a between-person estimate;
- an exploratory analysis with a prespecified primary estimand.

If the paper contains several estimands, identify which one best answers the main research question and which are extensions.

## 4. Build the analysis inventory

Inventory the full result set before planning slides. For each analysis, capture only fields that are useful:

- question answered;
- population/subpopulation;
- exposure and comparator;
- outcome;
- time window;
- model;
- effect measure and uncertainty;
- whether prespecified or exploratory when known;
- scientific role;
- relationship to the primary result.

Typical result families include:

- baseline or participant characteristics;
- crude incidence/rates;
- primary adjusted model;
- alternate outcome or exposure definitions;
- secondary outcomes;
- subgroup analyses;
- interaction/effect modification;
- dose-response;
- lag/time-window analyses;
- mediation;
- negative controls;
- competing-risk or missing-data analyses;
- sensitivity/robustness analyses;
- biomarker or high-dimensional screens;
- exploratory extensions.

## 5. Classify analysis roles

Use a role such as:

- `primary`
- `key_secondary`
- `effect_modification`
- `temporal_pattern`
- `dose_response`
- `mediation`
- `robustness`
- `sensitivity`
- `bias_probe`
- `negative_control`
- `descriptive`
- `exploratory`

Do not assume every analysis has equal presentation value.

## 6. Prioritize results

Use qualitative tiers rather than a false-precision score.

### Tier 1 — Core evidence

Directly answers the primary question or primary estimand. Normally include in the main deck.

### Tier 2 — Interpretation-critical evidence

Not necessarily the primary analysis, but needed to trust, qualify, or correctly interpret Tier 1. Examples include a long-lag analysis that materially addresses reverse causality, a sibling comparison that changes the confounding argument, or an analysis controlling a time-varying process central to interpretation.

Usually include in the main deck.

### Tier 3 — Supporting scientific evidence

Adds meaningful context, heterogeneity, clinical relevance, or secondary insight but is not essential to the main conclusion. Include if time and audience make it worthwhile.

### Tier 4 — Routine robustness / technical support

Confirms the result without materially changing its interpretation. Usually backup.

Upgrade to Tier 2 if it resolves a major inferential concern.

### Tier 5 — Exploratory / peripheral

Interesting but weakly connected to the main question, highly multiplicity-prone, or too detailed for the talk. Usually backup or omit.

When in doubt, ask whether removing the analysis would change what a careful epidemiologist believes the study shows. If not, it probably does not need main-deck space.

## 7. Interpret sensitivity and bias-probe analyses

Do not use the label "sensitivity analysis" as a reason to hide an analysis.

Separate:

- routine robustness: alternate model or specification with essentially unchanged inference;
- interpretation-critical robustness: directly tests a major alternative explanation.

For observational research, identify only the inferential threats that are genuinely relevant to the design or explicitly discussed by the source. Examples can include confounding, reverse causality, selection bias, surveillance bias, misclassification, immortal time bias, informative censoring, and time-varying confounding.

If the source explicitly identifies a concern, preserve its framing. If the planner infers a concern from the design, label it as planning inference rather than author conclusion.

A useful presentation chain is:

`Main association -> plausible alternative explanation -> analysis/design feature addressing it -> refined interpretation`

## 8. Handle effect modification and subgroup findings

Do not infer effect modification because one subgroup is significant and another is not.

Prefer the interaction estimate/test when the scientific question is whether effects differ between groups.

Promote subgroup/effect-modification evidence when it is:

- prespecified or scientifically central;
- supported by an interaction analysis or otherwise appropriate comparison;
- clinically meaningful;
- important to the final interpretation.

Demote long lists of underpowered or exploratory subgroup findings.

## 9. Handle participant characteristics

Do not automatically place Table 1 in the main deck.

Include participant characteristics when they matter for:

- generalizability;
- matching or comparability;
- obvious imbalance;
- selection;
- key clinical composition;
- interpretation of exposure/outcome;
- explaining follow-up or analytic population.

Otherwise summarize orally, simplify heavily, move to backup, or omit.

## 10. Handle null and discordant evidence

A null result can be essential when it answers an explicit research question or materially narrows the conclusion.

Do not hide conflicting results across cohorts, control groups, models, or outcome definitions. Determine whether the discordance affects robustness, precision, generalizability, or causal interpretation.

Possible presentation relationships include:

- convergence;
- triangulation;
- robustness;
- discordance;
- sensitivity;
- replication;
- extension;
- unresolved discrepancy.

Discordance can itself be a scientific takeaway.

## 11. Handle high-dimensional results

For biomarkers, pathogens, omics, genetics, many exposures, many outcomes, or large subgroup matrices, do not create one slide per variable.

First identify the scientific hierarchy, for example:

`Global signal -> main drivers -> phenotype -> prognosis`

or:

`Overall association -> heterogeneity -> most informative subgroup -> robustness`

Use overview/focus sequences when a dense figure is important but cannot be read in one step.

## 12. Compress analyses into scientific claims

Before allocating slides, reduce the result inventory to a small number of scientific claims.

For each claim, identify:

- the claim itself;
- primary supporting analysis;
- important secondary support;
- qualifiers or contradictory evidence;
- appropriate claim strength;
- presentation priority.

Prefer:

`15 analyses -> 3-5 scientific claims -> slides`

rather than:

`15 analyses -> 15 result slides`.

Use claim-strength labels when useful:

- descriptive;
- association;
- prediction;
- causal interpretation;
- mechanism;
- hypothesis;
- speculation.

Do not strengthen an observational association into causation. Do not convert a hypothesis into an established mechanism.

## 13. Plan Methods and Discussion

### Methods

Explain what the audience needs to understand and trust the results:

- design;
- population;
- exposure/comparator;
- outcome;
- timeline/time zero/follow-up;
- major confounding strategy;
- statistical method only to the depth needed for interpretation;
- reproducibility-critical model choices when they define the contrast, control a major bias, or explain why estimates differ.

Use: `method depth ∝ inferential burden`, not `method depth ∝ manuscript length`.

When model detail matters, use the audience-facing rules in `model-detail-for-slides.md`: describe the estimator and adjustment mechanism in scientific language, avoid raw implementation syntax, and distinguish direct outcome-model covariate adjustment from weighting/matching/standardization models.

### Discussion

Do more than restate results. Build:

`What did we learn? -> How does it compare with prior evidence? -> What is the most plausible interpretation? -> What limitation most affects that interpretation? -> What does it imply?`

Separate the study's own result, external literature, and mechanistic speculation.

## 14. Plan model and adjustment detail for slides

For each primary or interpretation-critical quantitative result, determine whether the audience needs a compact model note to understand what produced the estimate.

At minimum, know:

- the estimator/model family;
- how confounding or selection was handled;
- which covariates or covariate domains entered that adjustment mechanism;
- whether clustering, fixed effects, random effects, recurrent-event structure, time-varying exposure, lagging, or weighting changes interpretation.

Do not convert code syntax into slide text. Prefer descriptions such as `stabilized-IPCW weighted marginal survival estimates` or `within-individual fixed-effects Cox model, adjusted for prespecified time-varying covariates`.

If the covariate set is long, show domains on the main slide and route the complete variable list, windows, coding, and functional forms to backup. If a specific choice is central to the argument, name it explicitly even when other covariates are summarized by domain.

If covariates are used to construct weights or propensity scores rather than entered directly into the outcome regression, do not write a misleading generic `adjusted for` line. State the adjustment path accurately.

## 15. Epidemiology audit

Before finalizing the plan, check:

- Is the primary research question correct?
- Are population, exposure, comparator, outcome, and time structure correct?
- Is the primary estimand understood?
- Are effect measures interpreted correctly?
- Is the main result truly the main result rather than the smallest p-value?
- Is interpretation-critical robustness retained?
- Are exploratory findings overrepresented?
- Are interaction/subgroup claims valid?
- Are null findings retained when they close a question?
- Is discordant evidence represented fairly?
- Are observational claims appropriately cautious?
- Can every main result be traced back to the source?

## 16. Short examples

### Example A — Many subgroup rows

Input: one primary treatment comparison plus dozens of age/sex/comorbidity-specific incidence rows.

Plan: show the primary comparison; show subgroup evidence only if it materially changes interpretation or tests meaningful effect modification; do not reproduce every row.

### Example B — Reverse causality

Input: primary exposure-outcome association plus lag analyses.

If the lag analysis merely repeats the same result, it may be backup. If reverse causality is a central threat and a long-lag result materially informs that concern, promote it to interpretation-critical evidence.

### Example C — High-dimensional screen

Input: many exposure-outcome associations.

Plan the result as global signal -> strongest credible drivers -> relevant phenotype/prognosis extension. Avoid a variable-by-variable slide sequence.
