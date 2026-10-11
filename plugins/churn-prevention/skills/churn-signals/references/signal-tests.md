# Method for testing signals in the user's account history

## Windows

- Cut-off date: the end of the observation window. Signals are measured only up to it.
- Outcome window: starts after the cut-off; an account counts as churned if it cancelled inside it, active otherwise.
- Remove and list any signal dated after the cut-off or after the account's cancel request (leakage). A screen seen during cancelling is an outcome, not a predictor.

## Signal table (one row per signal)

| Signal | Fired n | Churn if fired | Churn if not fired | Difference [95% range] | Lift | Recall | Median lead (days, n) | Verdict |
|---|---|---|---|---|---|---|---|---|

Precision equals churn if fired, so it gets no column.

Assess association and actionability separately. Show the fired and not-fired counts and the difference interval; an interval including zero means the difference is not established. Flag small samples for caution, not automatic exclusion or a ban on individual review. Assess response time using the user's supplied latency and the count with sufficient lead time. If either is missing, ask for it and leave actionable coverage unresolved; do not assume 14 days or infer coverage from a median. Distinguish a review candidate from an automated intervention: deployment also needs validation, cost and intervention-benefit evidence.

## One-action threshold search

For one key action counted in the first K weeks (the user names the action and K):
- Retention for accounts at or above each cut-off vs below it, every cut-off with n and interval.
- Print how many cut-offs were tried; the more you try, the more likely one looks good by chance.
- Keep small groups visible with counts and uncertainty. Assess interval width, event counts, useful effect and action cost; do not reject a cut-off solely because one side has fewer than 20 accounts. Validate searched cut-offs before deployment.
- Label any knee "found in this data; test before use". It is a correlation until an experiment moves people across it.

## Score check (only when the user gives a formula or scores)

Churn rate by score band with intervals. A band that churns less than a band with a better score is flagged "non-monotonic". Weights are never invented or tuned here.

## Natural cadence

Judge inactivity against how often the customer's need recurs (weekly payroll, monthly reporting, yearly tax). A gap shorter than that cadence is not a signal.

## Watch rules

At most three. Distinguish low-risk individual review from automated rules; state evidence, response time and any missing actionable-coverage or intervention-benefit data for each. Each: trigger, owner role, action, what to measure, and when to re-test.

## Caveats

- State beside affected claims that association does not establish intervention benefit; identify missing intervention evidence when recommending action.
- Only when cohorts are compared: older cohorts look healthier because their least committed members already left (Fader & Hardie 2007, "How to project customer retention", Journal of Interactive Marketing 21(1)).
- Only when seat removals are a signal: they are covered as a signal only; contraction revenue is out of scope.

## Worked example

500 accounts active on 1 January; 60 cancelled by 31 March: 60/500 = 12.0% [9.4 – 15.1].

| Signal | Fired | Churn if fired | Churn if not | Difference | Lift | Recall | Lead | Verdict |
|---|---|---|---|---|---|---|---|---|
| Seats removed in December | 50 | 20/50 = 40.0% [27.6 – 53.8] | 40/450 = 8.9% [6.6 – 11.9] | +31.1 points [18.4, 45.1] | 4.5 (base 12.0%) | 33.3% | 41 | review candidate; actionable coverage requires response time and enough-lead counts |
| Data export started | 30 | 18/30 = 60.0% [42.3 – 75.4] | 42/470 = 8.9% [6.7 – 11.9] | +51.1 points [33.1, 66.6] | 6.7 (base 12.0%) | 30.0% | 2 | review candidate; actionable coverage requires response time and enough-lead counts |
| Cancel-confirmation page viewed | — | — | — | — | — | — | — | leakage, removed |
