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

Sample representative notes from:

- one background or motivation slide;
- one methods or technical explanation slide;
- one results, discussion, or wrap-up slide.

Infer and preserve the speaker's explanatory behavior, not just vocabulary:

- sentence length;
- frequency of `we`;
- preferred connectors;
- amount of numerical detail;
- directness versus polish;
- whether the speaker naturally says `so`, `now`, `first`, `then`, `next`, `however`, `we can see`, or similar phrases;
- whether complex reasoning is explained step by step rather than compressed into a polished summary.

Correct grammar when it affects clarity or professionalism, but do not automatically rewrite the speaker into highly polished native-speaker rhetoric.

## Yihan-style explanatory anchor when a similar deck is provided

When the user provides a deck with speaker notes similar to the `Statistics in observational studies` style, preserve this speaking pattern:

- start sections with a simple question, for example `So let's start with...` or `Now let's talk about...`;
- introduce examples before definitions when teaching a concept;
- use short spoken sentences;
- move one reasoning step at a time;
- use explicit navigation such as `First`, `Second`, `Third`, `Now`, `Then`, `However`, and `So`;
- orient the audience before giving numbers, formulas, or a table;
- repeat the same technical noun when needed instead of forcing synonym variation;
- explain derivations sequentially, for example `Now let's calculate...`, `If we take the ratio...`, `So the key point is...`;
- keep slide text concise and let the notes carry the reasoning chain.

This style is clear, direct, and researcher-like. Do not replace it with consulting, keynote, or manuscript prose.

Prefer:

> So at first, the solution looks very simple. If these instructions are important, why don't we just put everything into SKILL.md? But then we get another problem. The file becomes very long. The model can technically see all the instructions, but that does not mean every instruction gets the same attention. So the key point is: more context does not automatically mean more attention.

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

Keep one or two ideas per sentence. Use abstract terms such as `estimand`, `framework`, `triangulation`, `coherence`, `invariant`, or `lifecycle` only when the talk genuinely needs them, and define them from an example first when the audience is unfamiliar.

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

## Slide text and notes must complement each other

Do not turn the notes into a spoken copy of the slide.

The slide should carry what the audience needs to see, compare, or remember. The notes should carry:

- rationale;
- interpretation;
- selected numerical emphasis;
- caveats;
- transitions that help the audience follow the scientific logic.

If a table contains ten rows, the notes may mention only two or three.

## Handoff rule to slide-building workflows

When the planner produces approved `speaker_notes`, treat them as part of the scientific content contract.

A slide-building skill may:

- insert the notes into the PPTX;
- make minor grammatical or mechanical corrections if explicitly allowed;
- preserve sources/notes formatting required by PowerPoint.

A slide-building skill should not:

- rewrite the scientific scope;
- change the relationship between designs;
- add a new explanation for discordant results;
- weaken an intentional tension by saying results are incomparable because estimands differ;
- strengthen the causal interpretation;
- replace the user's speaking style with generic polished prose.

If slide order or scientific content changes materially during production, return to the canonical planner story and regenerate the affected notes.

## Quality check

Before delivery, ask:

- Does every note preserve the approved scientific role of the slide?
- Could the speaker plausibly say the sentences aloud without sounding as if they are reading a paper?
- Do methods sound procedural, results observational, and discussion interpretive?
- For teaching talks, does each major concept emerge from an example or problem before it is abstractly named?
- Are important cross-design inconsistencies addressed rather than dismissed?
- Did the note avoid reading every visible bullet or figure row?
- Did the note preserve the user's own academic speaking register when a style example was provided?