# Plan Mode

## Contents

1. Purpose
2. Presentation contract
3. Source coverage
4. Story selection
5. Example-first concept development
6. Slide-budget and packing logic
7. Representation logic
8. Slide roles
9. On-slide versus spoken content
10. User-facing plan format
11. Main/backup/omit routing
12. Plan audit
13. Plan-to-build handoff
14. Short examples

## 1. Purpose

Turn scientific understanding and prioritized evidence into a reviewable slide plan. Do not begin with a slide list before understanding the study or concept and selecting the evidence/examples.

For study presentations, a useful flow is:

`Source -> Study understanding -> Analysis inventory -> Evidence priority -> Scientific claims -> Story -> Storyboard`

For teaching or conceptual presentations, a useful flow is:

`Source -> Audience problem -> Concrete example -> Observation/tension -> Concept -> Mechanism -> General rule -> Storyboard`

## 2. Presentation contract

Infer or establish:

- audience;
- talk type;
- approximate duration;
- scientific or technical scope;
- core question;
- desired outcome;
- assumed audience knowledge.

Do not ask for information that can be inferred confidently from context. Ask only when the missing choice materially changes the plan.

## 3. Source coverage

For a scientific study, mark coverage as complete, partial, or missing for background, question/aim, design, population, exposure/comparator, outcome, methods, results, interpretation, and limitations.

For a teaching or conceptual talk, additionally assess:

- which concepts are unfamiliar to the audience;
- which concrete examples or failure cases are available;
- whether the audience can experience the problem before hearing the terminology;
- whether the user supplied prior decks or notes that establish a speaking style.

If a user provides an old deck with speaker notes, treat it as both content evidence where relevant and a style source. Do not copy its scientific claims into a new topic unless they are actually relevant.

## 4. Story selection

For a normal single study, prefer a recognizable scientific structure when it is clear:

`Background -> Knowledge gap -> Aim -> Methods -> Results -> Discussion -> Conclusion`

Do not force a novel narrative just to be clever.

For teaching, methodological, or conceptual talks where the audience is unfamiliar with the topic, prefer a problem-driven structure:

`Concrete example -> what looks wrong or surprising -> why? -> concept -> mechanism -> general rule -> application`

The concept should appear when it answers a question the audience already has, not merely because it is logically prior in a textbook.

For conflict, replication, or sequential-investigation stories, allow tension -> diagnostic analysis -> resolution when the evidence supports it.

## 5. Example-first concept development

Read `references/example-first-teaching.md` for teaching, tutorial, methodological, conceptual, and group-meeting talks when the audience may not know the vocabulary.

For every major unfamiliar concept, ask:

1. Can the audience first see a concrete failure, contradiction, numerical example, code snippet, table, or diagram?
2. What should they notice before the concept is named?
3. What question should naturally arise?
4. What is the smallest definition needed to answer that question?
5. What mechanism or architecture explains the example?
6. What general rule should they remember?

Prefer:

`example -> observation -> question -> concept -> mechanism -> rule`

over:

`definition -> theory -> example`

when the former improves understanding.

Do not make example-first sequencing ceremonial. If an audience already knows the concept, or if the example adds noise, introduce the concept directly.

Allow one concept to take 2-3 slides when useful. For example:

- Slide A: naive approach / concrete example;
- Slide B: failure or contradiction;
- Slide C: name the concept and generalize.

Do not compress these into one dense slide merely to reduce slide count.

## 6. Slide-budget and packing logic

Do not allocate slides equally across manuscript sections, source length, or terminology count.

Allocate more space when content has greater:

- scientific importance;
- number of reasoning steps;
- conceptual prerequisites;
- inferential complexity;
- methodological novelty;
- evidence density;
- interpretation complexity;
- pedagogical difficulty;
- need for example -> concept sequencing;
- need for overview/focus sequencing.

Do not use one-minute-per-slide as a hard rule.

Before splitting analyses or examples across slides, perform a claim/concept-level packing test:

1. Do they support the same scientific claim or conceptual job?
2. Would side-by-side comparison improve interpretation?
3. Can they share one semantic representation and remain legible?
4. Would combining them preserve one main job for the slide?
5. Would combining them destroy an intended reveal, tension, or example-before-definition sequence?

