# Story Synthesis Before Slides

Use this reference before building a slide-by-slide storyboard. Its purpose is to prevent a presentation from becoming a sequence of individually reasonable slides that do not form a coherent argument.

The required order is:

`content synthesis -> story synthesis -> story closure -> slide planning`

Do not draft slide numbers, titles, or page layouts until story closure passes.

## 1. Lightweight presentation state

Maintain a compact planning state from the conversation and source material. Keep only decisions that matter for story construction:

- `core_question`: the question the talk is trying to answer;
- `audience_state_start`: what the audience is assumed to know at the beginning;
- `desired_end_state`: what the audience should understand, believe, or be able to do by the end;
- `domain_constraints`: boundaries that materially shape the story;
- `canonical_examples`: examples or failure cases that should anchor the explanation;
- `locked_decisions`: user decisions that should not be silently reopened;
- `backup_or_rejected_topics`: useful material intentionally kept off the main path;
- `style_source`: prior deck, notes, or oral register to match;
- `open_questions`: unresolved choices that could materially change the story.

This state is not a user-facing schema. It is a control surface for planning.

## 2. Content synthesis

Before choosing a story, inventory the important content without assigning slides.

Possible content units include:

- scientific claims or results;
- concepts and definitions;
- failure cases;
- examples;
- mechanisms;
- methods or design choices;
- constraints or boundaries;
- competing explanations;
- checks, caveats, or limitations;
- optional background topics.

For each unit, record why it might matter. Do not assume that because two units share a topic they belong next to each other in the story.

## 3. Story synthesis

Convert the content inventory into a small number of story beats before thinking about slides.

For each proposed beat, determine:

- `answers`: what question or problem from the previous beat this resolves;
- `requires`: what the audience must already understand for this beat to make sense;
- `job`: what this beat contributes to the overall argument;
- `audience_after`: what the audience should understand after this beat;
- `creates`: what question, tension, or need should naturally lead to the next beat.

A strong sequence has a clear handoff:

`beat A creates -> beat B answers`

If the handoff is weak, reorder, merge, remove, or add the missing bridge before planning slides.

## 4. Prefer strong logical relations

Distinguish three kinds of adjacency:

### Knowledge prerequisite

B cannot be understood correctly until A is established.

Example:

`what a confounder is -> how adjustment targets confounding`

### Question-driven relation

A creates a problem or question that B naturally answers.

Example:

`prompt explicitly says "use previous code" but the model invents a variable -> why context presence does not guarantee reliable use -> staged workflow`

### Thematic relation

A and B are both about the same broad topic.

Example:

`Agent Skills -> ReAct -> context windows -> lifecycle`

Thematic relation alone is not sufficient justification for sequence. Use knowledge-prerequisite or question-driven relations for the main path whenever possible.

## 5. Audience-state reasoning

Track what the audience has actually been given enough reason to accept.

Before introducing a concept, ask:

1. What does this concept depend on?
2. Has the audience already seen the problem, evidence, or prerequisite that makes it necessary?
3. If not, would they reasonably ask "why not just do X instead?"

If an obvious alternative has not been addressed, the concept is premature.

Example:

Do not introduce `Plan -> Execute` as a solution before the audience has seen why a direct prompt can still miss explicit instructions. Otherwise the audience can reasonably ask: `Why not just put those steps in the prompt?`

## 6. Concept admission gate

Do not add a concept to the main deck merely because it is relevant or interesting.

Classify each candidate as:

- `required`: the story cannot make its central argument without it;
- `supporting`: helps explain or justify a required beat but need not become its own section;
- `backup`: useful for questions or depth, but interrupts the main argument;
- `omit`: not needed for this talk.

For every main-deck concept, be able to answer:

`What problem in the current story does this concept solve?`

If there is no specific answer, keep it supporting, backup, or omit it.

## 7. Top-level story architecture

Compress the talk into roughly 3-5 sections before slide planning.

A good section architecture answers distinct audience questions rather than grouping material by vocabulary.

Examples:

Teaching:

`What is it? -> Why is it needed? -> How does it work? -> How should we use/design it?`

Scientific study:

`What is the problem? -> What did we do? -> What did we observe? -> Why should we believe it? -> What does it mean?`

Do not proceed if the talk still needs a long list of peer-level topics to describe its structure.

## 8. Story closure check

Before generating a slide list, require all of the following:

1. **Core question**: the talk has one clear central question or teaching objective.
2. **Section closure**: the talk can be summarized in 3-5 major sections with distinct jobs.
3. **Beat necessity**: each main beat is required by the argument, not merely topically relevant.
4. **Audience readiness**: each major concept appears only after its prerequisites or motivating problem are established.
5. **Transition closure**: each major transition has a defensible `creates -> answers` relation.
6. **Alternative closure**: obvious audience objections such as `why not just...` are addressed before the proposed solution is introduced.
7. **Ending closure**: the final take-home directly answers the opening question.

If any item fails, revise the story model. Do not patch the problem at the slide-title level.

## 9. Storyboard comes after closure

Only after story closure passes should the planner decide:

- how many slides each beat needs;
- which beats should be combined or separated;
- visible titles;
- figures, examples, tables, or code artifacts;
- speaker notes;
- main versus backup placement.

One beat may take several slides, and several closely related beats may fit on one slide. Slide count is a realization decision, not the story model itself.

## 10. Replan gate for later feedback

When the user gives feedback, classify the change before editing the storyboard.

### Local edit

Examples: wording, visual density, title phrasing, one statistic, one example detail.

Action: patch the affected slide or note.

### Beat-level change

Examples: an example is wrong, a concept needs a different explanation, two adjacent beats should merge.

Action: rebuild the affected beat and its incoming/outgoing transitions.

### Story-model change

Examples: a domain constraint changes; a concept belongs to a different section; the audience's prior knowledge was wrong; the user says the overall flow is wrong.

Action: return to content/story synthesis and re-run story closure before changing slide order. Do not keep patching an obsolete storyboard.

## 11. Minimal user-facing summary

Do not expose the internal beat schema unless useful. In the user-facing plan, summarize:

- the top-level section logic;
- the question each section answers;
- the main example/evidence driving each section;
- the resulting slide-by-slide storyboard after closure.

The internal structure should improve coherence without making the planning output feel bureaucratic.
