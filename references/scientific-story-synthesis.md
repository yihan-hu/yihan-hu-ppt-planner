# Scientific Story Synthesis

## Contents

1. When to use
2. Required synthesis outputs
3. Analysis-role map
4. Conflict and resolution map
5. Intended-conclusion stress test
6. Claim synthesis
7. Slide packing
8. Narrative pacing
9. Rebuilding after major feedback
10. Audit

## 1. When to use

Use this workflow before slide planning when one or more of the following are true:

- the project contains multiple study designs or estimands;
- a supportive or sensitivity analysis materially changes interpretation;
- the work includes replication, triangulation, decomposition, mediation, negative controls, or treatment-state analyses;
- important results appear discordant;
- the presentation aims to reconcile conflicting published evidence;
- the user has a desired conclusion that must be checked against the complete result set;
- the result folder contains many analyses whose scientific relationships are not obvious from filenames or table order.

Do not use this workflow to manufacture drama. Use it to expose the actual logical dependencies in the evidence.

## 2. Required synthesis outputs

Before drafting the storyboard, internally construct:

1. `study_map`: design, population, exposure/comparator, outcome, time zero, follow-up, estimand;
2. `analysis_role_map`: every important analysis and what scientific job it performs;
3. `conflict_map`: results that appear to disagree or answer different versions of the question;
4. `resolution_map`: analyses that explain, decompose, qualify, or reconcile those conflicts;
5. `claim_map`: the smallest set of defensible scientific claims that covers the important evidence;
6. `slide_packing_map`: which analyses belong together on one slide and which need separate narrative beats.

Do not expose these internal schemas verbatim unless the user asks. Use them to produce a clearer user-facing plan.

## 3. Analysis-role map

For each important analysis, record at least:

- analysis/design name;
- population;
- exposure/comparator or treatment-state contrast;
- outcome;
- estimand/effect measure;
- primary numerical result when available;
- evidence hierarchy;
- narrative role;
- relationship to other analyses;
- major inferential caveat.

Use two independent classifications.

### Evidence hierarchy

Choose the best fit:

- `primary`;
- `secondary`;
- `sensitivity`;
- `supportive`;
- `exploratory`.

### Narrative role

Choose one or more when useful:

- `establish`: establishes the main answer;
- `context`: supplies prerequisite evidence;
- `replicate`: reproduces a prior or internal signal;
- `challenge`: creates tension with the current interpretation;
- `decompose`: separates a composite exposure, outcome, population, or mechanism;
- `explain`: provides a plausible explanation for another result;
- `reconcile`: helps bring apparently conflicting evidence into a coherent interpretation;
- `robustness`: tests stability of a claim;
- `boundary`: shows where the claim does not generalize;
- `limitation`: reveals a material inferential weakness.

Do not infer narrative importance from evidence hierarchy alone. A supportive analysis may be the key explanatory result in the talk.

## 4. Conflict and resolution map

Explicitly search for apparent tensions such as:

- primary versus sensitivity result;
- treatment-initiation versus current-use result;
- between-person versus within-person result;
- active-comparator versus non-user comparator result;
- overall versus subgroup result;
- replication versus stronger-design result;
- on-treatment versus post-discontinuation result;
- relative versus absolute effect result;
- published result versus user's result.

For each tension, ask:

1. Do the analyses actually estimate the same causal/statistical quantity?
2. Do population, time zero, exposure definition, comparator, follow-up, outcome, or treatment-state definitions differ?
3. Is one analysis nested within, selected from, or conditioned on a post-baseline state of another?
4. Is there a later analysis that explicitly decomposes or tests the source of the difference?
5. Should the presentation preserve the apparent contradiction temporarily so the resolving analysis has a clear scientific purpose?

If no analysis resolves the tension, preserve it as uncertainty rather than forcing synthesis.

### Useful conflict-resolution pattern

A valid complex story may look like:

`Published signal -> stronger-design analysis near null -> literature-aligned replication reproduces signal -> decomposition identifies why the signal appears -> integrated interpretation`

The purpose is not drama. The purpose is to make the inferential logic visible.

## 5. Intended-conclusion stress test

