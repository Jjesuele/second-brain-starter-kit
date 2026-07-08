---
name: draft-academic-essay
description: Use when drafting, restructuring, or expanding any school essay or written assignment, papers with MLA or APA citations of assigned course readings, in any subject.
---

# Draft Academic Essay

## Overview

Course essays cite assigned readings, follow the professor's prompt exactly, and read in the user's own voice. The two failure modes that ruin an essay are fabricated citations and chatbot prose. This skill prevents both. **REQUIRED SUB-SKILL:** edit-into-voice runs on every draft before delivery.

## Gate: three inputs before writing a word

1. The assignment prompt, verbatim.
2. The assigned readings or sources the user is allowed to cite (files, titles, or pasted excerpts).
3. The required citation format (MLA, APA, or professor's spec).

**If any of the three is missing, stop and ask for it. Do not draft from a paraphrased prompt. Do not substitute readings from general knowledge.** An essay citing a source the professor never assigned is worse than no essay.

## Procedure

1. **Restate the question.** Extract the professor's actual question from the prompt and write it as one sentence. The essay must answer that sentence, not a nearby easier one. If the prompt has multiple parts, list them; each part must be answered somewhere.
2. **Build the skeleton the user's way** (see the vault's `context/voice.md` for their structural habits). Reliable defaults when their voice file does not specify:
   - One central idea, stated in the first paragraph as an arguable thesis (someone could disagree with it), returned to as an anchor in every body paragraph.
   - Each body paragraph engages a source: introduce a quote or fact from an assigned reading, then interpret it in the writer's own move on it.
3. **Draft only from the provided sources.** Every citation points to a real page or section of a provided reading. Anything you cannot verify in the provided material gets a labeled placeholder asking for the source, never a plausible-looking citation to fill a gap.
4. **Run edit-into-voice on the full draft.** All of its checks apply.
5. **Deliver with a header:** thesis in one line; list of readings actually cited; list of every placeholder gap the user must resolve.

## Judgment Rubric

- [ ] Thesis in the first paragraph, arguable, echoed in each body paragraph
- [ ] Every body paragraph both cites a provided source and interprets it (no quote left hanging, no paragraph with zero source contact)
- [ ] Zero citations to works outside the provided list (verify each one)
- [ ] Every part of a multi-part prompt is answered
- [ ] Passes the edit-into-voice rubric

**Good paragraph:** quotes an assigned reading, then unpacks it with the writer's own position on it.
**Bad paragraph:** cites a real-sounding article the professor never assigned, or summarizes a reading without taking any position on it.

## Pushback Rules

- No prompt text → do not draft. Ask.
- Citations required but no readings provided → do not draft. Ask. Never supply outside sources unprompted for a course essay.
- If the thesis the user wants contradicts what the provided readings can actually support, say so plainly before drafting and propose the closest thesis the evidence carries.

## Self-Check (report before delivering)

State: every in-text citation matched against the provided-readings list (count checked / count total), number of placeholder markers with their locations, and the voice self-check line from edit-into-voice.
