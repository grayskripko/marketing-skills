# Affordability chain

How much one customer may cost, and what that means per signup, per click and per person reached. Built only from the user's numbers or labelled assumptions; no ratio rules of thumb.

## Affordable cost per customer

The contribution a customer brings inside the payback window:

```
subscription:  affordable = price per month × gross margin × window months
one-off sales: affordable = order value × gross margin × orders per customer inside the window
```

- Window: the user's; otherwise 12 months, stated in the answer as a plain assumption ("I assumed a 12-month window"), with a note that a shorter window makes every line below stricter.
- Gross margin: the user's; if missing, the chain is printed on an assumed margin, named in the Assumptions box, and every evidence grade is capped at D.
- Orders per customer inside the window: the user's; otherwise an assumption, printed.
- Yearly billing: use the yearly price × margin, counted once per year the window covers (cash basis: a yearly payment inside the window counts in full).
- Churn inside the window is ignored unless the user gives it; with monthly churn c over a window of w months the subscription line becomes price × margin × (1 − (1 − c)^w) ÷ c.
- A lifetime value from churn is used only when the user asks for it; then the horizon is capped at 36 months and labelled, because dividing by a small churn rate produces very long lifetimes nobody has observed.

Monthly wording ("per month") is used only for subscriptions; one-off businesses get per-order wording.

## Discounts, free periods and rewards

A discount or free period costs the revenue given up, not the contribution: a free month on a $39 plan costs $39, because the cost of serving the customer is paid either way. A free month to both the referrer and the referred customer costs $78. Compare the reward cost per referred customer with the affordable cost on that basis.

## The chain

Each line multiplies the one above by the next rate down the path:

| Line | Formula |
|---|---|
| Per customer | affordable (above) |
| Per signup or trial | per customer × signup-to-paid rate |
| Per visit or click | per signup × visit-to-signup rate |
| Per person reached | per visit × reach-to-visit rate |

Rates: the user's observed rates first, then rates the user states as guesses, then the plugin's labelled assumptions ("assumption, change me"). **An observed rate always replaces an assumed one**: after a test, recompute every ceiling with what was observed. A ceiling computed from an assumed rate is never compared with an observed cost without saying so.

## Break-even for one idea with a known cost

| Line | Formula | Note |
|---|---|---|
| Customers needed | cost ÷ affordable per customer | print unrounded, then rounded up |
| Customers expected | reach × each rate down the chain | unrounded |
| Share of cost returned in the window | expected × affordable per customer ÷ cost | percent, one decimal |
| Shortfall | needed (unrounded) − expected | |
| Cost per person reached | cost ÷ reach | next to the affordable per person reached |
| Rate multiple needed | cost per person reached ÷ affordable per person reached | how many times higher the combined rate must be |

Rounding: keep unrounded values through every step; round counts of customers up only when printing; money to cents; compare with a line before rounding.

## Gate wording

- The user gave a cost and it is more than the user's marketing cash for the whole window: "fails on your quote (cash)".
- The user gave a cost and the cost per expected customer is above the affordable cost **at rates the user observed**: "fails on your quote".
- The user gave a cost and it misses only at assumed or guessed rates: "unknown: misses at assumed rates (share returned X%)". This sends the idea to Test small first and allows it as a probe; it is never "fails on your quote".
- The user gave a cost and it fits: "passes on your quote at the assumed rates", naming which rates are assumed (at observed rates: "passes on your quote").
- No cost given: "unknown: hold a quote against these lines", followed by the per-customer, per-signup and per-click lines.

## Worked example: a newsletter sponsorship

Inputs from the user: $39 a month plan, 85% margin, 6-month window, a 3,000-reader newsletter quoting $1,200. Rates stated by the user as guesses: 2% of readers click, 10% of visitors start a trial, 40% of trials pay.

- Per customer: 39 × 0.85 × 6 = $198.90.
- Per trial: 198.90 × 0.40 = $79.56.
- Per click: 79.56 × 0.10 = $7.956, printed $7.96.
- Per reader: 7.956 × 0.02 = $0.15912, printed $0.16. The quote is 1,200 ÷ 3,000 = $0.40 per reader.
- Customers needed: 1,200 ÷ 198.90 = 6.03, so 7. Expected: 3,000 × 0.02 × 0.10 × 0.40 = 2.4. Shortfall 3.6.
- Returned within six months: 2.4 × 198.90 = $477.36, which is 39.8% of $1,200: about two-fifths.
- Rate multiple needed: 0.40 ÷ 0.15912 = 2.51.

Reading: at these guessed rates the sponsorship returns about two-fifths of its cost within six months; it would pay back if each reader cost $0.16 or less, or if the combined rate were about 2.5 times higher. The guesses are the weakest part, so the cheapest test is a smaller slot that measures the click and trial rates.

## Worked example: one-off orders

A candle shop: average order $32, 60% margin, customers order 1.5 times within 12 months (the user's figure). Affordable per customer: 32 × 0.60 × 1.5 = $28.80. Every later line uses orders, not months.
