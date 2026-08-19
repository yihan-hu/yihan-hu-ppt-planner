# Plan Mode

## Contents

1. Purpose
2. Presentation contract
3. Source coverage
4. Story selection
5. Slide-budget and packing logic
6. Representation logic
7. Slide roles
8. On-slide versus spoken content
9. User-facing plan format
10. Main/backup/omit routing
11. Plan audit
12. Plan-to-build handoff
13. Short examples

## 1. Purpose

Turn scientific understanding and prioritized evidence into a reviewable slide plan. Do not begin with a slide list before understanding the study and selecting the evidence.

A useful flow is:

`Source -> Study understanding -> Literature enrichment if needed -> Analysis inventory -> Evidence priority -> Scientific claims -> Story -> Storyboard`

## 2. Presentation contract

Infer or establish:

- audience;
- talk type;
- approximate duration;
- scientific scope;
- core question;
- desired outcome;
- assumed audience knowledge.

Do not ask for information that can be inferred confidently from context. Ask only when the missing choice materially changes the plan.

## 3. Source coverage

Mark the user's source coverage as complete, partial, or missing for:

- background;
- question/aim;
- design;
- population;
- exposure/comparator;
- outcome;
- methods;
- results;
- interpretation;
- limitations.

If enough information exists to understand the study but Background is missing, continue and use literature enrichment rather than stopping unnecessarily.

## 4. Story selection

For a normal single study, prefer a recognizable scientific structure when it is clear:

`Background -> Knowledge gap -> Aim -> Methods -> Results -> Discussion -> Conclusion`

Do not force a novel narrative just to be clever.

Within that structure, optimize each section:

### Background

Use only what makes the study question understandable and necessary.

### Methods

Show the design and analytic choices needed to interpret the evidence. When quantitative estimates depend on nontrivial modeling or adjustment, plan a compact audience-facing model/adjustment description and reserve full implementation detail for backup.

### Results

Organize by scientific question/claim, not manuscript table or figure order.

### Discussion

Interpret rather than repeat. Include prior evidence and limitations that materially affect the conclusion.

## 5. Slide-budget and packing logic

Do not allocate slides equally across manuscript sections or according to source length.

Allocate more space when content has greater:

- scientific importance;
- number of reasoning steps;
- conceptual prerequisites;
- inferential complexity;
- methodological novelty;
- evidence density;
- interpretation complexity;
- need for overview/focus sequencing.

Do not use one-minute-per-slide as a hard rule.

Before splitting analyses across slides, perform a claim-level packing test:

1. Do the analyses support the same scientific claim?
2. Would side-by-side comparison improve interpretation?
3. Can they share one semantic representation and remain legible at presentation distance?
4. Would combining them preserve one main scientific job for the slide?

If yes, prefer one integrated slide. Do not default to one analysis, model, table, or workbook per slide.

Keep analyses separate when they form distinct narrative beats, especially when one creates an apparent contradiction and a later analysis resolves it, or when combining them would hide an important change in estimand, treatment state, or population.

## 6. Representation logic

Before exact layout, decide the semantic form of each slide.

Possible structures include:

- definition;
- contrast;
- timeline;
- cohort flow;
- study architecture;
- causal hypothesis;
- knowledge gap;
- comparison;
- dose-response;
- temporal pattern;
- interaction;
- evidence triangulation;
- mechanism;
- uncertainty;
- trade-off;
- overview -> focus -> interpretation.

Then recommend an appropriate representation such as:

- diagram;
- timeline;
- flowchart;
- forest plot;
- table;
- comparison chart;
- preserved figure;
- annotated figure;
- conceptual schematic;
- matrix;
- minimal question/transition slide.

Do not specify pixel coordinates, exact dimensions, or detailed visual styling in Plan Mode.

## 7. Slide roles

Allow a slide to have one primary role and optional secondary functions.

Possible primary roles:

- opening;
- orientation;
- background;
- prerequisite;
- question;
- hypothesis;
- design;
- methods;
- evidence;
- result;
- interpretation;
- limitation;
- synthesis;
- transition;
- take-home;
- backup.

Possible secondary functions:

- navigation;
- recap;
- comparison;
- methods;
- result;
- interpretation;
- state update;
- bridge.

Do not require every slide title to be a declarative claim. In longer academic talks, navigation labels such as "Methods" can coexist with a separate audience question and takeaway.

For conventional academic talks, default the **visible title** to a short neutral label or noun phrase, for example `Background`, `Study design`, `Statistical analysis`, `Primary results`, `Sensitivity analyses`, `Design 3: three-state analysis`, `Discussion`, or `Conclusion`. The slide may still have a strong internal scientific job, but that job does not need to appear as a headline claim.

Avoid visible titles that sound like a sales pitch, op-ed, or presenter instruction, such as `Why our design is better`, `Both trials were near null`, or `The protective signal disappears`. If a result needs a concise descriptive subtitle, use an objective phrase rather than an argumentative claim.

Never convert internal planning language into slide copy. Fields such as purpose, narrative role, evidence priority, slide job, transition logic, or comments like `the point is reproducibility` are planning metadata only unless the user explicitly asks to show them.

## 8. On-slide versus spoken content

Plan four layers when useful:

- `on_slide`: information the audience needs to see, compare, locate, or remember;
- `spoken_narrative`: explanation, nuance, or transition better delivered orally;
- `evidence`: figure, table, number, or design supporting the claim;
- `backup`: detail reserved for Q&A or deeper inspection.

Do not convert every speaking point into slide text.

For important quantitative result slides, add a compact `model_note` when needed to interpret the estimate. Use scientific prose rather than code syntax. The note should identify the estimator/model family and adjustment mechanism; include key covariates or covariate domains and clustering/stratification only when they materially affect interpretation. If covariates were used to estimate weights, matching, or standardization rather than entered directly in the outcome model, describe that path accurately.

