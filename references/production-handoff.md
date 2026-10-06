# Production-Ready Handoff to Slide-Building Skills

## Purpose

Make the planner output complete enough that a slide-building skill can start from the approved storyboard without re-reading the study to decide what scientific content belongs on each slide.

Use this reference when:

- the user intends to continue into `academic-ppt` or another slide-building workflow;
- the user asks for a deck plan detailed enough to build directly;
- the project has complex methods, multiple analyses, exact numerical results, important caveats, concrete examples, or failure-case teaching sequences that should not be rediscovered during layout;
- a prior slide build exposed missing content decisions in the planner output.

The planner owns **scientific/technical content completeness and story sequence**. The slide-building skill owns **layout, visual hierarchy, packing, rendering, and QA**.

## 1. Handoff principle

Produce a `content-complete, layout-flexible storyboard`.

The planner should decide:

- what each slide contains;
- exact visible wording when the source supports it;
- which numerical estimates, labels, denominators, time windows, and caveats must appear;
- figure/table rows and required annotations;
- which concrete examples or failure steps must appear before the concept is named;
- what is spoken only;
- what may be compressed or moved to backup;
- what must not be deleted, merged, reordered, or reinterpreted because it changes the scientific or teaching logic.

The slide-building skill may decide:

- exact layout/template choice;
- typography, spacing, visual grouping, and image treatment;
- whether a dense slide needs to split into two;
- whether repeated wording can be shortened without changing meaning;
- whether a table becomes a figure or vice versa when the scientific information is preserved;
- minor ordering within a slide for visual clarity, unless the planner marked a protected sequence.

Do not leave missing scientific content, example details, or case steps for the slide-building skill to infer from protocol files, result folders, literature, or prior conversation unless the source is genuinely unavailable.

## 2. Required per-slide fields

For a production-ready handoff, specify the following when relevant.

### `visible_title`

Write the actual title intended to appear on the slide. For conventional academic talks, use a short neutral label or noun phrase.

For teaching and case-driven slides, prefer titles that identify what the audience is looking at, not titles that reveal the conclusion early. Good examples: `A simple example`, `Prompt v1`, `What goes wrong?`, `Codex: fixing a failing test`, `A repeated-step problem`, `A more engineered solution`, `Another solution`.

Avoid premature summary titles such as `More control is not always better`, `A paradigm shift`, or `You do not need GPT's architecture` before the case has made that point.

### `visible_subtitle`

Optional. Write the actual subtitle or analysis qualifier if useful. Do not use it for planner commentary.

### `on_slide_copy`

Write the visible bullets, labels, row headings, short explanatory sentences, and other text closely enough that it can be inserted directly into the slide.

Do not merely write `show eligibility criteria`, `summarize weighting`, or `show a prompt failure`. Supply the intended wording and the actual items.

### `case_setup`

Use this for case-driven teaching slides. State the concrete situation before abstraction.

Examples:

- `Task: revise a manuscript paragraph without changing scientific meaning.`
- `Task: a repository has one failing test; fix it.`
- `Problem: a Skill sometimes executes the same step twice.`

### `case_steps`

List the concrete sequence the audience must see or hear in order.

For a failure case, include as many as apply:

1. initial attempt;
2. observed failure;
3. first patch;
4. new edge case or second failure;
5. heavier proposed solution;
6. reframing question;
7. smaller/better solution;
8. concept revealed after the case.

Do not replace these steps with a summary label.

### `protected_sequence`

Use this when the order itself teaches the point. A protected sequence may be split across slides, but it must not be collapsed into an abstract framework, slogan, generic diagram, or unordered card set.

Write it explicitly, for example:

```text
protected_sequence:
1. Prompt v1 only asks for revision
2. Model changes scientific meaning
3. User adds preserve-meaning rule
4. Model preserves meaning but changes numbers
5. User adds number rule
6. Prompt has become task + rules + exceptions + checks
7. Now introduce Skill
```

### `concept_revealed_after_case`

If a concept should not appear until after the example creates the need for it, name it here. The builder must not put this concept into the title, headline, navigation, or opening graphic of the earlier case slide.

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

List content or sequencing that the slide-building skill must not remove, merge, reorder, or reinterpret. Examples:

- all primary estimates and CIs;
- reference category definition;
- separation of two-state replication and three-state decomposition into distinct slides;
- a limitation required to interpret the outcome;
- a null/reference line and effect measure;
- an analysis order required for the scientific logic;
- a failure-case order required for the teaching logic;
- the exact prompt/code/table fragment that makes the case concrete.

