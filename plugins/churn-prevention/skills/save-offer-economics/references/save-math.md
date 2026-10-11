# Save-offer measurement

## The checkpoint

The outcome is "paying full price in the first billing cycle after the discount or pause ends". For a 3-month discount on monthly billing that is month 4; for an annual plan it is the next annual renewal after the discounted one. Before the checkpoint, say paid retention and incremental effect are not yet measured; report supported uptake, current status and any decision-relevant list-price exposure without calling it recovered revenue. For a permanent downgrade, use the agreed new-plan price and a named follow-up window. Do not assume automatic resumption.

## The three numbers, side by side (per reason group and in total)

| Number | Formula | Reads as |
|---|---|---|
| Acceptance rate | accepted ÷ offered | how many said yes at the screen; never called a save |
| Retained share | paying full price at the checkpoint ÷ everyone offered (accepted or not) | how many of those offered still pay |
| Incremental retention | retained share (offered) − retained share (holdout) | how many stayed because of the offer |

Each rate gets n and a Wilson interval; the difference gets a Newcombe interval (`stats-glossary.md`). The headline is the incremental line and its verdict.

## Pause

| Outcome | Count |
|---|---|
| Paused, then resumed and paying at the next full cycle | |
| Cancelled at the end of the pause | |
| Still paused when the data ends | |

Paused accounts are never counted as paying while paused.

## Rented, not saved

Accepters who cancelled during the discount or in the first full-price cycle. Print the count and the rate over accepters; ids only when the user asks for the list. Compute it only when the data says which customers paying at the checkpoint had accepted; otherwise print the bound "at least (accepted − paying full price at the checkpoint) accepters were not paying full price" and ask for the split. Never assume that every decliner cancelled.

## Cost

- Gross discount cost = sum over accepters of (discounted months actually billed × list price × discount share).
- If only the terms are known: accepters × months × list price × discount share, labelled "maximum".
- Net cost = (revenue per holdout member − revenue per person offered) × number offered, over the offer month through the checkpoint. A negative result is a net gain. It requires actual month-by-month billing for both arms. If missing, lead with “actual net cost is unknown” and name the missing billing data. Show a terms-based gross ceiling only as a conditional scenario, not actual spend; do not add discounted-revenue ceilings unless requested or needed for the decision. Net cost may be higher or lower than gross discount cost.
- Incremental customers (point estimate) = incremental retention × number offered, with its range (the two ends of the incremental-retention range × number offered).
- Cost per incremental retained customer = actual cost ÷ incremental customers. If the effect interval includes zero, lead with "cost per extra customer is not established". A secondary conditional point-estimate ratio must name the billing assumptions and uncertain denominator; it is neither measured unit cost nor an upper bound on true unit cost. Show price-month ratios only when requested..

## Offer budget

Report repeat-offer counts without assuming cohort overlap or abuse. Change eligibility only under a supplied policy or evidence from linked offer history, paid retention and contribution; otherwise recommend review, not automatic exclusion. Cancellation remains equally easy.

## No holdout

Without a holdout, say the observed retained share does not establish incremental retention. If the user asks whether to continue an offer, propose a measured comparison briefly. Specify an allocation or sample size only when requested and when baseline, smallest worthwhile effect, available sample and practical constraints are known; use the allocation-aware formula in `references/stats-glossary.md` (or `stats-glossary.md` from this reference). Do not default to 10% or choose an effect for the user. Keep the appropriate paid checkpoint and change one variable at a time.

## Worked example

| | Offered | Holdout (no offer) |
|---|---|---|
| Entered the cancel flow | 360 | 40 |
| Accepted 30% off a $50 plan for 3 months | 90 | — |
| Paying full price in month 4 | 54 | 4 |

- Acceptance: 90/360 = 25.0% [20.8 – 29.7].
- Retained: 54/360 = 15.0% [11.7 – 19.1]; holdout 4/40 = 10.0% [4.0 – 23.1].
- Incremental: +5.0 points, Newcombe [−8.5, +12.3] → effect not established; the holdout of 40 is too small.
- Gross discount cost: maximum 90 × 3 × $50 × 30% = $4,050. Discounted revenue from accepters: at most 90 × 3 × $50 × 70% = $9,450. Net cost: not checked (months 1–3 not given for either arm).
- Point estimate: 0.05 × 360 = 18 extra customers, range −30 to +44 (−8.47 and +12.28 points × 360, before rounding) → $4,050 ÷ 18 = $225 gross each = 4.5 months of full price; not established.
- Accepters who left anyway: not computable (paying status not split by accepted and declined); at least 90 − 54 = 36 of 90 accepters were not paying full price in month 4.
- Holdout size to detect 10% → 15% with a 10% holdout: 400 held out, 3,600 offered, 4,000 cancel sessions. With a 50/50 split: 686 per group.
