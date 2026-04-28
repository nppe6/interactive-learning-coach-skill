# Learning Artifacts

Use this reference when the coaching session should leave behind durable material for review, continuation, or project practice.

## Document Persistence Policy

Create or update a Markdown document when:

- A course, open-source project, or large topic begins and needs a roadmap.
- A lesson explains a reusable concept.
- The learner completes a module, chapter, or source-code reading.
- The user asks to save notes, produce a study guide, or continue later.
- The session generates flashcards, quiz cards, a mistake log, or a review plan.
- A multi-session learning path needs progress tracking, return-session support, or second-pass review.
- A prerequisite concept blocks project learning and should be cached as a small reusable capsule.

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
learning-notes/react-learning-progress.md
learning-notes/threejs-scene-camera-renderer.md
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

## Progress File

- Progress record: `<topic>-progress.md`
- Resume rule: read the progress file first, then this roadmap row, then at most one linked lesson note.

## Learning Goal

<What the learner wants to be able to understand or build.>

## Assumed Starting Level

<Current level and known gaps.>

## Learner Baseline

- Overall level: <beginner / intermediate / advanced / unknown>
- Learning mode: <from scratch / guided project reading / exam review / migration build>
- Local references available: <notes, uploaded docs, bookmarks, prior capsules>
- Diagnostic status: <self-rated / quick-checked / unknown>

## Prerequisite Map

| Prerequisite | Needed For | Learner Level | Evidence | Preferred Source | Capsule Note | Trigger |
| --- | --- | --- | --- | --- | --- | --- |
| <concept> | <chapter/lesson> | zero/aware/familiar/practiced | <self-rate or check> | local/cached/official/model-stable | `<capsule>.md` | before <lesson> |

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

## Progress Link

- Progress record: `<topic>-progress.md`
- Current status lives in the progress file, not in this roadmap.

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

## Technology Translation Map

Use when the learner's goal includes migrating or reimplementing in another stack.

| Source Concept | Target Equivalent | Shared Responsibility | Caveat |
| --- | --- | --- | --- |
| <source> | <target> | <responsibility> | <not identical because...> |

## Concept Contrast Cards

| Pair | A Handles | B Handles | Confusion To Avoid | Project Example |
| --- | --- | --- | --- | --- |
| <A vs B> | <A role> | <B role> | <misconception> | <file/flow> |

## Dialogue-Derived Teaching Notes

- Learner answer or question: <what the learner said>
- Signal: <understood / partial / misconception / confusion / curiosity>
- Teaching adjustment: <how the next explanation should change>

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

## Progress Record Template

Use this as the default separate `<topic>-progress.md` file for every multi-session learning path. Keep volatile session state here instead of in the roadmap.

```markdown
# <Course, Project, or Topic> Progress

## Resume Snapshot

Keep this section short. Read it first when resuming. It is the primary low-token entry point.

- Current chapter: <chapter>
- Current lesson: <lesson>
- Last completed document: <path>
- Next resume point: <specific next step>
- Current weak spots: <short list>
- Prerequisite gaps: <short list>
- Prerequisite baseline: <zero/aware/familiar/practiced summary>
- Open next: <1-3 files/notes only>
- Recommended mode: <continue / review / repair / second pass / project>

## Current Position

<Optional detail if needed. Link out instead of duplicating full lesson notes.>

## Prerequisite Profile

| Concept | Level | Evidence | Source Preference | Capsule | Status |
| --- | --- | --- | --- | --- | --- |
| <concept> | zero/aware/familiar/practiced | <self-rate/check/dialogue> | local/cached/official/model-stable | `<capsule>.md` | needed/queued/done |

## Capsule Queue

| Capsule | Needed Before | Source To Use | Status |
| --- | --- | --- | --- |
| `<capsule>.md` | <lesson> | <local/cached/official/model-stable> | planned/done |

## Completed Lessons

| Lesson | Document | Evidence of Understanding | Weak Spots | Status |
| --- | --- | --- | --- | --- |
| <lesson> | <file> | <evidence> | <weak spots> | Complete/Needs review |

## Dialogue Signals

| Moment | Learner Signal | Interpretation | Follow-up |
| --- | --- | --- | --- |
| <question/answer> | <signal> | <what it means> | <repair or deepen> |

## Second-Pass Plan

- What to summarize first: <prior content>
- Foundations to re-teach: <basics>
- Gaps to repair: <weak spots>
- New examples to add: <examples>
- Deeper principles to add: <principles>
```

## Prerequisite Capsule Template

Use for just-in-time foundation concepts discovered during project learning. Keep it small and reusable.

```markdown
# <Prerequisite Concept>

## Learner Baseline

- Level for this concept: <zero / aware / familiar / practiced>
- Evidence: <self-rating, diagnostic answer, or prior dialogue>

## Why This Is Needed Now

<Project lesson or code path this unlocks.>

## Minimum Useful Idea

<The smallest explanation needed to continue.>

## Source

- Local/project source: <file or note>
- External/official source: <URL or title, if used>
- Source status: <local / cached / official / model-stable>
- Reuse decision: <reuse existing / create new / refresh from official docs>

## Project Connection

<How this concept appears in the current project.>

## Tiny Example

<Small example tied to the project.>

## Check Question

<One question to confirm readiness to return to the project.>

## Reuse Tags

- <topic>
- <project>
- <library/framework>
```

## Return Session Pattern

When the learner comes back, first open `<topic>-progress.md` and read only the Resume Snapshot. Open the roadmap row and one linked note only if needed, then choose a mode:

1. Continue: proceed from the next resume point.
2. Review: run recall questions from completed lessons.
3. Repair: re-teach weak spots detected from prior dialogue.
4. Second pass: summarize the old path, re-explain foundations, then add deeper examples.
5. Project: start or continue the practical task.

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

## Implementation Handoff Brief Template

Use when the learner chooses to start practice or implementation.

```markdown
# Practice Brief: <Task Name>

## Smallest Runnable Goal

<What should run by the end.>

## Out of Scope

- <What not to build yet>

## Contract First

- DTO / event / state shape: <contract>
- Success path: <expected events/output>
- Error/end behavior: <behavior>

## Checkpoints

1. <checkpoint and verification>
2. <checkpoint and verification>
3. <checkpoint and verification>

## Source-to-Target Mapping

| Original | Target | Note |
| --- | --- | --- |
| <source> | <target> | <caveat> |
```

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
