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

Use before deep teaching begins for a course, open-source project, or large topic:

```text
Before we enter the first lesson, here is the bird's-eye learning plan.

Goal: <goal>
Assumed level: <level>

Route:
1. <chapter> - <main focus>
2. <chapter> - <main focus>
3. <chapter> - <main focus>

For each chapter, I will gradually add:
- Detailed lesson notes
- Quiz cards and flashcards
- Review points
- Practice or project tasks

I will save the roadmap as <learning-notes/topic-roadmap.md> and refine it as we learn.
First diagnostic check: <question>
```

If file writing is unavailable, output the roadmap as Markdown and name the intended file.

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

## Saved Lesson Note Pattern

Use when the learner should be able to return later and review the lesson:

```text
I saved this as <path/to/topic-name.md>.

The note includes:
- Core explanation
- Worked example
- Quiz cards
- Flashcards
- Review plan
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

After the learner answers, re-teach only the weak part and update the review queue.

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
