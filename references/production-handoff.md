# Production-Ready Handoff to Slide-Building Skills

## Purpose

Make the planner output complete enough that a slide-building skill can start from the approved storyboard without re-reading the study to decide what scientific content belongs on each slide.

Use this reference when:

- the user intends to continue into `academic-ppt` or another slide-building workflow;
- the user asks for a deck plan detailed enough to build directly;
- the project has complex methods, multiple analyses, exact numerical results, or important caveats that should not be rediscovered during layout;
- a prior slide build exposed missing content decisions in the planner output.

The planner owns **scientific content completeness**. The slide-building skill owns **layout, visual hierarchy, packing, rendering, and QA**.

## 1. Handoff principle

Produce a `content-complete, layout-flexible storyboard`.

The planner should decide:

- what each slide contains;
- exact visible wording when the source supports it;
- which numerical estimates, labels, denominators, time windows, and caveats must appear;
- figure/table rows and required annotations;
- what is spoken only;
- what may be compressed or moved to backup;
- what must not be deleted or merged because it changes the scientific logic.

The slide-building skill may decide:

- exact layout/template choice;
- typography, spacing, visual grouping, and image treatment;
- whether a dense slide needs to split into two;
- whether repeated wording can be shortened without changing meaning;
- whether a table becomes a figure or vice versa when the scientific information is preserved;
- minor ordering within a slide for visual clarity.

Do not leave missing scientific content for the slide-building skill to infer from protocol files, result folders, or literature unless the source is genuinely unavailable.

## 2. Required per-slide fields

For a production-ready handoff, specify the following when relevant.

### `visible_title`

Write the actual title intended to appear on the slide. For conventional academic talks, use a short neutral label or noun phrase.

### `visible_subtitle`

Optional. Write the actual subtitle or analysis qualifier if useful. Do not use it for planner commentary.

### `on_slide_copy`

Write the visible bullets, labels, row headings, short explanatory sentences, and other text closely enough that it can be inserted directly into the slide.

Do not merely write `show eligibility criteria` or `summarize weighting`. Supply the intended wording and the actual items.

### `evidence_values`

List the exact values that must be represented: sample sizes, events, effect estimates, confidence intervals, time horizons, denominators, reference groups, units, thresholds, or other quantitative content.

### `figure_spec`

For a figure, specify:

- figure purpose/type;
- required structure or state order;
- exact row or node labels;
- effect measure and reference/null line when quantitative;
- required time points, groups, or contrasts;
- annotations that affect interpretation;
- whether the figure must preserve a published/source visual or may be redrawn deterministically.

A generic instruction such as `make a target-trial diagram` is insufficient when source material supports a more exact specification.

### `table_spec`

For a table, specify:

- columns;
- row labels;
- exact cell content or values when available;
- row grouping/order;
- which estimates should be emphasized;
- required footnotes or definitions.

### `model_note`

Write the recommended compact audience-facing model/adjustment note exactly or nearly exactly as it should appear. Distinguish direct covariate adjustment from weighting/matching/standardization.

### `footnote_or_caveat`

Write any visible caveat that materially changes interpretation, such as an unavailable outcome component, an approximate replication, residual imbalance, selected population, or unstable estimate.

### `must_preserve`

List content or sequencing that the slide-building skill must not remove, merge, or reinterpret. Examples:

- all primary estimates and CIs;
- reference category definition;
- separation of two-state replication and three-state decomposition into distinct slides;
- a limitation required to interpret the outcome;
- a null/reference line and effect measure;
- an analysis order required for the scientific logic.

If `must_preserve` content does not fit, the builder should split the slide rather than silently omit it.

### `compressible`

List content that may be abbreviated, reduced, moved to a footnote, or sent to backup if needed for legibility.

### `spoken_only`

List explanation, nuance, presenter transitions, or rationale that should normally not be copied onto the slide.

### `source_trace`

Trace important claims, definitions, and estimates to their source material. Include file/workbook/table/figure references or external literature provenance as available.

