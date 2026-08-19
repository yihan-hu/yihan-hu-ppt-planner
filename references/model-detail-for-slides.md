# Model Detail for Scientific Slides

## Contents

1. Purpose
2. Decide whether model detail belongs in the main deck
3. Use audience-facing model language
4. Describe adjustment accurately
5. Choose which covariates to show
6. Reproducibility-critical choices
7. Result-slide model notes
8. Main deck versus backup
9. Short wording patterns
10. Audit

## 1. Purpose

Use this guide when a scientific presentation includes adjusted effect estimates, weighting or matching, multilevel or repeated-measures models, survival models, fixed-effects analyses, time-varying exposures, recurrent events, or other analytic choices that materially affect how the audience should interpret the result.

The goal is not to reproduce statistical code on slides. The goal is to show enough of the analytic specification that a scientifically literate audience can understand what the estimate represents, how confounding or dependence was handled, and which choices are central to reproducibility.

## 2. Decide whether model detail belongs in the main deck

Promote model detail to the main deck when it is needed to understand or trust the result, especially when:

- the analytic design is a major contribution of the study;
- different models or estimands explain apparently conflicting results;
- weighting, matching, standardization, fixed effects, random effects, clustering, or time-varying treatment states materially change interpretation;
- prespecified choices are important to show that the analysis was not tuned to the observed result;
- a non-obvious model feature addresses a major bias concern;
- the audience is methodological, epidemiologic, statistical, or likely to ask how the estimate was obtained.

Do not add model detail merely because it exists in the protocol. If removing the detail would not change how the audience interprets or trusts the estimate, move it to backup.

## 3. Use audience-facing model language

Prefer a short scientific description over implementation syntax.

Do not put raw code such as `Surv(start, stop, outcome) ~ strategy`, internal variable names, package calls, or long formulas on the main slide unless the formula itself is the scientific point or the user explicitly wants a technical derivation.

Prefer descriptions such as:

- `Estimates from stabilized-IPCW weighted marginal survival models`
- `Adjusted Cox proportional hazards model`
- `Within-individual fixed-effects Cox model with recurrent-event gap time`
- `Linear mixed-effects model with participant-level random intercepts`
- `Propensity-score matched analysis with robust standard errors`

Keep the main statement short enough to function as a subtitle, caption, or small result-slide footnote.

## 4. Describe adjustment accurately

Do not collapse different adjustment mechanisms into the generic phrase `adjusted for` when that wording would misrepresent the model.

### Direct covariate adjustment

If covariates enter the outcome regression directly, wording such as the following is appropriate:

`Adjusted Cox model; covariates included age, sex, BMI, disease severity, and treatment history.`

### Weighting or standardization

If covariates are used to estimate weights, treatment probabilities, censoring probabilities, or standardization models rather than entered directly in the outcome model, say so explicitly:

`Estimates from stabilized-IPCW weighted marginal survival models. The IPCW model included prespecified demographic, clinical, treatment-history, and healthcare-utilization covariates.`

Avoid wording that makes it sound as though all listed covariates were additional terms in the final outcome model.

### Matching

Use language such as:

`Propensity-score matched comparison; the propensity model included ...`

### Within-person or fixed-effects models

Use language such as:

`Within-individual fixed-effects model, adjusted for prespecified time-varying treatment and medication covariates.`

### Multilevel or repeated-measures models

State the structural feature that changes interpretation, for example:

`Mixed-effects model with participant-level random intercepts; adjusted for ...`

Do not over-explain routine variance estimators unless clustering or repeated contribution is inferentially important.

## 5. Choose which covariates to show

On the main deck, show covariates at the level that best balances transparency and readability.

Use named covariates when the set is short and scientifically recognizable.

Use covariate domains when the full set is long, for example:

- demographics / socioeconomic status;
- disease severity;
- prior treatment;
- comorbidity;
- psychiatric or behavioral severity;
- healthcare utilization;
- concomitant medication.

Name a specific variable even within a domain when it is central to confounding control or audience interpretation.

