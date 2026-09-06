---
name: ppt-planner
description: Plan academic, scientific, teaching, and conceptual PowerPoint presentations before slide production. Use when turning papers, protocols, results, figures, incomplete study materials, technical concepts, or prior decks with speaker notes into a grounded storyboard; prioritizing evidence; teaching unfamiliar concepts from examples; matching a supplied speaking style; synthesizing conflicting designs or estimands; deciding main versus backup content; specifying presentation-facing statistical details; or preparing a content-complete handoff for slide production. Produce the presentation plan and slide-ready content, not a finished PPTX.
---

# PPT Planner

## Objective

Plan the argument before visual slide production. First understand the scientific or technical content, then decide what matters, then decide how the audience should encounter it and how the researcher should explain it aloud.

The planner owns both the storyline and, when requested or production-ready, the speaker-note draft. The note-writing pass must follow the approved scope, concept sequence, and analysis-role logic rather than reinterpret the content after the slides are planned.

Do not treat a manuscript's section order, table order, figure order, terminology hierarchy, or statistical significance ranking as the slide plan.

Do not create a finished PPTX in this skill. Stop after presenting the plan unless the user explicitly asks to continue with a separate slide-building workflow.

## Core workflow

1. Inspect all user-provided source material before planning, including prior decks and speaker notes when supplied.
2. Set a presentation contract: audience, talk type, approximate duration, scientific/technical scope, core question, desired outcome, and assumed knowledge. Infer obvious items; ask only when missing information would materially change the plan.
3. Assess source coverage: background, question/aim, design or conceptual structure, methods/mechanism, evidence/examples, interpretation, limitations, and any existing speaking-style evidence.
4. Reconstruct the scientific study or technical concept before selecting slides.
5. For teaching, methodological, conceptual, tutorial, or group-meeting talks where the audience may not know the vocabulary, read `references/example-first-teaching.md` before story selection. Prefer `example -> observation -> question -> concept -> mechanism -> general rule` when the audience can experience the need for the concept before it is named.
6. For epidemiological or clinical population research, read `references/epidemiology-study-planning.md` and identify the study design, time structure, primary estimand, main analyses, and major inferential concerns.
7. When statistical model specification, confounding adjustment, weighting, clustering, time-varying structure, or other analytic choices materially affect interpretation or reproducibility, read `references/model-detail-for-slides.md`. Plan audience-facing model/adjustment notes rather than code syntax, and distinguish covariates used directly in the outcome model from covariates used to construct weights, matching, standardization, or other adjustment mechanisms.
8. For academic talks, read `references/academic-slide-language.md` before drafting visible slide titles or on-slide prose. Default to conventional, neutral, descriptive titles and keep planner logic, sales-style claims, and meta-commentary out of the slide copy.
9. If background, prior evidence, knowledge gap, discussion context, or useful external visuals are missing or weak, read `references/literature-enrichment.md` and search the academic literature as needed.
10. Inventory the full set of analyses, examples, failure cases, and results before deciding what belongs in the presentation.
11. If the project has multiple designs, multiple estimands, replication, decomposition, discordant findings, interpretation-critical sensitivity analyses, or an intended conclusion that must be stress-tested, read `references/scientific-story-synthesis.md` and build the analysis-role, conflict/resolution, and claim maps before drafting slides.
12. Classify each important analysis or example on two separate dimensions: scientific/evidentiary importance and narrative role. Do not let a supportive or sensitivity label automatically make an analysis narratively minor; likewise, do not let an example become decorative if it is the mechanism by which the audience discovers a concept.
13. Stress-test the intended conclusion against the full evidence and teaching sequence. Treat the user's preferred framing as a hypothesis to test, not a conclusion to force.
14. Choose the simplest story that fits the evidence and audience. For a normal single study, prefer a recognizable scientific structure. For unfamiliar concepts, prefer problem/example first, then abstraction. For conflict, replication, or sequential investigation, allow tension -> diagnostic analysis -> resolution.
15. Build the slide-by-slide storyboard using `references/plan-mode.md`. Pack analyses by scientific claim and conceptual job rather than defaulting to one analysis or one term per slide.
16. When the user asks for a script/notes, provides an example speaking style, or intends to proceed directly into slide production, read `references/speaker-notes.md`. Treat supplied old decks/notes as the primary style reference. Draft the spoken narrative only after the story and slide order are stable. For a production-ready handoff, default to full per-slide `speaker_notes`; for an early plan, a shorter `spoken_narrative` is enough.
17. When the plan is intended for direct slide production, read `references/production-handoff.md` and make the storyboard content-complete: supply actual visible copy, exact evidence values, figure/table/example specifications, model notes, caveats, must-preserve content, compressible content, approved speaker notes, source trace, and layout freedom as relevant.
18. If the talk is a defense, multi-study thesis, multi-paper seminar, or complex sequential investigation, additionally read `references/advanced-narrative.md`.
19. Audit the plan for scientific fidelity, evidence/example selection, provenance, inference, teaching sequence, narrative completeness, conclusion strength, slide economy, academic wording, speaker-note fidelity, and production-handoff completeness.
20. Present the plan and stop for user review.
21. If later user feedback changes an analysis's scientific role, a concept's teaching sequence, the audience level, conclusion, preferred academic wording convention, speaking style, or handoff requirements, rebuild the synthesis and canonical storyboard before revising individual slides or notes. Do not patch an obsolete story locally.

## Example-first teaching rule

For explanatory talks, prefer to let the audience encounter the problem before naming the solution whenever that improves understanding.

Use:

