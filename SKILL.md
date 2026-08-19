# PPT Planner

## Objective

Plan the scientific argument before visual slide production. First understand the study, then decide what evidence matters, then decide how to present it.

Do not treat a manuscript's section order, table order, figure order, or statistical significance ranking as the slide plan.

Do not create a finished PPTX in this skill. Stop after presenting the plan unless the user explicitly asks to continue with a separate slide-building workflow.

## Core workflow

1. Inspect all user-provided source material before planning.
2. Set a presentation contract: audience, talk type, approximate duration, scientific scope, core question, desired outcome, and assumed knowledge. Infer obvious items; ask only when missing information would materially change the plan.
3. Assess source coverage: background, research question, design, population, exposure/comparator, outcomes, methods, results, interpretation, and limitations.
4. Reconstruct the scientific study before selecting slides.
5. For epidemiological or clinical population research, read `references/epidemiology-study-planning.md` and identify the study design, time structure, primary estimand, main analyses, and major inferential concerns.
6. When statistical model specification, confounding adjustment, weighting, clustering, time-varying structure, or other analytic choices materially affect interpretation or reproducibility, read `references/model-detail-for-slides.md`. Plan audience-facing model/adjustment notes rather than code syntax, and distinguish covariates used directly in the outcome model from covariates used to construct weights, matching, standardization, or other adjustment mechanisms.
7. For academic talks, read `references/academic-slide-language.md` before drafting visible slide titles or on-slide prose. Default to conventional, neutral, descriptive titles and keep planner logic, sales-style claims, and meta-commentary out of the slide copy.
8. If background, prior evidence, knowledge gap, discussion context, or useful external visuals are missing or weak, read `references/literature-enrichment.md` and search the academic literature as needed.
9. Inventory the full set of analyses and results before deciding what belongs in the presentation.
10. If the project has multiple designs, multiple estimands, replication, decomposition, discordant findings, interpretation-critical sensitivity analyses, or an intended conclusion that must be stress-tested, read `references/scientific-story-synthesis.md` and build the analysis-role, conflict/resolution, and claim maps before drafting slides.
11. Classify each important analysis on two separate dimensions: scientific evidence hierarchy and narrative role. Do not let a supportive or sensitivity label automatically make an analysis narratively minor.
12. Stress-test the intended conclusion against the full result inventory. Treat the user's preferred framing as a hypothesis to test, not a conclusion to force.
13. Choose the simplest scientific story that fits the evidence. For a normal single study, prefer Background -> Methods -> Results -> Discussion. For conflict, replication, or sequential-investigation stories, allow tension -> diagnostic analysis -> resolution when the evidence supports it.
14. Build the slide-by-slide storyboard using `references/plan-mode.md`. Pack analyses by scientific claim rather than defaulting to one analysis per slide.
15. When the plan is intended for direct slide production, especially handoff to Academic PPT, read `references/production-handoff.md` and make the storyboard content-complete: supply actual visible copy, exact evidence values, figure/table specifications, model notes, caveats, must-preserve content, compressible content, spoken-only notes, source trace, and layout freedom as relevant.
16. If the talk is a defense, multi-study thesis, multi-paper seminar, or complex sequential investigation, additionally read `references/advanced-narrative.md`.
17. Audit the plan for scientific fidelity, evidence selection, provenance, inference, narrative completeness, conclusion strength, slide economy, academic wording, and production-handoff completeness.
18. Present the plan and stop for user review.
19. If later user feedback changes an analysis's scientific role, evidence hierarchy, estimand interpretation, conclusion, preferred academic wording convention, or handoff requirements, rebuild the synthesis and canonical storyboard before revising individual slides. Do not patch an obsolete story locally.

## Scientific provenance

Keep three origins distinct throughout planning:

- `user_material`: supplied papers, tables, figures, results, drafts, protocols, or notes.
- `external_literature`: evidence retrieved from outside sources.
- `planning_inference`: structural or interpretive reasoning introduced for presentation planning.

Never present external literature as the user's own result. Never present a planning inference as a published scientific conclusion.

If user-provided sources do not support a factual claim, do not silently fill it with general knowledge. Either mark it as missing or, when literature enrichment is appropriate, search and cite an external source explicitly.

## Evidence selection rules

Prioritize scientific importance over visual attractiveness or statistical significance.

Normally give highest priority to evidence that:

- directly answers the primary research question or primary estimand;
- materially changes interpretation of the primary result;
- addresses a major alternative explanation such as confounding, reverse causality, exposure-state definition, or post-treatment selection;
- establishes temporality, robustness, or meaningful effect modification needed to trust the conclusion;
- reproduces, decomposes, explains, or reconciles an important published or internal finding;
- carries major scientific, clinical, or methodological importance;
- is necessary to understand the Discussion or final conclusion.

