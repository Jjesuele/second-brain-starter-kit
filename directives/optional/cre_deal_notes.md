# CRE Deal Notes

## What this workflow is

Turn commercial real estate work product into a structured, dated brain note: deal tear-downs, offering memo (OM) reviews, market studies, and meeting notes. The goal is twofold: a clean note now, and a compounding record of CRE pattern recognition over time.

## Prerequisites

- `context/standards.md` loaded (confidentiality rule especially)
- Relevant files in the vault's `skills/` folder, if any exist for the asset type
- `brain/INDEX.md` checked for related deals or prior notes on the market

## Inputs

| Field | Required | Description |
|---|---|---|
| Type | yes | Tear-down / OM review / market study / meeting notes |
| Material | yes | The OM, model, notes, transcript, or verbal download |
| Deal or topic name | yes | What to call it (genericized if sensitive) |

## Process

**Step 1: Extract.** Pull the hard facts from the material. For a deal: asset type, location, size, price and key metrics (cap rate, PSF, rent assumptions), business plan, sponsor. For a market study: the numbers that define the market (vacancy, rents, pipeline, absorption). Every number comes from the source; nothing estimated without a label.

**Step 2: Analyze.** What's the thesis? What has to go right? What are the two or three biggest risks? For tear-downs and OM reviews, note what the marketing is emphasizing versus quietly burying. This is the judgment layer; keep it separate from the facts layer.

**Step 3: Learn.** One section called "What this taught me": the pattern, term, or technique the owner didn't know before. If a term or concept keeps recurring across notes, propose extracting it into a skill file in the vault's `skills/` folder.

**Step 4: Save.** Write `brain/notes/YYYY-MM-DD_<type>-<name>.md` with sections: Facts, Read, What this taught me, Open questions. For meetings, add a Follow-ups section with owners and dates. Link related notes ([[wikilinks]]). Update INDEX.md.

## Quality gates

- [ ] Facts and analysis are clearly separated
- [ ] Every number traces to the source material; unknowns are labeled, not guessed
- [ ] Tear-downs and OM reviews: pricing verdict present (buyer type, return target, bid range, gap to the seller's number), or the teardown skill's missing-data rule explicitly invoked
- [ ] "What this taught me" section exists and says something real
- [ ] Confidentiality: note stays in the vault; nothing deal-identifying leaves it
- [ ] Note is dated, linked, and indexed

## Edge cases

- Verbal download with no documents: write the note anyway, mark it as from memory, and flag numbers as approximate.
- A note contradicts an earlier note about the same market or deal: keep both, add a dated line in the newer one saying what changed.