`concrete example -> something surprising/wrong/incomplete -> why? -> concept -> mechanism -> general rule`

Do not force this pattern when the audience already knows the concept or when the example would add noise. The rule is pedagogical, not ceremonial.

For each major unfamiliar concept, ask: `Can the audience experience the problem before I name the solution?`

## Scientific provenance

Keep three origins distinct throughout planning:

- `user_material`: supplied papers, tables, figures, results, drafts, protocols, notes, old decks, or examples.
- `external_literature`: evidence retrieved from outside sources.
- `planning_inference`: structural or interpretive reasoning introduced for presentation planning.

Never present external literature as the user's own result. Never present a planning inference as a published scientific conclusion.

If user-provided sources do not support a factual claim, do not silently fill it with general knowledge. Either mark it as missing or, when literature enrichment is appropriate, search and cite an external source explicitly.

## Evidence and example selection rules

Prioritize scientific importance and explanatory value over visual attractiveness or statistical significance.

Normally give highest priority to evidence or examples that:

- directly answer the primary research question or primary estimand;
- materially change interpretation of the primary result;
- address a major alternative explanation;
- establish temporality, robustness, or meaningful effect modification needed to trust the conclusion;
- reproduce, decompose, explain, or reconcile an important finding;
- expose the exact failure or contradiction that makes an unfamiliar concept necessary;
- carry major scientific, clinical, methodological, or pedagogical importance;
- are necessary to understand the Discussion or final conclusion.

Do not automatically promote the smallest p-value, largest effect estimate, most colorful figure, first table, or first result.

Do not automatically move sensitivity analyses, null results, supportive analyses, replications, or simple toy examples to backup. An item can be main-deck evidence when it resolves a major inferential concern or enables the audience to discover the concept.

## Slide-level synthesis rules

Plan around claims and conceptual jobs, not files, models, or vocabulary terms.

- Prefer one integrated slide when multiple analyses or examples support the same claim and remain legible.
- Do not split primary and sensitivity results merely because they were produced separately.
- Do not merge distinct narrative beats, especially when one creates a contradiction and a later slide resolves it.
- For teaching, allow one concept to unfold across 2-3 slides when the audience needs `example -> problem -> concept -> rule`.
- Use the principle `one main job per slide`, not `one analysis per slide` or `one term per slide`.
- Keep method detail proportional to what the audience needs to interpret the evidence or understand the mechanism.

## Academic slide-title and wording rules

For conventional scientific presentations, separate the **job of a slide** from its **visible title**. Claim-level planning may drive evidence selection internally, but visible academic slide titles should usually be short, neutral, and descriptive.

For teaching sequences, simple question or example titles are also appropriate, such as `A simple example`, `What goes wrong?`, `Why this happens`, and `The general rule`.

Do not default to keynote, consulting, marketing, or journalistic headline titles that state the interpretation before the audience sees the evidence.

Keep interpretation in the figure/table/example, concise caption, body text, spoken narrative, Discussion, or Conclusion. Never place planner-facing meta-language on slides.

For methods slides, describe what was done. For results slides, describe what was observed. For teaching slides, show the example before overloading the page with the abstract definition.

## Default presentation behavior

For a conventional single study, use this grammar when appropriate:

`Scientific problem -> What is known -> Knowledge gap -> Aim -> Study design -> Statistical strategy -> Primary result -> Interpretation-critical secondary evidence -> Discussion -> Conclusion`

For conceptual teaching, use this grammar when appropriate:

`Concrete problem/example -> observation -> question -> concept -> mechanism -> general rule -> application`

Keep Background selective. Keep Methods proportional to what the audience needs. Organize Results by scientific question and claim, not table/figure numbering.

## Output

Use the user-facing format in `references/plan-mode.md`. Default to a readable plan rather than dumping internal schemas.

At minimum, make clear:

- what the study or concept is actually asking;
- what source material is complete or missing;
- which external literature is needed or used;
- which results/examples are core, interpretation-critical, supporting, backup, or omitted;
- what scientific and narrative role each important analysis or example serves;
- which unfamiliar concepts should be discovered from an example before being named;
- what each planned slide is for;
- which analyses/examples should be combined versus separated for narrative reasons;
- what should be shown on-slide versus explained orally;
- when notes are requested or the plan is production-ready, the actual per-slide speaker-note draft in the user's researcher oral register when a style example exists;
- where reproducibility detail belongs in backup when relevant;
- when the plan will feed slide production, the actual slide-ready copy, exact numbers/labels, figure/table/example contents, model notes/caveats, must-preserve items, compressible items, source trace, and layout freedom needed by the builder.

## Handoff to slide production

Treat the handoff as a content contract, not a loose outline. For production-ready plans, the planner owns scientific/technical content completeness and the slide-building skill owns layout/visual execution. Read `references/production-handoff.md`.

When the user approves the plan, preserve the approved:

- study model, conceptual sequence, and primary estimand when relevant;
- scientific claims and claim strength;
- evidence/example priority and main/backup routing;
- analysis-role and conflict/resolution logic;
- example-first teaching sequence where intentionally used;
- external-literature provenance;
- narrative order and intentional repetitions;
- planned slide packing and figure/table/example treatment;
- visible slide copy and exact evidence values where specified;
- must-preserve versus compressible content;
- model notes, caveats, source trace, protected sequencing, and approved speaker notes when included.

A later slide-building workflow may re-layout, compress, or split a dense slide for readability, but it should not silently change scientific meaning, evidence hierarchy, conceptual teaching order, estimand, reference group, protected evidence, conclusion strength, or the approved speaker notes.