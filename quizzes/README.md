# quizzes/

Platform quiz files for Quiz Me mode — one per chapter.

## What this directory is for

These are structured quiz files for use in Medhavy, Canvas, or similar
platforms. They are distinct from Anki flashcards (`anki/`): Anki is for
vocabulary retention; quizzes test concept application and comprehension.

One file per chapter, matching the `chapters/` numbering convention.

## File format

Markdown. Filename: `[NN]-[chapter-slug]-quiz.md`

Each file should contain at minimum:
- 5–10 questions per chapter
- Question type labeled: multiple choice / short answer / true-false / matching
- Correct answer and brief rationale for each question
- Bloom's level tag for each question

## How it connects to Medhavy

Quiz files are the primary input for Medhavy's Quiz Me mode. The FSRS
spaced-retrieval scheduler uses quiz performance to set due dates.
Import format: [Medhavy quiz import format — update when finalized]

## Authored by

AI-assisted, with instructor review. Questions derived from `exercises/`
and `assessments/` sections in chapter files.
