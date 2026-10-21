---
name: price-framing
description: "Any question about how the user's own prices or plans are presented, even a quick one-liner: $49 or $50, show the annual discount as a percent or dollars, is the middle plan a decoy, what does this annual price work out to per month. Checks how prices are presented, with the arithmetic shown. Takes tiers, seats, features, monthly and annual prices, discounts or trial terms; recomputes them (per month, per seat, annual saving, months free, per day), reads which price anchors and which plan is pre-selected, tests whether any tier is a decoy, and checks price endings and percent vs amount discounts. Use when the user asks to check the prices, tiers, anchoring, decoys or discount framing on a pricing page or paywall. Whether a 'was' price, fee or trial term is allowed goes to dark-patterns-check. Evaluates the prices given; does not propose new prices unless asked, write the pricing page or predict a lift."
---

# Price framing

Check how prices and plans are presented, with the arithmetic shown.

- Recompute every saving, per-month, per-seat and per-day figure from the user's prices, and keep the prices as given.
- A tier is a decoy only if it is worse than or equal to the target on every listed attribute, price included, and not simply worse than both other options. Keep a decoy apart from anchoring, middle-option framing and defaults.
- Say which price anchors the table and which plan is pre-selected or highlighted. Compare percent and amount framing of the same discount, and convert an annual discount to months free.
- The left-digit effect needs the leftmost digit to change ($79 vs $80 does; $74 vs $75 does not).
- Do not propose new prices unless asked. Give replacement labels or copy that uses the user's figures, and if the question is which version sells more, the experiment and the metric that would answer it.

## How to answer

- Lead with what the user asked for: the verdict, the number, the fixed copy or the first change. Keep it as short as the request allows; add a section only if it changes what the user will do.
- Use the user's facts, numbers and wording. Recheck their arithmetic and show the formula when a figure matters.
- Stay inside the request. No unrequested research references, legal disclaimers, risk labels, guardrail lists or follow-up projects.
- When copy needs fixing, give replacement copy that is ready to paste and built from the user's facts. If a fact is missing, use one clearly named placeholder.
- If an element is already accurate and does its job, say keep it. Mark small optional improvements as optional, not as fixes.
- Never write fake reviews, counters, stock levels, deadlines, "was" prices or statistics. If asked for one, say in one sentence you won't, then give the honest version that serves the same goal.