If the first four are yes and the fifth is no, prefer one integrated slide.

Keep items separate when they form distinct narrative beats, especially when one creates an apparent contradiction and a later slide resolves it, or when an example is intentionally used before the concept is named.

## 7. Representation logic

Before exact layout, decide the semantic form of each slide.

Possible structures include:

- concrete example;
- failure case;
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
- naive approach -> failure -> fix;
- overview -> focus -> interpretation.

Then recommend a representation such as diagram, timeline, flowchart, forest plot, table, code snippet, before/after contrast, comparison chart, preserved figure, annotated figure, conceptual schematic, matrix, or minimal question/transition slide.

Do not specify pixel coordinates, exact dimensions, or detailed visual styling in Plan Mode.

## 8. Slide roles

Allow a slide to have one primary role and optional secondary functions.

Possible primary roles include opening, orientation, background, prerequisite, example, failure, question, hypothesis, concept introduction, design, methods, evidence, result, interpretation, limitation, synthesis, transition, take-home, and backup.

Do not require every slide title to be a declarative claim. In longer academic talks, navigation labels such as `Methods` can coexist with a separate audience question and takeaway.

For conventional academic talks, default visible titles to short neutral labels or noun phrases. For teaching sequences, simple titles such as `A simple example`, `What goes wrong?`, `Why this happens`, and `The general rule` are appropriate.

Avoid visible titles that sound like a sales pitch, op-ed, or presenter instruction. Never convert planner-facing metadata into slide copy.

## 9. On-slide versus spoken content

Plan four layers when useful:

- `on_slide`: information the audience needs to see, compare, locate, or remember;
- `spoken_narrative`: a brief planning-level explanation, nuance, or transition better delivered orally;
- `evidence`: figure, table, number, code example, failure case, or design supporting the claim/concept;
- `backup`: detail reserved for Q&A or deeper inspection.

When the user asks for a script/notes, provides a style example, or the plan is production-ready, add `speaker_notes`. Read `references/speaker-notes.md` before drafting them.

If an old deck or transcript is supplied, match the speaker's explanatory behavior: sentence length, use of `so/now/first/then/however`, degree of numerical detail, and step-by-step reasoning. Do not replace the user's oral register with generic polished prose.

Do not convert every speaking point into slide text. Slides show; notes explain.

For important quantitative result slides, add a compact `model_note` when needed to interpret the estimate.

## 10. User-facing plan format

Default to a readable plan with these sections. Adapt when the project is simple.

### A. Presentation strategy

Summarize audience/talk type/duration, core question, core message, and overall architecture. For teaching talks, state whether example-first sequencing is being used and why.

### B. Study or concept understanding

For epidemiology, summarize design, population, exposure/comparator, outcome, time structure, primary estimand, and major inferential concerns.

For conceptual talks, summarize the audience's starting mental model, the key failure/problem to expose, and the target concepts they should understand by the end.

### C. Source coverage and literature needs

State what is supported by user material, what is missing, and what external literature is needed or was used. Identify supplied old decks/notes used as a speaking-style reference.

### D. Evidence/example prioritization

Group items into Core, Interpretation-critical, Supporting, Backup, and Omitted. Explain important routing decisions.

### E. Scientific claims or conceptual takeaways

Compress the deck into the small number of claims or rules the presentation should communicate. For teaching, note which example is responsible for motivating each major concept.

### F. Slide-by-slide storyboard

For each slide, include only relevant fields from:

- slide number;
- section;
- role;
- visible academic title/navigation label;
- internal purpose/scientific or pedagogical job;
- optional audience question;
- key on-slide content;
- evidence/example/source;
- what the audience should notice before interpretation;
- whether a concept is intentionally not named yet;
- suggested representation;
- compact model/adjustment note when needed;
- exact visible copy when intended for direct production;
- exact evidence values when available;
- figure/table/code/example specification;
- visible footnote/caveat when needed;
- must-preserve content;
- compressible content;
- spoken-only note when useful;
- full `speaker_notes` when requested or for direct production;
- source trace;
- layout freedom;
- takeaway;
- transition;
- backup link.

### G. Backup plan

Include only when relevant.

