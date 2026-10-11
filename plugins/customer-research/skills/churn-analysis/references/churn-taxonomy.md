# Churn taxonomy

Keep stated reasons and supported secondary/interacting explanations. Assign a primary cause only when supported; otherwise mark it unknown. Assess controllability separately against feasible action, resources, time horizon and customer circumstances when useful. CH and LD codes are internal; name reasons in words in the answer.

| Code | Starting reason category |
|---|---|
| CH1 | price or budget |
| CH2 | value not reached (never set up, never adopted, results not seen) |
| CH3 | missing capability |
| CH4 | product quality (bugs, downtime, speed) |
| CH5 | moved to an alternative |
| CH6 | business event (closed, merged, downsized, champion left) |
| CH7 | service or support |
| CH8 | other or unclear |

## Stated vs evidenced reason

When the notes, usage details or follow-up say more than the one-line reason, record both.

| Id | Stated reason | Evidenced reason | Evidence |
|---|---|---|---|
| C07 | "too pricey" (price) | possible value-not-reached explanation; price may also contribute | notes: setup never finished; 2 logins in 60 days |

Count stated reasons and evidence patterns separately. Where causation is not confirmed, label inferred causes as hypotheses and retain competing or interacting explanations; do not replace a stated price reason merely because usage is low.

## Decided vs cancelled

When the text shows when the customer decided to leave (often weeks before cancelling), record both dates or events. Use an evidenced decision moment to frame follow-up questions. Discuss possible intervention timing only when requested or decision-relevant, as a hypothesis rather than proof of an effective fix.

## Signals (heuristics from practitioners, not laws)

- Churn concentrated among new customers points at onboarding or at acquiring the wrong customers.
- Rising churn among long-tenure customers points at core value breaking or a stronger alternative.
- Price with low use may indicate value not reached, unaffordability or both; investigate the sequence rather than assuming causation.

## Lost deals (separate table)

Lost deals were never customers. Give them L01… ids and code them in their own table, never counted with cancellations and never given cancellation reasons, tenure bands or a controllable-by-onboarding flag.

| Code | Reason |
|---|---|
| LD1 | price or budget |
| LD2 | poor fit (needs, size, industry) |
| LD3 | chose an alternative |
| LD4 | timing |
| LD5 | no decision |
| LD6 | other or unclear |

## Never

- Count lost deals together with cancellations.
- Average across reasons or across segments without printing the segment table.
- Produce churn scores, probabilities or predictions.
