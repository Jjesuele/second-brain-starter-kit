---
name: draft-academic-essay
description: Use when drafting, restructuring, or expanding any school essay or written assignment, papers with MLA or APA citations of assigned course readings, in any subject.
---

# Draft Academic Essay

## Overview

Course essays cite assigned readings, follow the professor's prompt exactly, and read in the user's own voice. The two failure modes that ruin an essay are fabricated citations and chatbot prose. This skill prevents both. **REQUIRED SUB-SKILL:** edit-into-voice runs on every draft before delivery.

## Gate: three inputs before writing a word

1. The assignment prompt, verbatim. Exception: if the user states the professor gave only a broad topic and no written prompt, their description of the topic counts as the prompt; record their exact words.
2. The assigned readings or sources the user is allowed to cite (files, titles, or pasted excerpts). Exception: if the user states the professor allows or expects outside research, the Web-research path below replaces this input.
3. The required citation format (MLA, APA, or professor's spec).

**If any of the three is missing and no exception applies, stop and ask for it. Do not draft from a paraphrased prompt. Do not substitute readings from general knowledge.** An essay citing a source the professor never assigned is worse than no essay.

## Web-research path (only when the user says outside sources are allowed)

1. Sources must be reliable named outlets or institutions (wire services, major papers, think tanks, government briefings). No Wikipedia, no user-generated content, even as a convenience.
2. Cite only pages actually fetched this session. A source seen only in a search-result summary is not citable.
3. Verify every quote before delivery: after drafting, re-fetch each cited page and confirm the exact quoted wording appears. A quote that cannot be re-confirmed gets cut or replaced, never left in.
4. Some outlets block automated fetching. Do not cite what could not be fetched; find a fetchable source instead and tell the user which outlets were skipped and why.
5. Every number and factual claim in the essay traces to one of the fetched sources or gets cut. The no-fabrication gate applies with full force since there is no professor-provided reading list as a backstop.
6. Every source used gets an in-text citation and an entry in the citation list at the end. No source appears in one place without the other.

## Procedure

1. **Restate the question.** Extract the professor's actual question from the prompt and write it as one sentence. The essay must answer that sentence, not a nearby easier one. If the prompt has multiple parts, list them; each part must be answered somewhere.
2. **Build the skeleton the user's way** (see the vault's `context/voice.md` for their structural habits). Reliable defaults when their voice file does not specify:
   - One central idea, stated in the first paragraph as an arguable thesis (someone could disagree with it), returned to as an anchor in every body paragraph.
   - Each body paragraph engages a source: introduce a quote or fact from an assigned reading, then interpret it in the writer's own move on it.
   - One widening closer at the end (a sentence that opens the argument outward), not one per paragraph.
3. **Draft only from the provided sources.** Every citation points to a real page or section of a provided reading. Anything you cannot verify in the provided material gets a labeled placeholder asking for the source, never a plausible-looking citation to fill a gap.
4. **Run edit-into-voice on the full draft.** All of its checks apply.
5. **Deliver with a header:** thesis in one line; list of readings actually cited; list of every placeholder gap the user must resolve.
6. **Deliver in the format the user's operating file or vault standards name; default to a Word .docx for coursework.** Build it in the assignment's format (APA default: Times New Roman 12, double spaced, title page, page numbers, hanging-indent references), validate the file, and name its full path in the delivery message. Keep the markdown source alongside it. Unknown title-page fields (course, professor) get labeled placeholders, never guesses.

## Judgment Rubric

- [ ] Thesis in the first paragraph, arguable, echoed in each body paragraph
- [ ] Every body paragraph both cites a provided source and interprets it (no quote left hanging, no paragraph with zero source contact)
- [ ] Zero citations to works outside the provided list (verify each one); on the web-research path, zero citations to pages not fetched and quote-verified this session
- [ ] Every part of a multi-part prompt is answered
- [ ] Passes the edit-into-voice rubric

**Good paragraph:** quotes an assigned reading, then unpacks it with the writer's own position on it.
**Bad paragraph:** cites a real-sounding article the professor never assigned, or summarizes a reading without taking any position on it.

## Pushback Rules

- No prompt text → do not draft. Ask.
- Citations required but no readings provided → do not draft. Ask. Never supply outside sources unprompted for a course essay; the web-research path opens only when the user says the professor allows it.
- If the thesis the user wants contradicts what the provided readings can actually support, say so plainly before drafting and propose the closest thesis the evidence carries.

## Self-Check (report before delivering)

State: every in-text citation matched against the provided-readings list (count checked / count total), number of placeholder markers with their locations, and the voice self-check line from edit-into-voice.
