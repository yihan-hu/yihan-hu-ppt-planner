# Example-first Teaching and Concept Development

Use this reference for teaching, methodological, conceptual, tutorial, journal-club, onboarding, or group-meeting presentations where the audience may not already know the vocabulary.

## Core principle

Do not introduce an abstract concept merely because it is logically prior. When possible, first show a concrete case where the audience can see the problem, contradiction, or need for the concept. Then name the concept that resolves it.

Preferred sequence:

`example -> observation -> question -> concept -> mechanism -> general rule -> next example/application`

This is especially useful when the concept is unfamiliar, such as confounding, interaction, odds ratio, metadata boundaries, progressive disclosure, state machine, or lifecycle management.

## Case fidelity rule

A case is not a label. A useful teaching case must preserve enough concrete sequence for the audience to experience the problem.

Do not replace a case with a summary such as:

- `Prompt gets too long`;
- `GPT over-engineers`;
- `Every bug becomes a rule`;
- `More control is not always better`.

Instead, plan the story beat explicitly:

1. What was the original task?
2. What did the user/model try first?
3. What exactly failed?
4. What patch or attempted solution followed?
5. What new problem did that create?
6. What reframing or better solution resolved it?
7. Only then, what concept or general rule should be named?

If these steps are the point of the slide, mark them as a protected sequence in the production handoff. The slide builder may split the sequence across slides, but must not compress it into an abstract label, slogan, or decorative pipeline.

## Planning behavior

For each major concept, ask:

- Can the audience experience the problem before I name the solution?
- Is there a small example, table, code snippet, diagram, failure case, or numerical toy example that makes the concept necessary?
- What should feel surprising, wrong, or incomplete before the concept is introduced?
- What is the smallest definition needed after the example?
- What general rule should the audience remember?
- Which concrete steps of the example must remain visible or spoken in order, rather than being replaced by a takeaway?

Do not default to `definition -> theory -> example` unless the audience already knows the field or the concept is only a minor prerequisite.

## Slide sequencing patterns

### Pattern A: simple conceptual teaching

Use:

1. concrete example;
2. observed pattern or contradiction;
3. question: why does this happen?;
4. concept name and short definition;
5. diagram/mechanism;
6. general rule.

Example structure:

`Ice cream sales and drowning are correlated -> heat explains both -> this is confounding -> a confounder is a common cause of exposure and outcome.`

### Pattern B: technical derivation

Use:

1. start from a concrete numerical table or familiar model;
2. calculate the quantity the audience already understands;
3. change the design or sampling process;
4. show what breaks;
5. introduce the estimator or concept that still works;
6. then give the formula.

Example structure:

`Full population 2x2 table -> risk ratio works -> case-control sampling changes denominators -> risk cannot be estimated -> odds ratio remains stable -> use OR in case-control studies.`

### Pattern C: agent or workflow concepts

Use:

1. show the naive workflow;
2. show a realistic failure;
3. show why the obvious fix is incomplete;
4. introduce the engineering concept;
5. state the rule.

Example structure:

`Put all instructions in SKILL.md -> the file becomes huge -> the critical rule loses salience -> progressive disclosure -> but references are passive -> activation conditions are needed.`

### Pattern D: failure-case driven skill design

Use when the point is an agent/skill design lesson learned from practice:

1. show the actual task or request;
2. show the first natural prompt or skill instruction;
3. show the concrete bad output or repeated behavior;
4. show the first patch;
5. show how patching starts to accumulate;
6. show the heavier architecture that looks tempting;
7. ask what problem actually needs to be solved;
8. show the smaller semantic instruction or boundary rule;
9. name the design principle.

Example structure:

`Skill repeats a completed step -> add one rule -> edge case remains -> GPT proposes state machine/validator/retry/fallback -> architecture becomes heavy -> real need is to check whether the step is already complete -> one semantic instruction may be enough.`

## On-slide style

Keep visible slide text simple and mostly descriptive. The slide should show the example, contrast, table, diagram, or failure. The concept name can appear only after the problem is visible.

Prefer titles such as:

- `A simple example`
- `What goes wrong?`
- `Why this matters`
- `Now we can define...`
- `The general rule`
- `A repeated-step problem`
- `A more engineered solution`
- `Another solution`

Avoid starting a beginner-facing section with titles such as:

- `Definition of progressive disclosure`
- `Formal lifecycle semantics`
- `Theoretical motivation`
- `More control is not always better`
- `A paradigm shift in agent design`

unless the audience already needs that level of abstraction.

## Speaker-note behavior

When notes are requested, write the spoken explanation as a reasoning path. Use short steps:

- start with a simple question;
- orient the audience to the example;
- state what they should notice;
- ask what this implies;
- then introduce the concept;
- end with the key point.

Good spoken pattern:

> So at first, the solution looks very simple. If these instructions are important, why don't we just put everything into SKILL.md? But then we get another problem. The file becomes very long. The model can technically see all the instructions, but that does not mean every instruction gets the same attention. So the key point is: more context does not automatically mean more attention.

Avoid replacing the step-by-step explanation with polished summary language such as:

> This illustrates a fundamental limitation of monolithic instruction architectures.

That sentence may be technically correct, but it does not teach the concept in the user's preferred explanatory style.
