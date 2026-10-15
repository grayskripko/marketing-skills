# Test math

Use when the decision turns on it or the user asks whether a volume is enough. When a count goal or a rule set before launch already decides, an interval adds nothing.

## Is this volume enough?

Take a low and a high rate from the user's own data. For each: expected count = n × p; chance of zero = (1 − p)^n; chance of at least k from the binomial (for k = 2: 1 − (1 − p)^n − n·p·(1 − p)^(n−1)). Say which outcome would change the decision.

## Count goals at small volume

When the reach available is small, a test cannot estimate a rate. It can still answer "did at least k happen by the read date?".

- k comes from the user's goal, or from spend ÷ the most a customer may cost, rounded up.
- Stop at zero (or one) outcome after all outcomes mature.
- To make a rate readable later: more reach, a longer window, or measuring an earlier step that happens more often.

## Zero events

Zero successes out of n is not proof of a zero rate. A quick upper bound is about 3 ÷ n (rule of three). Compare it with the lowest rate that would still pay back; if the bound is already below it, stopping is safe; otherwise the result is inconclusive.

## When a rate really matters

If the user asks for precision, or a scale decision depends on whether a rate is above a line, use the Wilson 95% interval: p = k ÷ n, z = 1.96, centre = (p + z²/(2n)) ÷ (1 + z²/n), half-width = z × √(p(1 − p)/n + z²/(4n²)) ÷ (1 + z²/n). Check values: 5/18 → 12.5%–50.9%; 0/120 → 0.0%–3.1%.

## How much more volume

At observed rates, the reach needed for k outcomes = k ÷ (outcomes ÷ reach so far). Example: 2 paying from 18 stores; 5 paying would need about 5 ÷ (2 ÷ 18) = 45 stores. This is a scenario, not a requirement; decide the next batch from its cost and hours.
