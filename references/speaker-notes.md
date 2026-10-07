# Speaker Notes Planning and Drafting

Use this reference when the presentation plan should include a spoken narrative or full speaker notes, especially for academic research talks, lab meetings, defenses, journal clubs, epidemiology, biostatistics, clinical methods, and AI/agent-methodology talks.

The planner owns both the **scientific story** and the **spoken interpretation**. Speaker notes must be written from the approved slide order, analysis-role map, conflict/resolution logic, and conclusion strength. Do not let a late note-writing pass invent a new story.

## Two levels of spoken output

### `spoken_narrative`

Use for an early or reviewable plan. Keep it to 1-3 bullets or a short paragraph describing what the presenter should explain orally.

### `speaker_notes`

Use for a production-ready plan, a direct handoff to a slide-building workflow, or whenever the user asks for a script/notes. Write the actual spoken draft for each main slide.

If the user intends to move directly into slide production, default to full `speaker_notes` unless they explicitly ask for planning only.

Do not duplicate both fields at full length. If `speaker_notes` is present, omit `spoken_narrative` or reduce it to a one-line intent.

## Lock scope before drafting notes

Before writing notes, confirm from the canonical plan:

- the broad question or teaching objective;
- the role of each slide;
- which examples introduce concepts and which slides define or generalize them;
- which analyses or examples are primary, diagnostic, supportive, or backup;
- which apparent conflicts should remain visible;
- which later slides explain, qualify, or resolve those conflicts;
- the strongest conclusion supported by the full evidence.

If the user changes the scientific framing, teaching sequence, conclusion, or audience level, rebuild the canonical plan first and then rewrite notes from that updated plan.

## Match the user's own speaking style when available

If the user provides an old deck, transcript, script, or speaker notes, treat it as the primary style reference.

Sample representative material from:

- one background or motivation slide;
- one methods or technical explanation slide;
- one results, discussion, or wrap-up slide.

Infer and preserve explanatory behavior, not just vocabulary:

- sentence length;
- average ideas per sentence;
- preferred connectors;
- amount of numerical detail;
- directness versus polish;
- whether slide wording is repeated directly;
- how much presentation-management language is used;
- whether complex reasoning is explained one step at a time;
- how much abstraction is introduced before an example.

Correct grammar when it affects clarity or professionalism, but do not rewrite the speaker into polished keynote, consulting, or manuscript prose.

## Draft beats before slides

Do not independently write a self-contained mini-script for every slide.

For any multi-slide teaching or reasoning beat:

1. Write the whole spoken passage as one continuous explanation.
2. Identify where the visual slide changes naturally.
3. Split the passage across the slide notes.
4. Keep the unresolved question at the end of one slide when the next slide answers it.
5. Only summarize at the end of the beat when a summary is genuinely useful.

A middle slide usually does **not** need its own introduction, explanation, and takeaway.

Before accepting a slide boundary, ask:

- What has the audience just heard?
- What remains unresolved?
- Does the next sentence directly continue that reasoning?
- Am I restarting the topic only because the slide changed?

## Semantic granularity

Do not calibrate style only by word count.

A note may be long when it contains a real derivation, example, calculation, definition, or sequence of reasoning. A short note may still feel verbose if several sentences only frame, qualify, recap, or manage the presentation.

Prefer sentences that add at least one of:

- a factual detail;
- an example;
- a calculation or reasoning step;
- a definition;
- a causal or logical relation;
- a necessary caveat;
- a direct transition to the next unresolved point.

Minimize sentences whose only job is to announce structure, such as `The question is...`, `The main point is...`, `What matters here is...`, or `This slide shows...`.

For a simple conceptual slide, a useful default is one short transition plus 2-4 content sentences. Expand only when the content itself needs more explanation.

## Directly speakable language

Speaker notes must sound like sentences the researcher could say aloud without translating them mentally.

Do not narrate the presentation as an object. Avoid stage-direction language such as:

- `It says...`
- `On the slide...`
- `The phrase here is...`
- `The box on the left shows...`
- `As you can see from this slide...`

Prefer the content itself:

> Suppose I ask the Agent to add a sensitivity analysis.

It is fine to orient the audience to a figure, table, or code region when location matters, for example `Look at the upper rows first` or `In the previous code, the object is eligible_cohort`.

## Avoid forced framing and forced closure

Do not use a repeated formula in which every slide starts with a thesis sentence and ends with a takeaway sentence.

Use these patterns sparingly, not as default templates:

- `The main point is...`
- `The key point is...`
- `The question is...`
- `A natural reaction is...`
- `What matters here is...`
- `This slide answers...`
- `The main takeaway is...`