When the user states a preferred conclusion, desired framing, or expected negative/positive finding, treat it as an intended take-home to test.

Ask:

- Which analyses directly support it?
- Which important analyses appear to contradict it?
- Are those analyses estimating the same quantity?
- Does another analysis explain or qualify the contradiction?
- What is the strongest wording supported by the full evidence?
- Which stronger wording would overclaim?

Never suppress a discordant analysis merely because it complicates the desired message.

Prefer distinctions such as:

- `no evidence of benefit` rather than `proved no benefit`;
- `association attenuated after decomposition` rather than `bias was proven`;
- `post-discontinuation periods had higher observed risk` rather than `discontinuation caused the outcome`, unless the design supports that causal claim.

## 6. Claim synthesis

Compress analyses into a small set of claims before allocating slides.

A good claim should:

- answer a scientific question;
- be supported by one or more analyses;
- use strength appropriate to the design;
- explain why the audience should care;
- remain valid when important sensitivity or discordant results are considered.

Do not create claims that are merely analysis labels such as `Sensitivity analysis` or `Design 3 result`.

For each claim, identify:

- main supporting evidence;
- interpretation-critical supporting evidence;
- contradictory evidence, if any;
- limitation or caveat that changes wording;
- whether the claim needs one slide or a short sequence.

## 7. Slide packing

Allocate slides at the claim level, then test whether the evidence fits legibly.

### Merge analyses on one slide when all are true

1. They serve the same scientific claim.
2. Direct comparison improves understanding.
3. They can share a semantic representation such as a forest plot, paired panels, timeline, or compact matrix.
4. Key labels and estimates remain readable at presentation distance.
5. The slide still has one main scientific job.

Examples:

- two primary analyses answering parallel populations can share one slide;
- main and horizon sensitivity estimates can share one forest plot;
- primary and alternative-comparator estimates can share one robustness slide;
- diagnostic summaries for two parallel target trials can share one methods/results slide if the same diagnostic threshold is being assessed.

### Keep analyses separate when any are true

- one result creates an apparent contradiction and the next resolves it;
- the audience must first understand one model before the next model has meaning;
- the analyses answer different scientific questions despite similar effect measures;
- combining them would hide an important change in estimand or population;
- the slide would require dense text or tiny labels to remain complete.

Use the rule:

`one main scientific job per slide, not one model per slide`

## 8. Narrative pacing

Do not reveal an explanatory result too early when doing so would make the preceding replication or contradiction scientifically purposeless.

When evidence supports it, use short sequences such as:

`Primary answer -> apparent contradiction -> explanatory analysis -> resolved interpretation`

or

`Replication -> decomposition -> reconciliation`

Separate these beats even if the numbers could technically fit on one slide, because the audience needs to update its mental model between steps.

Conversely, do not stretch routine robustness across multiple slides merely to create pacing.

## 9. Rebuilding after major feedback

User feedback is major when it changes any of the following:

- which analysis is primary or supportive;
- what an analysis was designed to accomplish;
- the estimand or exposure-state interpretation;
- the intended final conclusion;
- whether one result explains another;
- the relationship between studies/designs;
- the appropriate main-versus-backup routing.

After major feedback:

1. update the study and analysis-role maps;
2. rebuild conflict/resolution and claim maps;
3. re-run the slide-packing decisions;
4. regenerate one canonical storyboard from the beginning;
5. explicitly discard obsolete local sequencing decisions.

Do not keep patching slide numbers onto a story whose scientific logic has changed.

## 10. Audit

Before presenting the plan, check:

- Does every important analysis have a clear scientific and narrative role?
- Are supportive analyses allowed to be main-deck when they are interpretation-critical?
- Have apparent conflicts been distinguished from differences in estimand?
- Does a resolving analysis appear after the tension it resolves?
- Has the desired conclusion been stress-tested rather than assumed?
- Are same-claim analyses unnecessarily split across slides?
- Are distinct narrative beats inappropriately collapsed onto one page?
- Is the final wording no stronger than the strongest design supports?
- If the user changed the scientific framing, was the plan rebuilt rather than patched?
