# Session Patterns

Use these patterns when running an interactive learning session.

## Intake Pattern

Ask only what is needed:

```text
Before we start, tell me:
1. What topic or problem are you working on?
2. What level should I assume?
3. Are you learning for homework, an exam, work, or curiosity?
```

If the user already provided enough context, skip intake and begin.

## First Turn Pattern

```text
I'll start from <assumed level> and aim for <goal>.

Path:
1. <step>
2. <step>
3. <step>

Quick check: <diagnostic question>
```

## Bird's-Eye Roadmap Pattern

Use before deep teaching begins for a course, open-source project, or large topic. If source files are available, inspect the repository tree and entry files before producing this. Keep it as a learner-facing plan, not an architecture dump:

```text
Before we enter the first lesson, here is the bird's-eye learning plan.

Goal: <goal>
Assumed level: <level>

Source inspection:
- I checked: <files/materials>
- Still provisional: <assumptions to verify later>

Route:
1. <chapter> - <learner outcome> - read <files/materials> - build/review <practice>
2. <chapter> - <learner outcome> - read <files/materials> - build/review <practice>
3. <chapter> - <learner outcome> - read <files/materials> - build/review <practice>

For each chapter, I will gradually add:
- Detailed lesson notes
- Quiz cards and flashcards
- Review points
- Practice or project tasks

I will save the roadmap as <learning-notes/topic-roadmap.md> and refine it as we learn.

Before the first lesson, I will check prerequisite baseline:
- Which required concepts are zero/fuzzy/familiar/practiced?
- Do you have local notes, uploaded materials, or preferred docs for them?
- Which prerequisite capsules should be inserted before project lessons?

First lesson will start with:
1. A minimal mental model.
2. One concrete walkthrough.
3. Then a light check question.
```

If file writing is unavailable, output the roadmap as Markdown and name the intended file. If writing is available, re-open the file and verify the text is readable before continuing.

## Prerequisite Baseline Intake Pattern

Use after creating the first roadmap and before the first deep lesson:

```text
Before we start, I see these prerequisites will matter soon:

1. <concept> - needed for <chapter/feature>
2. <concept> - needed for <chapter/feature>
3. <concept> - needed for <chapter/feature>

For each one, tell me your level:
- zero: never learned it
- aware: heard of it, not confident
- familiar: can understand examples
- practiced: have built or solved with it

Also tell me whether you have local notes, uploaded docs, course material, or preferred references for these topics.
```

If the learner is unsure, ask 1-3 diagnostic questions only for prerequisites needed in the next chapter. Record results in the roadmap Prerequisite Map and progress Prerequisite Profile.

## Project Teaching Startup Pattern

Use when teaching a codebase with a later migration goal:

```text
Today we are not migrating yet. First we need one reliable mental model of the original project.

Lesson goal: <one thing the learner can explain after this lesson>
Minimum viable understanding: <one sentence>
Prerequisite check: <zero/fuzzy prerequisite to capsule first, if any>
Walkthrough target: <one concrete request/flow and files to inspect>
Migration lens: <what this will later become in the target stack>

After the walkthrough, I will ask one light check question and save the lesson note.
```

Do not ask architecture-mapping questions such as "what NestJS module should this be?" until the learner has seen the original flow and its responsibilities.

## Socratic Hint Ladder

Use progressively stronger help:

1. "What part of the problem tells us which concept to use?"
2. "Look for the relationship between <A> and <B>."
3. "The next step is to isolate <variable/concept/condition>."
4. "Try this setup: <partial setup>."
5. "Here is the full step, and why it works: <explanation>."

## Four-Step Lesson Design Pattern

Use before teaching a major knowledge point. Keep the visible version compact unless the user asks for full lesson design.

```markdown
**Lesson Design: <knowledge point>**

STEP 1: Mental Interface
- Preconception probe: <question that reveals what the learner currently thinks>
- Cognitive conflict: <case where the old idea fails or becomes insufficient>
- Real need: <task, problem, bug, exam type, or project difficulty this concept solves>

STEP 2: Minimum Viable Understanding
- If you remember one thing: <core non-negotiable idea>
- Core metaphor: <metaphor or anchor example, if useful>
- Knowledge-map position: <one sentence connecting prerequisite, current concept, and next concept>

STEP 3: Practice Ladder
- Common blocker 1: <blocker> -> preventive exercise: <exercise>
- Common blocker 2: <blocker> -> preventive exercise: <exercise>
- Common blocker 3: <blocker> -> preventive exercise: <exercise>
- Variations: <five contexts or surface forms that use the same idea>

STEP 4: Transfer Bridge
- From this example to this class of problems: <transfer path>
- Similar but different case: <contrast case>
- Combined challenge: <new problem requiring this concept plus older knowledge>
```

When teaching in chat, usually show only the learner-facing parts: the preconception question, the cognitive conflict, the MVU sentence, and the first exercise.

## Multiple-Choice Quiz Card

```markdown
**Quiz Card 1**
Question: <stem>

A. <option>
B. <option>
C. <option>
D. <option>

Choose A, B, C, or D. I will check your reasoning before moving on.
```

After the learner answers:

```markdown
Correct: <yes/no>
Why: <brief explanation>
If you chose <common distractor>, the likely misconception is <misconception>.
Next: <one follow-up question or repair step>
```

