# Pricing Playbook (reference for the Underwriting Read)

Everything here is a rule of thumb to verify against deal data and current market — never a fact about any specific deal. Rules of thumb drift; re-check them against live market data every few months. Every number produced with these recipes carries `(derived)` or `(illustrative)` and shows its arithmetic.

## Implied-price decoder

Unpriced OMs still tell you the price. Translate the language, show the algebra, label the result `(derived)`.

| Broker phrase | Algebra | What it tells you |
|---|---|---|
| "double-digit going-in yields" | in-place NOI divided by 0.10 | ceiling of the seller's hoped-for range: the price they expect offers to beat |
| "sub-7 cap" (any "sub-X cap") | in-place NOI divided by X percent | floor of the seller's expectation — a lower cap means a HIGHER price |
| "significant mark-to-market" | in-place rent vs the OM's own market rents | check the direction first; if in-place is above market, the phrase inverts to roll-down |
| "N remaining contractual rent" | N divided by each candidate price | percent of basis covered by signed leases |
| "priced below replacement cost" | ask for the replacement math | usually signals the income does not support the price |
| "guidance available upon request" | comps set the range | broker price discovery; anchor on your grid, not their hints |
| "act fast", "offers due", "buyers circling" | nothing | process pressure carries zero pricing information; changes no number |

## Red-flag library

Sweep every deal. Report hits with their numbers AND clean passes by name.

1. **Sublease space inside full occupancy.** A subtenant in the rent roll means both the tenant of record and the occupant have signaled they will not hold the space at that rent. Compute: sublease rent vs contract rent, spread in dollars per year (SF times spread times 12, shown).
2. **Cap rate quoted on pro-forma NOI.** Compute the in-place version and restate the cap on it. The gap between the two caps is the seller's optimism, quantified.
3. **Percentage rent inside base rent.** Strip it out; restate NOI and the cap ex-percentage rent. Percentage rent is volatile income priced as if it were contractual.
4. **Tax reassessment at sale.** Compare assessed value to candidate prices. In California (Prop 13), taxes reset to roughly 1.1 to 1.2 percent of the purchase price at closing (rule of thumb; check the county). Everywhere: if assessed value is far below price, recompute NOI with sale-basis taxes and show both numbers.
5. **Free rent burn-off and straight-lined rents.** Ask whether year-one cash rent equals the rent roll number. Abatements inflate the early yield.
6. **Physical vs economic occupancy.** Units or suites can be occupied and not paying. Check collections against GPR when a T-12 exists.
7. **"Recently renovated" with no reserve line.** Renovation age plus zero capital reserve equals deferred spending hidden from NOI. Convention: reserves of 0.10 to 0.50 per SF per year in underwriting (rule of thumb).
8. **WALT shorter than the hold.** The exit buyer inherits the rollover; your exit cap should say so.
9. **Income concentration.** Any single tenant above one third of total rental income is a concentration finding. Compute the share and state it.
10. **Retail: co-tenancy, kick-outs, operating covenants.** Find every termination right and conditional rent clause; compute the distance between current sales and any threshold, and the rent lost if co-tenancy triggers (shown as contract rent times the reduction percentage).
11. **Multifamily: market rents dressed as current.** "In-place NOI" built on market rents is pro-forma wearing a costume — rebuild on contract rents. Vacancy below the 5 percent convention gets restated at 5 percent (rule of thumb). Missing turnover and loss-to-lease lines are findings.
12. **Zero general vacancy in a multi-year pro forma.** A model that predicts turnover while charging no vacancy is arguing against itself.
13. **Fantasy debt.** Assumed leverage or rate better than market. Run the DSCR check in the grid recipe; if it fails, the leverage does not exist.

## Buyer-type table (rules of thumb; verify per deal and per market cycle)

| Type | Levered IRR target | Typical leverage | What it actually pays on |
|---|---|---|---|
| Core | 7 to 9 percent | 30 to 50 percent | in-place income, credit, duration |
| Core-plus | 9 to 12 percent | 50 to 60 percent | in-place plus modest lease-up |
| Value-add | 13 to 18 percent | 60 to 70 percent | stabilized NOI the buyer must create |
| Opportunistic | 18 percent and up | 70 percent and up | an outcome the buyer must build |

The same asset prices differently for each type. The verdict must name which type the bid range belongs to. If the user does not name one, default to value-add at mid-teens levered for practice reads and say the default was used.

## NOI derivation recipe (only when NOI is absent — never over a stated number)