If `must_preserve` content does not fit, the builder should split the slide rather than silently omit or abstract it.

### `compressible`

List content that may be abbreviated, reduced, moved to a footnote, or sent to backup if needed for legibility.

### `spoken_only`

List explanation, nuance, presenter transitions, or rationale that should normally not be copied onto the slide.

### `source_trace`

Trace important claims, definitions, examples, and estimates to their source material. Include file/workbook/table/figure references, prior-deck references, conversation decisions, or external literature provenance as available.

### `layout_freedom`

State the visual degrees of freedom. Examples:

- paired panels, two-row forest plot, or compact table are all acceptable;
- builder may split into two slides if labels become unreadable;
- figure and text may swap left/right;
- table must remain a table because exact row-wise reading matters;
- protected sequence must remain sequential, but visual representation may be timeline, stacked prompt versions, or stepwise before/after.

## 3. Minimum completeness by slide type

### Background / previous studies

Provide the actual studies, comparison dimensions, main estimates or conclusions, and citation/source trace. If recommending a literature table, specify its columns and rows.

### Study design / methods

Provide the exact design-defining choices needed to understand or reproduce the scientific contrast: time zero, treatment strategies, grace period, new-user/washout rules, censoring/state rules, follow-up, adjustment mechanism, major covariate domains, model family, and important thresholds when relevant.

Do not dump implementation code. Do not leave these items as vague labels if the source defines them precisely.

### Results

Provide the full planned plotting/table dataset for the slide: row labels, point estimates, CIs, denominators/events when needed, reference categories, time horizons, and model note. For a forest plot, the builder should not have to search the result folder to reconstruct rows.

### Teaching / conceptual slides

Provide the actual example, not only the concept name.

For each concept that is introduced through an example, specify:

- audience starting assumption;
- concrete example or failure;
- what the audience should notice;
- the question that should arise;
- the smallest definition that follows;
- the general rule or application.

If the example is a prompt, code snippet, command, small table, or visual, provide the exact visible fragment or a faithful simplified version.

### Failure-case slides

Provide the actual sequence. Do not write only `failure case`.

A complete failure case usually needs:

- original task;
- initial solution;
- observed failure;
- attempted patch;
- new failure or cost;
- better solution or boundary decision;
- concept/rule introduced after the audience sees the failure.

Mark the sequence as `protected_sequence` when the order matters.

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
- invent missing case steps;
- drop `must_preserve` evidence to make the slide cleaner;
- replace concrete examples with generic labels;
- strengthen or weaken the claim;
- change reference groups, estimands, time horizons, or analysis labels;
- merge distinct narrative beats when the plan explicitly protects their separation;
- reveal a concept in the title before an intentionally example-first slide;
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

For a case-driven teaching slide, use:

```text
Slide 4
visible_title: Prompt v1 -> v4
role: failure case

case_setup:
- Task: revise a manuscript paragraph without changing scientific meaning.

case_steps:
1. Prompt v1: Revise this paragraph.
2. Failure: model changes the scientific claim.
3. Patch: add `Preserve scientific meaning`.
4. Failure: model preserves meaning but changes numbers.
5. Patch: add `Do not change numbers`.
6. New cost: prompt is now task + rules + exceptions + checks.
7. Concept revealed after this slide: Agent Skill.

must_preserve:
- The prompt-version sequence
- At least two concrete failures and two patches
- Do not title this slide `Skill is not a long prompt`

layout_freedom:
- May use stacked prompt cards, timeline, or before/after columns. Split if needed.
```

Use readable prose rather than literal YAML/JSON unless the user asks for machine-readable output.

## 6. Handoff audit

Before finalizing a production-ready plan, verify:

- Could a slide-building skill build the deck without deciding what scientific content to add?
- Are exact numbers, labels, time points, reference groups, and caveats supplied for quantitative slides?
- Are figure/table specifications concrete enough to render directly?
- For teaching slides, are the concrete examples and case steps supplied, not only the concepts?
- Are protected sequences clearly marked when order teaches the point?
- Are visible slide words separated from planner notes and spoken-only content?
- Are `must_preserve` and `compressible` clearly distinguished?
- Is layout flexibility preserved so the builder can solve actual page-fit problems?
- Is every important scientific item traceable to user material or explicitly labeled external literature/planning inference?
