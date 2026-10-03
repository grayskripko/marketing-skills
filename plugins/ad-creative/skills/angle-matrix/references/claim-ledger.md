# Claim ledger

The ledger lists every checkable statement in the ad, says what kind of proof it needs and whether the user has it. It never weakens a claim on its own: the user decides whether to supply proof, rewrite or drop.

## Claim types

| Type | Spotted by | Proof that answers it |
|---|---|---|
| Rank or superlative | best, #1, top, leading, fastest, most popular | a named, dated source that measured the ranking, covering the same market and period |
| Endorsement | recommended by, trusted by, used at, expert or celebrity names | a written record of the endorsement and permission to use it; any paid or family link disclosed |
| Outcome | results, time to result, savings, "in 7 days" | data from the product's actual users or a test, plus what a typical user gets |
| Statistic | percentages, counts of customers or hours | the dataset or survey, its size (n), date and who ran it |
| Price or discount | % off, from $X, save, was/now | the current price list and the dates the offer runs; for "was" prices, when that price was really charged (UK-CAP-3.39) |
| Free | free, free trial, no card | the terms showing nothing is charged beyond delivery or reply cost |
| Time limit or scarcity | today only, ends Sunday, few left | the real end date or stock count |
| Review or rating | 4.6/5, "customers say", quotes | the review source, count, date range, and how reviews were collected |
| Environmental (EU audience) | eco, green, sustainable, carbon neutral | a recognised ecolabel or certification scheme; no offset-based product claims |
| Comparison | than X, unlike others | a like-for-like test of the same need, verifiable features |

## Evidence classes

| Class | Meaning | Ledger status |
|---|---|---|
| none | nothing supplied | Hold |
| stated | the user asserts it in chat ("we have 1,200 reviews"); text that appears only inside a pasted ad is class none until the user confirms it | Hold for rank, endorsement, outcome, rating, statistic and environmental claims; Ready for prices, dates and free terms the user controls, marked "user-stated" |
| document | the user names a document they hold (survey file, price list, contract) | Ready, with "keep this on file" |
| third-party | an independent, named, dated source | Ready, with the source and date printed next to the claim |

## Ledger table (output format)

| # | Claim text | Type | Fact id | Evidence class | Rule ids | Status | What would clear it |
|---|---|---|---|---|---|---|---|

## Rules for the writer skills

- Each fact the user gives becomes F1, F2… and is quoted exactly; numbers are not rounded up, and hedges are kept ("about 2 minutes" never becomes "2 minutes" or "seconds").
- A survey figure carries its n and year in a footnote line (for example "Survey of 48 customers, 2026").
- A missing fact becomes `[proof needed: …]` in the copy and a Hold row in the ledger.
- Typical-results line: when copy cites a standout customer result, add what users generally get, or Hold.
- Disclosure line: creator or customer content made under any payment or perk carries the connection inside the ad (US-FTC-END).

## Hold logic

- A Hold is never cleared by the model. The line stays on Hold until the user supplies the evidence or removes the claim.
- If the user asks for a version without the claim, drop the claim entirely. Do not swap in a vaguer phrase that implies the same thing ("one of the top apps" for "#1").
- A line drafted from a user-stated price, date or free term carries "user-stated — keep the terms on file".