- **NNN:** NOI approximately equals total base rent times 0.97 — a management drag of about 3 percent of effective gross revenue (rule of thumb; leases often cap the fee at 3 percent of base rent — if the deal's own documents state a different management fee, use the deal's number and say so). Show the multiplication. Label `(derived)`.
- **Gross or full-service leases:** cannot be derived without an expense schedule. Stop; send it to Open questions.
- **Multifamily:** GPR at CONTRACT rents, minus the larger of actual economic vacancy and the 5 percent convention, plus other income, minus T-12 expenses with taxes RESET to sale basis (candidate price times the local rate). Show NOI both before and after reassessment.

## Pricing grid recipe

1. **Buyer type and target.** From the table above; state which and why.
2. **Hold.** Five years default; seven when the plan is heavy rollover repositioning.
3. **Stabilized exit NOI.** Rebuild income at the OM's OWN market rents grown at its OWN growth rates, then apply the NOI derivation recipe. Add nothing the OM did not print.
4. **Exit cap.** At or above the going-in market cap; never below going-in without a printed reason. Sales cost 2 percent (rule of thumb).
5. **Debt.** Buyer-type LTV at a rate from the material, or a labeled rule-of-thumb rate. Interest only for simplicity; say so.
6. **DSCR check.** In-place NOI divided by annual interest must be at least 1.25 (rule of thumb) or the leverage is fantasy — cut LTV until it passes and report that you did.
7. **Per candidate price** (three or four bracketing the seller's number):
   - Going-in yield = in-place NOI divided by price (show it).
   - Average annual cash flow = the average of in-place and stabilized NOI, minus interest (a crude average; label it).
   - Net exit = stabilized NOI divided by exit cap, times 0.98, minus debt balance.
   - Equity multiple = (total cash flows plus net exit) divided by equity.
   - Approximate levered return from the lookup table below.
8. **Downside column.** Exit cap up 75 basis points AND stabilized NOI down 7 to 10 percent; recompute the row. A bid is only safe if the downside cell still clears the buyer's minimum (roughly the target minus 5 points, rule of thumb).
9. **Bid range.** The prices where the base case clears the target and the downside clears the minimum. State it against the seller's number: that difference is the bid-ask gap.

**Equity multiple to approximate levered IRR** (treats value as realized at exit; when annual cash flow is a big share of the total, true IRR runs 1 to 3 points higher — say so when it applies):

| Multiple | 5-year hold | 7-year hold |
|---|---|---|
| 1.25x | 4.6 percent | 3.2 percent |
| 1.5x | 8.4 percent | 6.0 percent |
| 1.75x | 11.8 percent | 8.3 percent |
| 2.0x | 14.9 percent | 10.4 percent |
| 2.25x | 17.6 percent | 12.3 percent |
| 2.5x | 20.1 percent | 14.0 percent |
| 3.0x | 24.6 percent | 17.0 percent |

## Worked example (entirely invented numbers — the output shape to match)

*Alder Grove Corporate Center: 100,000 SF two-building NNN office, unpriced OM advertising "double-digit going-in yields". Rent roll: Tenant A 60,000 SF at 6.20 per SF per month to Mar-2028; Tenant B 40,000 SF at 5.70 to Sep-2030. OM's own market rents: 5.00 both buildings.*

- In-place rent: 60,000 x 6.20 x 12 = 4,464,000; 40,000 x 5.70 x 12 = 2,736,000; total 7,200,000 per year (derived).
- NOI (NNN recipe): 7,200,000 x 0.97 = 6,984,000 (derived).
- Seller's number: "double-digit" means 6,984,000 / 0.10 = 69.8M ceiling (derived).
- Roll direction: 7,200,000 / 6,000,000 - 1 = 20.0% — in-place rent is 20% above the OM's own market rents (derived).
- Cliff: 60% of NRA expires in one window (Mar-2028) — over one third, named as a cliff.
- Sweep: no sublease space (clean); cap quoted on nothing (unpriced); no percentage rent (clean); assessed-value data absent — reassessment to Open questions; zero general vacancy in pro forma (hit).
- Grid (value-add, mid-teens target, 5-yr hold, exit 8.00% on stabilized NOI 5,820,000 = 6,000,000 x 0.97; downside exit 8.75% on 5,400,000; 60% LTV interest only at 6.5%; DSCR at 60M: 6,984,000 / 2,340,000 = 2.98, passes; all cells illustrative):

| Price | Going-in | Levered approx (base) | Levered approx (downside) |
|---|---|---|---|
| 55M | 12.7% | ~22% | ~17% |
| 60M | 11.6% | ~18% | ~13% |
| 65M | 10.7% | ~15% | ~9% |
| 70M | 10.0% | ~11% | ~5% |

- Verdict: a value-add buyer targeting mid-to-high teens levered supports 55M to 62M, centering near 58M so the downside stays in double digits; the decoded ask of about 69.8M leaves a bid-ask gap of roughly 8M to 15M (illustrative).
