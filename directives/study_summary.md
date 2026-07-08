# Study Summary

## What this workflow is

Turn a lecture, reading, chapter, or course unit into a dense study note built for actually learning the material, not just filing it. Works for coursework and for anything technical picked up at work.

## Prerequisites

- `brain/INDEX.md` checked for earlier notes from the same course or topic
- Relevant files in the vault's `skills/` folder, if any exist for the subject

## Inputs

| Field | Required | Description |
|---|---|---|
| Material | yes | Lecture notes, slides, reading, transcript, or textbook section |
| Course/topic | yes | What this belongs to |
| Purpose | no | Exam prep / problem set support / general understanding (default: general) |

## Process

**Step 1: Compress.** Extract the core ideas with their exact definitions, formulas, and numbers. Specifics over summaries: "MC = MR at profit max" beats "firms optimize." Keep the author's or professor's framing where it matters for the exam.

**Step 2: Connect.** Link to earlier notes from the course and to real-world hooks from the owner's own work and interests (see `context/me.md`). Real connections only; a forced connection teaches the wrong pattern.

**Step 3: Test.** End the note with 3 to 5 self-test questions that require actually understanding the material, with answers collapsed at the bottom. For quantitative topics, include one worked example.

**Step 4: Save.** Write `brain/notes/YYYY-MM-DD_<course>-<topic>.md` with sections: Core ideas, Connections, Self-test. Link with [[wikilinks]]. Update INDEX.md.

## Quality gates

- [ ] Definitions and formulas are exact, not paraphrased into mush
- [ ] Contains specifics: numbers, named models, worked examples where relevant
- [ ] Self-test questions exist and are answerable from the note
- [ ] Dated, linked, indexed

## Edge cases

- Material is too long for one note (a whole textbook chapter with 4 distinct models): split into multiple notes, one per model, linked to a short overview note.
- Handwritten or messy source: transcribe what's legible, flag gaps with [UNCLEAR] rather than guessing.
