# Learning Artifacts

Use this reference when the coaching session should leave behind durable material for review, continuation, or project practice.

## Document Persistence Policy

Create or update a Markdown document when:

- A course, open-source project, or large topic begins and needs a roadmap.
- A lesson explains a reusable concept.
- The learner completes a module, chapter, or source-code reading.
- The user asks to save notes, produce a study guide, or continue later.
- The session generates flashcards, quiz cards, a mistake log, or a review plan.

Do not create a document for a tiny one-off answer unless the user asks to save it.

Default folder: `learning-notes/`.

If the repository already has a better location such as `docs/study/`, `notes/`, `course-notes/`, or `learning/`, use that existing convention.

## Naming Rules

Name documents by course, module, source project, or knowledge point. Do not name only by date.

Preferred pattern:

```text
<course-or-source>-<module-or-topic>.md
```

Examples:

```text
learning-notes/react-learning-roadmap.md
learning-notes/react-hooks-useeffect.md
learning-notes/vue-source-code-roadmap.md
learning-notes/linear-algebra-eigenvalues.md
learning-notes/compiler-lexer-tokenization.md
learning-notes/open-source-project-auth-flow.md
learning-notes/django-orm-query-optimization.md
```

Use lowercase ASCII slugs for filenames unless the existing project uses another convention. Keep the title inside the document human-readable and in the learner's language.

## Roadmap Document Template

Create this before deep teaching begins for a course, open-source project, or large topic. The first version should be a bird's-eye plan, not a fully detailed textbook or architecture dump. Refine it as the learner progresses.

For codebase learning, inspect the repository tree and entry files before filling this template. If inspection is incomplete, mark claims as provisional.

Keep the roadmap learner-facing. It should help the learner know what will be learned, why it matters, which files or materials will be opened, how review will work, and what practical output will be built.

```markdown
# <Course, Project, or Topic> Learning Roadmap

## Learning Goal

<What the learner wants to be able to understand or build.>

## Assumed Starting Level

<Current level and known gaps.>

## Bird's-Eye Overview

<Short overview in the learner's language. Explain the product/problem first, then the major moving parts. Avoid low-level implementation details until chapter notes.>

## Source Inspection

- Entry points inspected: <files or materials>
- Important areas to inspect later: <files or modules>
- Provisional assumptions: <claims that still need verification>

## Learning Route

| Chapter | Learner Outcome | Materials / Files | Key Ideas | Review Focus | Practice / Project Point | Status |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | <what the learner can explain/do> | <files/materials> | <2-4 ideas> | <review> | <practice> | Planned |
| 2 | <what the learner can explain/do> | <files/materials> | <2-4 ideas> | <review> | <practice> | Planned |

## Chapter Plan

### Chapter 1: <Name>

- Why it matters: <reason>
- Minimal mental model: <one sentence>
- Learn: <concepts>
- Read or inspect: <files/materials>
- Watch for: <common mistakes>
- First walkthrough: <one concrete flow/example before quiz>
- Practice: <exercise or mini task>
- Review: <recall or transfer task>
- Translation track: <how this maps to the target stack, if applicable>
- Document: `<future-topic-note>.md`

## Project Ladder

- Guided drill: <small task close to lesson examples>
- Mini project: <transfer task after several chapters>
- Capstone: <module-level practical project>

## Review Queue

| Topic | Next Review | Weak Spot | Status |
| --- | --- | --- | --- |
| <Topic> | <Date or relative day> | <Weak spot> | Planned |

## Open Questions

- <Question to resolve as the learner goes deeper>
```

For open-source projects, adapt the learning route to code-reading layers. Keep the first pass shallow and defer deep details to chapter notes:

1. Product purpose and user flow.
2. Repository structure and build/run path.
3. Architecture and major modules.
4. Data model or state flow.
5. One important feature end to end.
6. Testing and debugging strategy.
7. Extension task.
8. Capstone rebuild or plugin feature.

