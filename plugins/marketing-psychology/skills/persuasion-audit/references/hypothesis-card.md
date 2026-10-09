# Hypothesis card

Use this instead of predicting a result, and only when the user plans to test a change or asks about lift: one card, for the top change. Test design, sample size and readouts are out of scope for this plugin.

```
Hypothesis: Because [mechanism, study (authors, year), grade in words] addresses [barrier, quoted from the input],
changing [one element: before -> after] should raise [primary metric] for [segment].
Legitimate only if: [the fact that must be true]
Variant: one change against the current version
Guardrails: [pick: refunds, cancellations within 30 days, chargebacks, complaints, unsubscribes]
Decision rule: a lift on the primary metric together with a guardrail breach counts as a failed test.
How to test: To size and read this test, use a conversion-rate-optimisation (A/B testing) skill, a sample-size tool or your experimentation platform.
Feasibility: 126 trials run by two government nudge units averaged +1.4 percentage points, an 8.0% relative
increase (DellaVigna & Linos 2022); that is no forecast for this change. Effects that small need large samples; on low traffic, ship only honest,
low-risk changes and claim no lift. Changes that remove a blocking step (a hand-off, a missing permission,
a hidden step) are not covered by that average; size the test from your own baseline with a sample-size tool.
```

Rules:
- One mechanism and one change per card. Name the study (authors, year) and the grade in words; never print a ledger id. For a friction or enablement fix write "removes a step; no effect size claimed".
- Guardrails come from L31: a change that lifts sign-ups while raising refunds or complaints has not worked.
- Never add a sample size, duration, power figure or significance threshold.
- When the evidence grade is D, do not write a card; say why and suggest a change with a better-supported mechanism or a friction fix.