## 9. User-facing plan format

Default to a readable plan with these sections. Adapt when the project is simple.

### A. Presentation strategy

Summarize audience/talk type/duration, core question, core message, and overall architecture.

### B. Study understanding

For epidemiology, summarize design, population, exposure/comparator, outcome, time structure, primary estimand, and major inferential concerns.

### C. Source coverage and literature needs

State what is supported by user material, what is missing, and what external literature is needed or was used.

### D. Result prioritization

Group results into:

- Core;
- Interpretation-critical;
- Supporting;
- Backup;
- Omitted.

Explain the reason for important routing decisions.

### E. Scientific claims

Compress selected analyses into the small number of claims the presentation should communicate. For complex or discordant evidence, briefly state which analyses are intentionally packed together because they support one claim and which are intentionally separated because they form distinct narrative beats.

### F. Slide-by-slide storyboard

For each slide, include only relevant fields from:

- Slide number;
- section;
- role;
- visible academic title/navigation label (normally short and neutral);
- internal purpose/scientific job (for planning only, not slide copy);
- optional subtitle/question when scientifically useful;
- key on-slide content;
- evidence/source;
- suggested representation;
- compact model/adjustment note when needed for quantitative interpretation;
- exact visible copy or row labels when the plan is intended for direct production;
- exact evidence values and reference groups when available;
- figure/table specification detailed enough to render without rediscovering the source;
- visible footnote/caveat when interpretation depends on it;
- must-preserve content;
- compressible content;
- spoken-only note when useful;
- source trace;
- layout freedom;
- takeaway;
- transition;
- backup link.

### G. Backup plan

Include only when relevant.

### H. Plan audit

Summarize major checks and any unresolved scientific gaps.

Keep the output easy to revise with comments such as "merge 5 and 6", "move this earlier", "put this in backup", or "split Figure 3 into overview and focus".

When the storyboard will be handed directly to a slide-building skill, read `references/production-handoff.md` and default to a content-complete, layout-flexible specification rather than a high-level outline. The builder should be able to decide how to lay out the page without having to decide what scientific content belongs on it.

## 10. Main/backup/omit routing

Use presentation routing such as:

- `main`;
- `supporting`;
- `backup`;
- `omit`.

`omit` means the content is unnecessary for this talk, not scientifically unimportant.

Do not remove evidence merely to create whitespace if it is necessary to understand or trust a claim.

## 11. Plan audit

### Scientific understanding

- Is the study question correct?
- Is the primary estimand correctly represented?
- Are methods and effect measures interpreted correctly?

### Evidence selection

- Is the primary result truly primary?
- Is interpretation-critical evidence retained?
- Are exploratory results dominating?
- Are null or discordant findings retained when scientifically important?

### Background and literature

- Does Background lead to the research question?
- Is external evidence clearly sourced and separated from user results?
- Are knowledge-gap claims justified?

### Inference

- Is claim strength appropriate for the design?
- Can the audience tell what estimator/model produced each important quantitative result?
- Is the adjustment path described accurately, especially when covariates enter weighting/matching/standardization rather than the outcome regression?
- Are important limitations or alternative explanations hidden?
- Are subgroup/interaction claims valid?

### Narrative

- Does each slide have a job?
- Are Methods placed before the evidence that depends on them?
- Are Results organized around questions and claims rather than manuscript order?
- Does the conclusion answer the opening question?

### Slide economy

- Are too many low-value details on the main path?
- Are analyses supporting the same claim unnecessarily split across slides?
- Have distinct contradiction/resolution beats been collapsed prematurely?
- Should dense evidence use overview -> focus -> interpretation?
- Is backup carrying detail that does not need main-stage attention?

### Provenance

- Can every scientific claim be traced to user material or an explicitly cited external source?
- Are planning inferences labeled as such when they could be mistaken for source claims?

### Production handoff

- Could a slide-building skill build each planned slide without re-reading the underlying study to decide what scientific content belongs on it?
- Are exact values, labels, reference groups, time horizons, and caveats supplied for quantitative slides?
- Are figure/table specifications concrete enough to render directly?
- Are `must_preserve` and `compressible` separated clearly?
- Are visible slide words separated from spoken-only or planner-only notes?
- Is enough layout freedom preserved for the builder to solve actual page-fit problems?

## 12. Plan-to-build handoff

After user approval, preserve:

- study model;
- primary estimand;
- selected scientific claims;
- claim strength;
- evidence priority;
- provenance;
- main/backup routing;
- planned narrative order;
- intentional repeated maps or navigation;
- figure/table treatment;
- approved visible copy and exact evidence values;
- must-preserve versus compressible content;
- model notes, caveats, source trace, and protected sequencing.

A later slide-building workflow may re-layout, compress, or split a dense slide for readability but should not silently change scientific meaning, evidence hierarchy, estimand, reference group, must-preserve content, or the approved conflict/resolution logic. It should not be expected to rediscover missing values, labels, caveats, or model definitions from the underlying files. If later user feedback changes the scientific role or interpretation of an analysis, rebuild the canonical plan before editing individual slide assignments.

## 13. Short examples

### Example A — Complete manuscript

Read the whole paper, reconstruct the study, inventory all results, classify them by role, compress to a few claims, then build a conventional scientific storyboard.

### Example B — Results only

Use the supplied aim/methods/results to reconstruct the study. Mark Background as missing, search only the literature needed to establish rationale/gap, then plan the deck.

### Example C — Too many results

Do not build one slide per table. Rank the analyses, identify which change interpretation, compress into claims, and route routine robustness to backup.