Do not dump dozens of ICD/ATC codes, spline-basis terms, internal variable names, or redundant derived variables onto a main slide. Put the complete list and coding rules in backup when reproducibility matters.

## 6. Reproducibility-critical choices

When methods are a substantive part of the contribution, identify the small set of locked choices another analyst would need to reproduce the scientific contrast. Depending on the study, these may include:

- time zero or index-date definition;
- treatment/exposure strategy and comparator;
- grace period or exposure window;
- new-user, washout, or eligibility rules;
- artificial censoring or treatment-state transition rules;
- adjustment mechanism;
- covariate measurement windows;
- major functional forms or prespecified categories when non-obvious;
- weight truncation, matching caliper, or standardization target when material;
- time scale, recurrent-event structure, fixed-effects/strata/random-effects structure;
- lag rules;
- clustering level for uncertainty;
- missing-data strategy when it can change the analytic population or estimand.

Do not automatically put all of these in the main deck. Select the choices that define the estimand, address a major bias concern, or explain a result. Route the rest to backup.

## 7. Result-slide model notes

For important quantitative result slides, consider a compact model note in small text when the displayed estimate would otherwise be ambiguous. A good note usually contains no more than three elements:

1. estimator/model family;
2. adjustment mechanism and key covariate domains;
3. dependence/uncertainty feature only if important.

Example:

`Stabilized-IPCW weighted marginal Cox estimates; IPCW included prespecified demographic, clinical, treatment-history, psychiatric, and healthcare-utilization covariates; robust uncertainty clustered by individual.`

If the same model underlies several adjacent result slides, establish the model once in Methods and use a shorter repeated note on Results. Do not repeat a full methods paragraph on every slide.

When two results come from materially different models, make that difference visible even if both display hazard ratios. This is especially important for target-trial versus current-use, between-person versus within-person, two-state versus three-state, or primary versus landmark analyses.

## 8. Main deck versus backup

### Main deck

Keep details that:

- define the scientific contrast;
- materially affect bias control;
- explain why two analyses differ;
- establish that the model was prespecified or harmonized when this matters;
- are necessary to interpret the displayed estimate.

### Backup

Use backup for:

- full covariate dictionary;
- exact ICD/ATC code lists;
- complete measurement windows and coding categories;
- full functional-form specification;
- weight-model term disposition;
- matching/weight diagnostics beyond the main summary;
- software/package syntax;
- internal variable names;
- alternate computational engines that do not change the estimand.

A reproducible presentation does not require every implementation detail on the main path. It requires a clear route from the main scientific estimate to the full specification when questions arise.

## 9. Short wording patterns

### Directly adjusted survival model

`Adjusted Cox model; covariates: age, sex, disease severity, comorbidity, and prior treatment.`

### Weighted causal analysis

`Stabilized-IPCW weighted marginal survival estimates; IPCW based on prespecified baseline demographic, clinical, treatment-history, and care-process covariates.`

### Propensity-score analysis

`Propensity-score weighted analysis; propensity model included ...`

### Within-individual analysis

`Within-individual fixed-effects Cox model; adjusted for prespecified time-varying medication and treatment-state covariates.`

### Mixed model

`Linear mixed-effects model with participant-level random intercepts; adjusted for ...`

### Avoid on the main slide

- raw package syntax;
- regression formulas copied from code;
- phrases such as `not ITT` unless that distinction is itself necessary for the audience to interpret the study;
- exhaustive method qualifications that belong in the protocol rather than the presentation.

## 10. Audit

Before finalizing the storyboard, check:

- Can the audience tell what model or estimator produced each important effect estimate?
- Is the adjustment mechanism described accurately rather than generically?
- Are covariates shown at an appropriate level of detail?
- If two analyses use different estimands or model structures, is the difference visible?
- Have reproducibility-critical choices been surfaced when methods are central to the study contribution?
- Are code syntax and implementation-only detail kept out of the main deck unless needed?
- Is a full covariate/model specification available in backup for Q&A when appropriate?