## Lesson Document Template

```markdown
# <Human-readable lesson title>

## Learning Goal

<What the learner should be able to understand or do.>

## Prerequisites

- <Prerequisite>

## Core Ideas

1. <Idea>
2. <Idea>
3. <Idea>

## Four-Step Lesson Design

### STEP 1: Mental Interface

- Preconception probe: <What the learner may currently believe>
- Cognitive conflict: <Example where that belief is incomplete or fails>
- Real need: <Why this concept matters in problems, projects, or real use>

### STEP 2: Minimum Viable Understanding

- If you remember one thing: <Core non-negotiable idea>
- Core metaphor: <Metaphor or anchor example>
- Knowledge-map position: <Prerequisite -> current concept -> next concept>

### STEP 3: Practice Ladder

- Common blocker 1: <blocker>
  Preventive exercise: <exercise>
- Common blocker 2: <blocker>
  Preventive exercise: <exercise>
- Common blocker 3: <blocker>
  Preventive exercise: <exercise>
- Variations:
  1. <variation>
  2. <variation>
  3. <variation>
  4. <variation>
  5. <variation>

### STEP 4: Transfer Bridge

- Transfer path: <How to move from this example to this class of problems>
- Similar but different contrast case: <case>
- Combined old-knowledge challenge: <problem>

## Explanation

<Concise explanation with examples.>

## Worked Example

<Example and reasoning path.>

## Common Misunderstandings

- Misunderstanding: <incorrect idea>
  Correction: <correct idea>

## Quiz Cards

1. Question: <stem>
   A. <option>
   B. <option>
   C. <option>
   Answer: <answer>
   Why: <brief explanation>

## Flashcards

1. Q: <atomic question>
   A: <short answer>

## Review Plan

- Now: <recall check>
- Day 1: <review task>
- Day 3: <transfer task>
- Day 7: <mixed practice>
- Day 14-30: <mastery check>

## Next Practice

<Small next task.>
```

## Module Index Template

Use an index when a learning path has multiple documents.

```markdown
# <Course or module name>

## Current Goal

<Goal>

## Learning Path

1. [<Topic 1>](<topic-1>.md)
2. [<Topic 2>](<topic-2>.md)

## Review Queue

| Topic | Next Review | Weak Spot | Status |
| --- | --- | --- | --- |
| <Topic> | <Date or relative day> | <Weak spot> | <Learning/Reviewing/Mastered> |

## Project Ladder

- Guided drill: <task>
- Mini project: <task>
- Capstone: <task>
```

## Review Session Pattern

When a learner returns to review, start with recall before explanation:

```text
Let's review <topic>. First, try these without looking:
1. <recall question>
2. <application question>
3. <mistake repair question>
```

Then:

- Mark strong concepts.
- Identify weak concepts.
- Re-teach only the weak concept.
- Add one transfer question.
- Update the review queue.

## Project Generation Pattern

Create practical projects from course examples, exercises, or open-source code by preserving the learning objective and changing the surface context.

```markdown
# Practice Project: <Project Name>

## Source Pattern

<Course example, codebase pattern, or concept this project is based on.>

## Learning Objective

<What this project proves the learner can do.>

## Requirements

1. <Requirement>
2. <Requirement>
3. <Requirement>

## Constraints

- <Constraint that keeps the task focused>

## Checkpoints

1. <Small milestone>
2. <Small milestone>
3. <Small milestone>

## Extension Tasks

- <Optional stretch>

## Rubric

| Criterion | Good Evidence |
| --- | --- |
| Correctness | <Evidence> |
| Understanding | <Evidence> |
| Transfer | <Evidence> |
```

## Project Levels

- Guided drill: close to the original example; useful immediately after teaching.
- Mini project: same pattern in a different scenario; useful after several related lessons.
- Capstone project: combines multiple module ideas; useful after a large module.