### `layout_freedom`

State the visual degrees of freedom. Examples:

- paired panels, two-row forest plot, or compact table are all acceptable;
- builder may split into two slides if labels become unreadable;
- figure and text may swap left/right;
- table must remain a table because exact row-wise reading matters.

## 3. Minimum completeness by slide type

### Background / previous studies

Provide the actual studies, comparison dimensions, main estimates or conclusions, and citation/source trace. If recommending a literature table, specify its columns and rows.

### Study design / methods

Provide the exact design-defining choices needed to understand or reproduce the scientific contrast: time zero, treatment strategies, grace period, new-user/washout rules, censoring/state rules, follow-up, adjustment mechanism, major covariate domains, model family, and important thresholds when relevant.

Do not dump implementation code. Do not leave these items as vague labels if the source defines them precisely.

### Results

Provide the full planned plotting/table dataset for the slide: row labels, point estimates, CIs, denominators/events when needed, reference categories, time horizons, and model note. For a forest plot, the builder should not have to search the result folder to reconstruct rows.

### Discussion / interpretation

Separate source-supported observations from planning inference. Supply calibrated wording and explicitly flag overclaims to avoid.

### Backup

Specify the question the backup slide answers and the exact content needed to answer it. Do not route material to backup merely as `full methods` or `more sensitivity analyses` when exact items are known.

## 4. Packing and builder freedom

Planner granularity should not freeze visual layout.

The builder may:

- compress redundant prose;
- convert a list into a diagram or table;
- combine compatible result rows into one forest plot;
- split a dense slide when necessary for legibility;
- move low-priority detail to a footnote or backup if marked compressible.

The builder may not:

- invent missing scientific details;
- drop `must_preserve` evidence to make the slide cleaner;
- strengthen or weaken the claim;
- change reference groups, estimands, time horizons, or analysis labels;
- merge distinct narrative beats when the plan explicitly protects their separation;
- replace a source-supported caveat with generic wording.

## 5. Canonical handoff format

For each production-ready slide, use a compact structure like:

```text
Slide 12
visible_title: Design 3: three-state analysis
visible_subtitle: Current use and post-discontinuation periods modeled separately

on_slide_copy:
- Exposure states: pre-initiation no use; current GLP-1RA use; post-discontinuation
- Reference: pre-initiation no use

figure_spec:
- Four-row forest plot
- 30-day lag: current use 0.96 (0.65-1.42); discontinuation 1.58 (1.10-2.26)
- 60-day lag: current use 0.99 (0.57-1.72); discontinuation 1.71 (1.07-2.73)
- Null line: HR = 1.0

model_note:
- Within-individual fixed-effects Cox analysis of recurrent events; treatment-state exposure lagged by 30 or 60 days.

footnote_or_caveat:
- Post-discontinuation estimates are observational treatment-state associations and should not be interpreted as the causal effect of stopping treatment.

must_preserve:
- Reference category definition
- Both lag analyses and all CIs
- Distinction between current use and discontinuation

compressible:
- Event counts may move to backup

spoken_only:
- Explain that two-state non-use had included post-discontinuation time.

source_trace:
- three-state results workbook; protocol treatment-state definition

layout_freedom:
- State diagram and forest plot may be left/right or top/bottom; split only if labels become unreadable.
```

Use readable prose rather than literal YAML/JSON unless the user asks for machine-readable output.

## 6. Handoff audit

Before finalizing a production-ready plan, verify:

- Could a slide-building skill build the deck without deciding what scientific content to add?
- Are exact numbers, labels, time points, reference groups, and caveats supplied for quantitative slides?
- Are figure/table specifications concrete enough to render directly?
- Are visible slide words separated from planner notes and spoken-only content?
- Are `must_preserve` and `compressible` clearly distinguished?
- Is layout flexibility preserved so the builder can solve actual page-fit problems?
- Is every important scientific item traceable to user material or explicitly labeled external literature/planning inference?
