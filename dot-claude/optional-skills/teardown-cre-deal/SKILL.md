---
name: teardown-cre-deal
description: Use when processing any CRE offering memorandum (OM), deal memo, tear-down, market study, or deal meeting notes, turning deal material into a brain note, reviewing a deal, or being asked "what do you think of this deal".
---

# Teardown CRE Deal

## Overview

The structure lives in the vault at `directives/optional/cre_deal_notes.md` (Extract → Analyze → Learn → Save). Read and follow it. This skill governs the judgment inside the Analyze step: **an OM is a marketing document, and the job is to critique it, not summarize it.** A summary of an OM repeats the seller's pitch; a teardown finds what the pitch is hiding.

## Procedure

1. **Open the vault directive and follow its four steps.** This skill plugs into steps 2-3.
2. **Extract with provenance.** Every number carries its source location (page/section). A number you computed gets the label `(derived)`. A number recalled from conversation gets `(approximate, from memory)`. Nothing gets estimated from "market typical" without a label saying so.
3. **Two-column read.** Classify each major claim as:
   - **Verifiable fact:** rent roll, in-place NOI, executed leases, comps with addresses, actual expenses.
   - **Marketing:** pro-forma numbers, stabilized projections, "irreplaceable location", "significant upside".
   Then write what the marketing emphasizes and what it buries. Check these specific hiding spots every time: vacancy assumptions, capex needs, lease rollover schedule, concessions/free rent, and whether the quoted cap rate is on in-place or pro-forma NOI. If the OM quotes a cap rate, state which NOI it uses; if it is pro-forma, compute or request the in-place version.
4. **Thesis and risks.** State the deal thesis in one sentence of the form "buyer pays X believing Y will happen." List the 2-3 things that must go right and the 2-3 biggest risks. **Each risk must name a specific number in this deal that breaks if the risk hits.** "Interest rates could rise" fails the bar. "The exit assumes a cap rate on projected NOI far above in-place" passes it, with the actual figures from the deal. If the deal's own numbers are missing, a risk may use hypothetical scenario math, but every such number carries the label `(illustrative)`; an unlabeled invented number in a risk section reads as deal data later.
5. **Lesson.** "What this taught me" must contain something the user did not already know: a term, a trap, a pattern. If the same lesson has now appeared in 2+ prior brain notes, propose extracting it into a skill file in the vault's `skills/` folder per the directive.
6. **Save per the directive:** `brain/notes/YYYY-MM-DD_<type>-<name>.md`, wikilinks, INDEX.md line, run the directive's own QA checklist.

## Confidentiality (hard rule, from the vault's `context/standards.md`)

Deal names, firm financials, and internal employer material stay inside the vault. Anything external-facing gets genericized per the user's standards.md: describe the deal type and market generically, never the deal name. If asked to include identifying deal details in external content, refuse and genericize, citing their standards.

## Judgment Rubric

- [ ] Facts and analysis in separate sections; no opinion sentences in the Facts section
- [ ] Every number traced to a source or explicitly labeled (derived / approximate)
- [ ] The Read names at least one thing the marketing buries
- [ ] Cap rate basis (in-place vs pro-forma) identified whenever a cap rate appears
- [ ] Every risk names a number in this deal, not a generic macro worry
- [ ] Any hypothetical number in a risk carries `(illustrative)`
- [ ] Lesson section says something real, not "learned about cap rates"

## Pushback Rules

- Source document not provided (verbal description only) → write the note anyway, mark it "from memory", flag every number approximate, and say the analysis is provisional. Do not fill gaps with market-typical numbers.
- Asked to "just summarize the OM" → do the extraction, but say the Read section is where the value is and include it unless the user explicitly declines.

## Self-Check

Run the directive's QA checklist verbatim. Then confirm: filename matches the naming pattern, INDEX.md got its one line, and the note contains zero unlabeled derived numbers.