### H. Plan audit

Summarize major checks and unresolved gaps. If speaker notes are included, confirm that they preserve the approved scope and the user's oral register.

Keep the output easy to revise with comments such as `merge 5 and 6`, `move this example earlier`, `do not name the concept yet`, `put this in backup`, or `split this into example and explanation`.

## 11. Main/backup/omit routing

Use `main`, `supporting`, `backup`, or `omit`.

`omit` means unnecessary for this talk, not scientifically unimportant.

Do not remove an example merely because it is simple if it is doing essential pedagogical work.

## 12. Plan audit

### Scientific/technical understanding

- Is the study question or technical concept correct?
- Is the primary estimand correctly represented when relevant?
- Are methods and effect measures interpreted correctly?
- Are technical terms defined accurately?

### Evidence/example selection

- Is the primary result truly primary?
- Is interpretation-critical evidence retained?
- Are null or discordant findings retained when scientifically important?
- Does each major teaching example actually illuminate the concept, rather than just decorate the slide?

### Teaching sequence

- For an unfamiliar concept, can the audience encounter the problem before the terminology?
- Is the concept named only after the example creates a reason to care?
- Is the definition shorter than the example/mechanism warrants?
- Has an example/concept pair been over-compressed into a dense slide?
- Does each concept end with a memorable general rule or application?

### Narrative

- Does each slide have one main job?
- Are Methods placed before evidence that depends on them?
- Are Results organized around questions/claims rather than manuscript order?
- Does each transition create the next question naturally?
- Does the conclusion answer the opening question?

### Speaker-note fidelity

- If the user supplied old notes, does the draft preserve sentence length, directness, connectors, and stepwise explanation?
- Does the speech sound like a researcher speaking, not a manuscript or consulting deck?
- Are complex derivations explained one step at a time?

### Slide economy

- Are too many low-value details on the main path?
- Are analyses supporting the same claim unnecessarily split?
- Have distinct contradiction/resolution or example/concept beats been collapsed prematurely?
- Is backup carrying detail that does not need main-stage attention?

### Provenance

- Can every scientific claim be traced to user material or an explicitly cited external source?
- Are planning inferences labeled when they could be mistaken for source claims?

### Production handoff

- Could a slide-building skill build each planned slide without deciding what content belongs on it?
- Are exact values, labels, caveats, examples, and protected sequencing supplied?
- Are visible slide words separated from spoken-only or planner-only notes?
- If full speaker notes are included, do they preserve the canonical story and the user's speaking style?
- Is enough layout freedom preserved for the builder to solve page-fit problems?

## 13. Plan-to-build handoff

After user approval, preserve:

- study model or conceptual sequence;
- primary estimand when relevant;
- selected scientific claims/conceptual takeaways;
- evidence/example priority;
- provenance;
- main/backup routing;
- planned narrative order;
- protected example-before-concept reveals;
- intentional repetitions;
- figure/table/code/example treatment;
- approved visible copy and exact evidence values;
- must-preserve versus compressible content;
- model notes, caveats, source trace, protected sequencing, and approved speaker notes when present.

A later slide-building workflow may re-layout, compress, or split a dense slide for readability but should not silently change scientific meaning, evidence hierarchy, conceptual teaching order, protected examples, conclusion strength, or planner-authored speaker notes.

## 14. Short examples

### Example A — Complete manuscript

Read the whole paper, reconstruct the study, inventory all results, classify them by role, compress to a few claims, then build a conventional scientific storyboard.

### Example B — Conceptual teaching

Do not start with a formal definition if a simple example can create the need for it. Show the case, ask what went wrong, introduce the concept, then generalize.

### Example C — Odds ratio in case-control studies

Start from a full-population 2x2 table, calculate risk and odds, then change to case-control sampling. Let the audience see that the risk denominator becomes artificial while the odds ratio is preserved. Introduce the principle only after the numerical example.

### Example D — Progressive disclosure in Agent Skills

Start from the naive idea of putting every rule into `SKILL.md`. Show how the file becomes long and important rules lose salience. Then move details into references and show the next failure: the model may never load them. Only then introduce the general architecture: `SKILL.md = control`, `references = knowledge`, `runtime = enforcement`.