Also avoid defensive `not X, but Y` constructions unless there is a real misconception to correct.

## Do not invent rhetorical causality

A smooth transition is not enough; the conceptual relation must be true.

Do not write language that makes mechanism B sound like the solution to failure A unless it actually is.

For example:

- buried or overloaded context -> context design / activation;
- genuinely multi-step work -> staged workflow / plan-execute;
- ignored mechanically checkable rule -> gate;
- earlier PASS invalidated by later change -> lifecycle / freshness.

If the next slide introduces a separate problem, say so simply.

## Yihan-style explanatory anchor when a similar deck is provided

When the user provides a deck with notes similar to the `Statistics in observational studies` style, preserve this speaking pattern:

- use short spoken sentences;
- move one reasoning step at a time;
- introduce examples before formal definitions when teaching an unfamiliar concept;
- use simple connectors such as `So`, `Now`, `First`, `Then`, and `However` only when they sound natural;
- orient the audience before a formula, table, or code comparison;
- repeat the same technical noun when needed instead of forcing synonym variation;
- keep the language close to the visible slide text when that helps the audience follow;
- allow a slide to end without a recap when the next slide continues the same beat.

This style is direct and researcher-like. Do not replace it with consulting, keynote, or manuscript prose.

Prefer a continuous two-slide beat such as:

> The prompt already says to use the previous code and not invent variable names. In the previous block, the object is eligible_cohort. But the next block switches to cohort_df.
>
> Why can this still happen? The model is following the task, the previous code, and several instructions at the same time. Adding more instructions makes the prompt longer, but the important rule can still be buried.

Avoid:

> This illustrates a fundamental limitation of monolithic instruction architectures and motivates context-aware routing.

## Default oral register

Aim for researcher oral English: clear, direct, technically correct, and easy to say aloud.

Prefer:

- `We used...`
- `We included...`
- `We compared...`
- `First...`
- `Then...`
- `Next...`
- `After that...`
- `We can see...`
- `The estimate is around...`
- `We observed...`
- `So this suggests...`

Keep one or two ideas per sentence. Use abstract terms such as `estimand`, `framework`, `triangulation`, `coherence`, `invariant`, `runtime`, `gate`, or `lifecycle` only when the talk genuinely needs them.

For an unfamiliar term, show the concrete problem, action, or process first when possible, then name the concept. A term should earn its name.

Avoid unnecessary manuscript-style upgrades such as:

- `Taken together, these findings provide compelling evidence...`
- `This pattern underscores the importance of...`
- `Within this framework, the analyses provide a coherent triangulation...`
- `These results should be interpreted through the lens of...`

## Slide-role rules

### Title

Use 1-2 simple sentences to introduce the topic. Do not preload background, methods, or conclusions.

### Background / motivation

Explain what is known, what remains unclear, and why the question matters. When teaching, start from an example or a simple question when possible.

### Concept introduction

Use the pattern from `references/example-first-teaching.md`: example -> observation -> question -> concept -> mechanism -> general rule. Do not begin with a formal definition if the audience can first experience the need for the concept.

### Methods / design

Explain what was done in sequence and why the important design choices matter. Procedural narration is usually natural:

> We first identified every eligible visit. Each visit could start a new trial. Then we assigned the treatment strategies and allowed the grace period.

Do not read every inclusion criterion aloud unless it is central to the design.

### Statistical analysis

Name the model or estimator and explain its purpose in plain academic language. Distinguish direct covariate adjustment from weighting, matching, or standardization when that affects interpretation.

### Results figure

Use a simple three-step pattern:

1. Orient the audience to the relevant part of the figure.
2. Mention only the key values.
3. State the observed pattern.

Example:

> If you look at the upper rows first, the estimates are very close to one. At five years the hazard ratio is about 1.0. So we do not see a clear increase or decrease in risk in this analysis.

Do not narrate every row.

### Sensitivity / decomposition / diagnostic analysis

Say why the analysis was done, what changed, and what that means for the previous interpretation.

Prefer direct wording such as:

- `we split the non-use period`;
- `current use moved close to one`;
- `risk was higher after discontinuation`;
- `the result was not stable across all time horizons`.

### Discussion / synthesis

Put the analyses together in broad scientific terms. Compare directions across designs when they speak to the same drug/outcome question, while acknowledging why exact effect sizes may differ.

Do not use `different estimands` as a default escape from discordance. If the broad pattern is inconsistent, say that and explain what evidence may account for it.

### Conclusion

