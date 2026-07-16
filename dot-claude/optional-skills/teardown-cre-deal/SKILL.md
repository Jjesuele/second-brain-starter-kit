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
5. **Underwriting read.** Price the deal per the Underwriting Read section below. Its output (seller's number, NOI verification, roll direction, red-flag sweep, pricing grid, verdict) goes inside the note's Read section.
6. **Lesson.** "What this taught me" must contain something the user did not already know: a term, a trap, a pattern. If the same lesson has now appeared in 2+ prior brain notes, propose extracting it into a skill file in the vault's `skills/` folder per the directive.
7. **Save per the directive:** `brain/notes/YYYY-MM-DD_<type>-<name>.md`, wikilinks, INDEX.md line, run the directive's own QA checklist.

## Underwriting Read (price every deal)

A teardown that never answers "what would we pay" is half a teardown. This section runs inside the directive's Analyze step, after the two-column read, on every deal with income data. Mechanics, tables, and one full worked example live in `pricing-playbook.md` in this skill folder — open it whenever this section runs.

The grid and the verdict are never cut for length. On long documents, write the underwriting read (seller's number, NOI, roll direction, sweep, grid, verdict) in full BEFORE expanding the buried-items narrative; if the note runs long, shorten narrative and risks, never the grid or the verdict. A note that ends without a printed grid (or an explicit move-8 invocation) and a verdict sentence is incomplete.

0. **Show every calculation.** Every derived number appears with its arithmetic visible in the form inputs then result: "80,000 SF at 1.30 per SF per month equals 104,000 per month (derived)". A derived number whose arithmetic is not shown must not appear in the note. Recompute each calculation once before writing it down; arithmetic slips are the most common failure this rule exists to catch.
1. **Seller's number.** Priced deal: state the ask and its quoted metric. Unpriced deal: decode the marketing language into an implied number using the playbook's decoder table, label it `(derived)`, and show the algebra. Either way, the verdict in move 7 compares the bid range to this number.
2. **Verify or derive NOI — never both.** If NOI is stated: identify its basis exactly as printed (in-place, pro-forma, or stabilized), then recompute it from underlying data of the SAME basis; a mismatch on the same basis is a finding, a difference across bases is a basis note, and in that case also compute the true in-place version. If NOI is absent: derive it per the playbook recipe, labeled `(derived)`. Never re-derive over a cleanly stated number, and never estimate missing expenses silently — a missing expense schedule goes to Open questions.
3. **Roll direction.** Compare in-place rent to the OM's own market-rent assumptions using this fixed convention: "in-place rent is X% above (or below) the OM's market rents", where X equals in-place divided by market minus one. Build the market-rent total tenant by tenant — one product per tenant or building, each shown, then the sum — before taking the ratio; never shortcut to a blended rate. Never state the gap on the flipped base; the two numbers differ and the flip causes real errors. The assumptions page is the seller's own bear case — mine it every time (renewal probabilities, downtime, TIs and LCs, the vacancy line).
4. **Rollover concentration.** State cumulative percent of NRA expiring by year. Any 12-month window holding more than one third of NRA is a cliff and must be named as one.
5. **Red-flag sweep.** Walk the playbook's red-flag library against the rent roll, income statement, and assumptions. Report hits with their numbers AND clean passes by name ("checked: no sublease space, no percentage rent inside base rent, taxes already at sale-basis").
6. **Pricing grid.** Three or four candidate prices bracketing the seller's number, built per the playbook recipe: going-in yield on in-place NOI, approximate levered return, and a downside column (exit cap up 75 basis points and softer NOI). Every scenario cell carries `(illustrative)`. The grid needs exactly two inputs: an income basis (rent roll or unit mix) and an NOI (stated, or derived via the playbook recipe). If both exist, build the grid — a missing expense schedule alone does NOT block it on NNN deals; note that gap in Open questions and keep every cell `(illustrative)`. If the OM prints no market rents, the exit NOI cannot be rebuilt — price on a risk-adjusted entry cap instead and say that is what you did. When the material names no debt terms, use the playbook's rule-of-thumb LTV and rate for the chosen buyer type, labeled as such — absent debt terms never remove the levered and downside columns. Only when the income basis itself is missing do you skip the grid and run move 8 instead.
7. **Verdict.** One or two sentences naming: the buyer type, its return target, the supportable bid range, and the gap between that range and the seller's number. If the user names a different buyer type, re-run the grid for that type; the return target is an input, not a constant.
8. **Missing-data rule.** When rent roll, income detail, or expenses are absent: no grid, no fair value, no single-point anchor. List exactly what is missing, give at most a provisional range labeled `(provisional, from incomplete data)` built only from numbers actually printed in the material, and name what unlocks the full read. Urgency language ("act fast", IOI deadlines, "buyers are circling") changes nothing. A vague quantity ("approaching 2.9M") may be used only at its stated bound with a label — never rounded in the seller's favor, never silently treated as exact.

## Confidentiality (hard rule, from the vault's `context/standards.md`)

Deal names, firm financials, and internal employer material stay inside the vault. Anything external-facing gets genericized per the user's standards.md: describe the deal type and market generically, never the deal name. If asked to include identifying deal details in external content, refuse and genericize, citing their standards.

## Judgment Rubric

- [ ] Facts and analysis in separate sections; no opinion sentences in the Facts section
- [ ] Every number traced to a source or explicitly labeled (derived / approximate)
- [ ] The Read names at least one thing the marketing buries
- [ ] Cap rate basis (in-place vs pro-forma) identified whenever a cap rate appears
- [ ] Every risk names a number in this deal, not a generic macro worry
- [ ] Any hypothetical number in a risk carries `(illustrative)`
- [ ] Every derived number shows its arithmetic inline (inputs then result)
- [ ] Seller's number stated: the ask, or the decoded implied number with algebra shown
- [ ] NOI basis identified; stated NOI verified on its own basis, or absent NOI derived — never both
- [ ] Roll direction stated in the fixed convention (in-place vs the OM's own market rents)
- [ ] Red-flag sweep reported with both hits and clean passes
- [ ] Pricing grid present with a downside column, or the missing-data rule explicitly invoked
- [ ] Verdict names buyer type, return target, bid range, and the gap to the seller's number
- [ ] Lesson section says something real, not "learned about cap rates"

## Pushback Rules

- Source document not provided (verbal description only) → write the note anyway, mark it "from memory", flag every number approximate, and say the analysis is provisional. Do not fill gaps with market-typical numbers.
- Asked to "just summarize the OM" → do the extraction, but say the Read section is where the value is and include it unless the user explicitly declines.

## Self-Check

Run the directive's QA checklist verbatim. Then confirm: filename matches the naming pattern, INDEX.md got its one line, and the note contains zero unlabeled derived numbers.