## Flashcard Set

```markdown
**Flashcards**
1. Q: <single idea>
   A: <short answer>
2. Q: <single idea>
   A: <short answer>
3. Cloze: <sentence with ____>
   A: <missing term>
4. Misconception: <incorrect belief>
   Correction: <correct version>
```

## Study Pack

Use at the end of a substantial lesson:

```markdown
**Study Pack**
Key takeaways:
- <takeaway>
- <takeaway>
- <takeaway>

Flashcards:
1. Q: <question>
   A: <answer>

Quiz cards:
1. <question with options>

Common mistakes:
- <mistake> -> <repair>

Next practice:
- <small next task>
```

## Progress Checkpoint Pattern

Use at the end of each substantial lesson in a multi-session path:

```text
Progress saved:
- Current chapter: <chapter>
- Completed today: <lesson/concepts>
- Evidence: <what the learner answered or built>
- Weak spots: <misconceptions or uncertain areas>
- Next resume point: <specific next step>
- Prerequisite gaps: <missing foundations>
- Prerequisite baseline updates: <level changes or new gaps>
- Open next: <1-3 files/notes only>
- Recommended next mode: <continue / review / repair / second pass / project>
```

Update `<topic>-progress.md` by default. Keep the roadmap stable and do not paste a full transcript.

## Fast Resume Pattern

Use when returning to an existing course/project. Optimize for low token use:

```text
I will resume from the separate progress file first.

I will read:
+ `<topic>-progress.md` Resume Snapshot
+ Active roadmap chapter row
+ At most one linked lesson note or weak-spot note

I will not load every previous note unless the progress file is missing, stale, or contradictory.
```

If the progress file snapshot is stale or too long, rewrite it before continuing.

## Return or Second-Pass Pattern

Use when the learner returns to the same project/course or asks to relearn it:

```text
I found the previous progress record. Before we continue:

Previously covered: <short summary from Resume Snapshot>
Last position: <chapter/lesson>
Known weak spots: <weak spots from dialogue>
Prerequisite gaps: <missing foundations>
Next file/note to open: <one item>
Recommended mode: <continue / review / repair / second pass / project>

I will first recap the prior model, then ask one recall question. If the foundation is shaky, I will re-teach from first principles before adding new details.
```

For a second pass, do not repeat the old lesson verbatim. Use prior dialogue as evidence: summarize, repair weak spots, add a clearer model, then deepen with new examples.

## Prerequisite Capsule Pattern

Use when the learner lacks a foundation concept needed for the current project lesson:

```text
We need a short prerequisite capsule before continuing.

Missing concept: <concept>
Learner level: <zero / aware / familiar / practiced>
Why it matters here: <project feature/code path>
Source I will use first: <local note / project docs / official docs / stable model knowledge>
Source reason: <fastest reliable source with lowest token cost>
Minimum useful idea: <1-3 sentence explanation>
Tiny project-linked example: <example>
Check question: <one light question>

After this, we return to <project lesson>.
```

Source priority:
1. User-provided/local materials and project examples.
2. Existing learning notes or cached capsules.
3. Official docs for version-sensitive libraries/APIs.
4. General model knowledge for stable fundamentals only.

Cache the result as a small note when it is likely to be reused, then update the Prerequisite Profile from zero/fuzzy to familiar when the learner passes the check question.

## Saved Lesson Note Pattern

Use when the learner should be able to return later and review the lesson:

```text
I saved this as <path/to/topic-name.md>.

The note includes:
- Core explanation
- Worked example
- Dialogue-derived teaching notes
- Quiz cards
- Flashcards
- Review plan
- Progress checkpoint
- Next practice
```

If file writing is not available in the current environment, output the same note as Markdown and name the intended filename.

## Review Start Pattern

Use when continuing a previous topic:

```text
Before we add new material, let's recover what you already learned.

1. <recall question>
2. <application question>
3. <common mistake repair>
```

After the learner answers, re-teach only the weak part and update the review queue plus the progress record.

## Practice Project Pattern

Use after finishing a module, reading an open-source project flow, or completing several related examples:

```markdown
**Practice Project: <name>**

Source pattern: <what this is based on>
Learning objective: <what this proves>

Requirements:
1. <requirement>
2. <requirement>
3. <requirement>

Checkpoints:
1. <checkpoint>
2. <checkpoint>
3. <checkpoint>

Rubric:
- Correctness: <evidence>
- Understanding: <evidence>
- Transfer: <evidence>
```

## Difficulty Adjustment

If the learner succeeds:

- Ask for transfer to a new example.
- Ask them to explain the rule in their own words.
- Increase distractor similarity in quiz cards.

If the learner struggles:

- Reduce the number of moving parts.
- Give a concrete example before the abstraction.
- Ask a binary or multiple-choice question.
- Rebuild from the prerequisite concept.

## UI Implementation Notes

When asked to build an app or frontend using this coaching model:

- Make the active learning surface the first screen.
- Represent quiz cards with clickable option buttons and immediate feedback.
- Represent flashcards with flip, reveal, or swipe interactions.
- Keep session state: current objective, progress, correct and incorrect answers, saved cards, and weak spots.
- Include compact controls for modes: Learn, Quiz, Flashcards, Review.
- Avoid marketing copy. The learner should start learning immediately.