Give the smallest set of take-home points supported by the study or teaching sequence. Do not re-read all prior estimates or repeat every prior concept.

## Calibration and causality

Use calibrated wording:

- `is consistent with`;
- `suggests`;
- `may contribute to`;
- `higher observed risk`;
- `the estimate was close to one`;
- `we should be cautious`.

Avoid unsupported wording:

- `proves`;
- `caused`;
- `explains everything`;
- `demonstrates conclusively`;
- `false protective effect`.

For post-discontinuation or treatment-state analyses, distinguish an observed association from the causal effect of stopping treatment unless the design supports that causal interpretation.

## Lexical alignment with slide text

Use the same important nouns, labels, variables, and comparison terms that appear on the slide.

If the slide compares `eligible_cohort` with `cohort_df`, the notes should normally say those names directly. Do not replace clear visible terms with a second layer of abstraction unless the abstraction is itself being taught.

When visible slide copy is already clear and speakable, reading it directly or closely paraphrasing it is often better than inventing another formulation.

This does **not** mean reading every visible bullet or table row. Repeat what helps the audience track the explanation; omit what they can read without help.

## Slide text and notes should work together

Do not mechanically read every visible word. But also do not paraphrase clear slide text just to make the notes sound different.

The slide should carry what the audience needs to see, compare, or remember. The notes should add only what helps the audience understand the reasoning:

- rationale;
- sequence;
- selected numerical emphasis;
- interpretation;
- caveats;
- a necessary transition.

If a table contains ten rows, the notes may mention only two or three. If a slide contains one clear definition and three criteria, the notes may simply read or closely paraphrase those criteria and add a short explanation.

## Planner language is not automatically speaker language

Internal planning aphorisms, labels, and compression devices should not automatically become audience-facing notes.

Examples that may be useful internally but can be too abstract for beginners include:

- `Use machinery for invariants; use judgment for judgment.`
- `Mutation invalidates evidence.`
- `More context != more attention.`
- `Complexity should be earned.`

Translate them into concrete speech unless the audience already understands the abstraction. For example:

> Use hard checks for things that can be verified exactly. Use model or human review for things that require interpretation.

or:

> The code changed after the review passed, so the old PASS may no longer apply.

## Handoff rule to slide-building workflows

When the planner produces approved `speaker_notes`, treat them as part of the scientific content contract.

A slide-building skill may:

- insert the notes into the PPTX;
- make minor grammatical or mechanical corrections if explicitly allowed;
- preserve sources/notes formatting required by PowerPoint.

A slide-building skill should not:

- rewrite the scientific scope;
- change the relationship between designs or mechanisms;
- add a new explanation for discordant results;
- invent a causal link between adjacent teaching beats;
- strengthen the causal interpretation;
- replace the user's speaking style with generic polished prose.

If slide order or scientific content changes materially during production, return to the canonical planner story and regenerate the affected notes.

## Speaker Language and Granularity Audit

Before delivery, ask all of the following:

1. **Directly speakable**: Could the speaker say every sentence naturally, or does any line describe the slide rather than the subject?
2. **Continuous across slides**: Were multi-slide beats drafted as continuous speech, or does every slide restart with a new mini-introduction?
3. **No forced framing/closure**: Are there repeated `main point`, `key point`, `question is`, `natural reaction`, or unnecessary `not X, but Y` constructions?
4. **High semantic density**: Does each sentence advance content, reasoning, evidence, or interpretation rather than merely manage the presentation?
5. **Lexically aligned**: Do the notes use the same important terms, labels, values, and object names the audience sees?
6. **Concrete before abstract**: Does an unfamiliar technical term appear only after the audience has seen the example, action, or problem it names?
7. **True transition logic**: Does every causal-sounding transition reflect a real conceptual relation rather than rhetorical smoothness?
8. **Appropriate repetition**: Are clear slide phrases repeated when useful, while unnecessary full-slide reading is avoided?
9. **Style fidelity**: Does the note preserve the user's own academic speaking register and semantic granularity when a style example was provided?
10. **Scientific fidelity**: Do methods sound procedural, results observational, discussion interpretive, and causal claims calibrated?

## Quality check

Before delivery, ask:

- Does every note preserve the approved scientific role of the slide?
- Could the speaker plausibly say the sentences aloud without sounding as if they are reading a paper?
- Do methods sound procedural, results observational, and discussion interpretive?
- For teaching talks, does each major concept emerge from an example or problem before it is abstractly named?
- Are important cross-design inconsistencies addressed rather than dismissed?
- Did the note avoid reading every visible bullet or figure row?
- Did the note preserve the user's own academic speaking register when a style example was provided?