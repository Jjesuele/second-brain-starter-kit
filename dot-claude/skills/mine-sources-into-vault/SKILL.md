---
name: mine-sources-into-vault
description: Use when importing documents, transcripts, exports, or pasted material into the second brain vault — "import these docs", "add this to sources", "mine this into the brain", "pull what's useful from these files" — or when files sit in sources/ waiting to be processed.
---

# Mine Sources Into Vault

## Overview

Raw material (school docs, work docs, transcripts, exports) lands in the vault's `sources/` folder and gets mined into the vault's living files. The two failures that corrupt a vault are **promoting one context's preferences into universal rules** (one professor's essay conventions quietly becoming core principles for all essays) and **paraphrase drift that turns a sourced fact into an invented one.** Mining is extraction with provenance, not synthesis.

## Procedure

1. **Inventory before importing.** Check `sources/*/INDEX.md` and `brain/INDEX.md` for what is already in. Never re-mine material that has an import note (look for notes like `YYYY-MM-DD_*-imported`). If it is already in, say where it lives and stop.
2. **Land the raw files first.** Copy or convert into `sources/<collection>/`, one line per file in that collection's `INDEX.md`, following the existing pattern there. Raw files are kept as-is; they are the provenance trail.
3. **Route each extracted fact to exactly one destination:**
   - Identity fact about the owner (courses, jobs, dates, strengths) → `context/me.md`
   - Durable technique or domain knowledge that holds across contexts → the matching folder under `skills/`
   - Event, lesson, or decision → dated note in `brain/` (follow the brain-capture skill's filter and format)
   - Concrete story with situation, action, result → `brain/references/story-bank.md`
   - Unsure → brain note. It is the cheapest to move later.
4. **Scope-to-source rule.** Any convention, preference, or requirement that comes from ONE professor, ONE course, ONE employer, or ONE person goes in a section labeled with that source and date, for example `## Prof. Alvarez, WRIT 101, fall 2025`. It never becomes an unlabeled rule, checklist item, or "core principle". Files that collect such sections state at the top that the current assignment's or employer's guidelines win. Only the owner's own cross-context style may be stated generally, and that lives in `context/voice.md`, nowhere else.
5. **Extract with provenance.** Every fact written into the vault names its source file. Quotes are verbatim. Numbers, names, and dates are copied, not recalled. A gap gets `[FILL IN: what is needed]`, never a plausible filler. Illegible or ambiguous source content gets `[UNCLEAR]`.
6. **Genericize confidential material at extraction time.** Employer names, internal figures, and private facts may live inside the vault, but anything routed toward external-facing files (story bank entries used in applications, skills that feed cover letters) gets the generic form per `context/standards.md` rule 3: "a mid-size project at my internship", never the internal name.
7. **Show the routing plan before writing.** One line per destination file: what goes in and from which source. Wait for approval. For big imports, propose the plan for the batch, not per fact.
8. **After writing:** INDEX.md lines for new brain notes, an import note recording what was mined (matching the existing `*-imported` notes), commit and push the vault.

## Worked Example — the scope-to-source failure

Source material: a professor's feedback across several essays in one course says openers should skip hooks and lead with the thesis.

**FAIL:**
> ## Essay principles
> - No hooks. State the thesis in the first sentence.
> - Avoid rhetorical questions as openers.

Why it fails: two ungrounded universals. A different professor may want a hook. A model following this file would now write every essay for every course to one professor's taste.

**PASS:**
> Note: the current assignment's own prompt and the professor's stated guidelines always override anything below.
>
> ## Prof. Alvarez, WRIT 101, fall 2025
> Wants no hooks: thesis stated up front, no rhetorical-question openers (source: margin feedback in sources/school-docs, essays 2 and 4).

Why it passes: same information, zero loss, scoped to its source with provenance, and the override line makes the precedence explicit for a literal-minded reader.

## Judgment Rubric

- [ ] Every extracted fact names its source file; spot-check 3 against the raw source
- [ ] Zero unlabeled universal rules extracted from a single-source preference
- [ ] Any file collecting per-source conventions carries the "current guidelines win" line at top
- [ ] Nothing re-mined that an import note already covers
- [ ] Confidential specifics genericized in anything external-facing
- [ ] Routing plan was shown and approved before files were written
- [ ] New brain notes indexed; an import note exists for the batch

**Good:** "Resume v3 says lifeguard, city pool, summer 2024, supervised 200+ daily visitors → me.md, source cited."
**Bad:** "The owner's essays show they should always avoid personal anecdotes" (one professor's preference laundered into an identity fact).

## Pushback Rules

- Asked to bulk-mine email, Drive, or old chat history wholesale → push back once: bulk mining fills the vault with unvetted notes and burns heavy tokens. Offer a targeted single-collection grab instead. If the owner insists, proceed with the filter applied hard.
- A fact cannot be traced to a source file in the batch → do not write it flat. Mark it `(approximate, from conversation)` or leave it out and ask.
- Asked to write a universal writing or work rule extracted from one person's feedback → push back once, name the scope-to-source rule, and write the scoped version instead. Only the owner can promote something into voice.md or standards.md.

## Self-Check

Before reporting done: reread every new or edited vault file and confirm each single-source convention sits under a source-labeled heading. Confirm INDEX.md line count matches new note count. Confirm the import note exists and the vault committed and pushed. State which 3 facts were spot-checked against raw sources.