Do not automatically promote the smallest p-value, largest effect estimate, most colorful figure, first table, or first result in the manuscript.

Do not automatically move sensitivity analyses, null results, supportive analyses, or replications to backup. An analysis that resolves a major inferential concern, explains another result, or closes an explicit research question can be main-deck evidence even when it is not primary in the statistical hierarchy.

## Slide-level synthesis rules

Plan around claims, not files or models.

- Prefer one integrated slide when multiple analyses support the same claim, side-by-side comparison improves interpretation, and the page remains legible at presentation distance.
- Do not split primary and sensitivity results merely because they were produced by separate models or workbooks.
- Do not merge analyses that form distinct narrative beats, such as an apparent contradiction followed by the analysis that resolves it, when keeping them separate improves comprehension.
- Use the principle `one main scientific job per slide`, not `one analysis per slide`.
- Keep method detail proportional to the evidence it is needed to interpret.

## Academic slide-title and wording rules

For conventional scientific presentations, separate the **scientific job of a slide** from its **visible title**. Claim-level planning may drive evidence selection internally, but visible academic slide titles should usually be short, neutral, and descriptive.

Prefer titles such as `Background`, `Study rationale`, `Study design`, `Study population`, `Statistical analysis`, `Primary results`, `Sensitivity analyses`, `Design 3: three-state analysis`, `Discussion`, `Strengths and limitations`, and `Conclusion`.

Do not default to keynote, consulting, marketing, or journalistic headline titles that state the interpretation before the audience sees the evidence, such as `Both trials were near null`, `The protective effect disappears`, or `Why our design is better`. Use a declarative claim title only when the user explicitly prefers headline-style slides or the talk format clearly calls for it.

Keep interpretation in the figure/table, concise caption, body text, spoken narrative, Discussion, or Conclusion. Never place planner-facing meta-language on slides, including phrases such as `the point is...`, `this slide proves...`, `for reproducibility rather than implementation`, `key selling point`, or instructions about what the presenter should emphasize.

For methods slides, describe what was done. For results slides, describe what was observed. Reserve causal or explanatory interpretation for Discussion unless the slide is explicitly an interpretation slide.

## Default presentation behavior

For a conventional single study, use this as the default grammar when appropriate:

`Scientific problem -> What is known -> Knowledge gap -> Aim -> Study design -> Population/exposure/comparator/outcome -> Statistical strategy -> Primary result -> Interpretation-critical secondary evidence -> Discussion -> Strengths/limitations -> Conclusion`

Keep Background selective. Keep Methods proportional to what the audience needs to interpret the evidence. Organize Results by scientific question and claim, not by table/figure numbering.

## Output

Use the user-facing format in `references/plan-mode.md`. Default to a readable plan rather than dumping internal schemas.

At minimum, make clear:

- what the study is actually asking;
- what source material is complete or missing;
- which external literature is needed or used;
- which results are core, interpretation-critical, supporting, backup, or omitted;
- what scientific and narrative role each important analysis serves;
- where apparently conflicting results arise and whether another analysis resolves them;
- what scientific claims the selected evidence supports;
- what each planned slide is for;
- which analyses should be combined on one slide versus separated for narrative reasons;
- for important quantitative result slides, what compact model/adjustment note should appear on-slide or in small text, when needed to interpret the estimate;
- what should be shown on-slide versus explained orally;
- where full model specification, covariate lists, coding choices, and other reproducibility detail belong in backup when relevant;
- when the plan will feed slide production, the actual slide-ready copy, exact numbers/labels, figure or table contents, model notes/caveats, must-preserve items, compressible items, source trace, and layout freedom needed by the builder.

## Handoff to slide production

Treat the handoff as a content contract, not a loose outline. For production-ready plans, the planner owns scientific content completeness and the slide-building skill owns layout/visual execution. Read `references/production-handoff.md`.

When the user approves the plan, preserve the approved:

- study model and primary estimand;
- scientific claims and claim strength;
- evidence priority and main/backup routing;
- analysis-role and conflict/resolution logic;
- external-literature provenance;
- narrative order and intentional repetitions;
- planned slide packing and figure/table treatment;
- visible slide copy and exact evidence values where specified;
- must-preserve versus compressible content;
- model notes, caveats, source trace, and protected sequencing.

A later slide-building workflow may re-layout, compress, or split a dense slide for readability, but it should not have to invent missing scientific content. It must not silently change the scientific hierarchy, conflict/resolution logic, estimand, reference group, protected evidence, or strength of the conclusion.
