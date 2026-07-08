---
name: summarize-for-study
description: Use when turning lecture notes, course readings, textbook chapters, or technical work material into study notes, "summarize this lecture", "make a study note", "help me learn this chapter".
---

# Summarize For Study

## Overview

The workflow lives in the vault at `directives/study_summary.md` (Compress → Connect → Test → Save). Read and follow it. This skill governs the quality bar inside each step: **exactness over paraphrase, real connections over decorative ones, application questions over recall questions.** The exam tests the professor's version of the material, so a smooth paraphrase that drifts from the source is a corrupted study note.

## Procedure

1. **Compress with exactness.** Copy definitions and formulas exactly as the source states them, in quotes or as math. "MC = MR at profit max" beats "firms optimize." Keep the professor's framing and terminology where the exam will use it, even if a cleaner phrasing exists.
2. **Connect only where real.** Link to earlier course notes in the brain. Add a real-world hook from the user's own work or interests (see the vault's `context/me.md`) only when the mechanism genuinely matches. Zero decorative links; a forced connection teaches the wrong pattern.
3. **Test with application questions.** Write 3-5 self-test questions requiring the idea to be applied, not recalled. Test each one yourself: **if it can be answered by pattern-matching a sentence in the note, rewrite it.** Answers go collapsed at the bottom. Quantitative topics get one fully worked example with real numbers.
4. **Save per the directive:** `brain/notes/YYYY-MM-DD_<course>-<topic>.md` with Core ideas / Connections / Self-test sections, wikilinks, INDEX.md line. Material too big for one note (a chapter with 4 models) splits into one note per model plus a short overview note. Illegible or ambiguous source content gets `[UNCLEAR]`, never a guess.

## Judgment Rubric

- [ ] Spot-check 2 definitions/formulas against the source: verbatim, not paraphrased
- [ ] Every core idea carries at least one specific (number, named model, worked example)
- [ ] Each self-test question fails the copy-lookup test (not answerable by finding one sentence)
- [ ] Quantitative topic → one worked example with numbers is present
- [ ] Zero guessed content; gaps marked `[UNCLEAR]`

**Good question:** "A landlord's marginal cost of leasing one more floor is near zero but rents are falling. What does MC = MR imply about whether to lease it, and at what rent?"
**Bad question:** "What is the profit-maximization condition?" (answerable by copy-lookup)

## Pushback Rules

- No source material provided ("summarize the lecture" with no notes attached) → ask for the material. **Never generate a topic summary from general knowledge and present it as course notes**; it will differ from what the professor said, and the exam tests the professor's version.
- Source is a photo/handwriting that is partly illegible → transcribe what is legible, mark gaps `[UNCLEAR]`, and list them so the user can fill from memory while it is fresh.

## Self-Check

Run the directive's QA gate. Report: which 2 definitions were spot-checked against source, confirmation each self-test question passed the rewrite rule, and that the note is dated, linked, and indexed.
