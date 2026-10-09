# Save-offer measurement

## The checkpoint

The outcome is "paying full price in the first billing cycle after the discount or pause ends". For a 3-month discount on monthly billing that is month 4; for an annual plan it is the next annual renewal after the discounted one. If the data stops earlier, label the retained and incremental columns "end of discount, not yet net", print only the acceptance rate, and put the headline under Not checked.

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
- Net cost = (revenue per holdout member − revenue per person offered) × number offered, revenue counted from the offer month through the checkpoint. Negative = net gain. It needs month-by-month paying status for both arms. When that is missing, label the discount cost "gross", print the discounted revenue collected from accepters (at most accepters × months × list price × (1 − discount share)), and put the net cost under Not checked. Without that status the net cost can be higher or lower than the gross figure; do not say which.
- Incremental customers (point estimate) = incremental retention × number offered, with its range (the two ends of the incremental-retention range × number offered).
- Cost per incremental retained customer = discount cost ÷ incremental customers, also shown as months of full price (cost ÷ price). Print it only next to the interval, labelled "point estimate"; if the interval includes 0, add "the true number could be zero, so this cost per customer is not established".

## Offer budget

Accounts that took any offer more than once in 12 months are counted as "exclude from offer eligibility". This changes who sees an offer; it never refuses, delays or complicates their cancellation.

## No holdout

Print: "Retained share is an upper bound; it includes people who would have stayed anyway." Then one holdout line: share of sessions held out (10% default, editable) and the sample size for the smallest effect the user cares about, for that split (formula in `stats-glossary.md`; never divide the equal-split figure by the holdout share). Full test design is out of scope; the next round changes one variable, keeps a holdout and uses the full-price checkpoint.

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
