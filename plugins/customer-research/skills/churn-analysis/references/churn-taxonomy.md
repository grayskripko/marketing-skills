# Churn taxonomy

Each record (C01…) gets one primary reason, optional secondary reasons, and a controllable flag.

| Code | Reason | Controllable |
|---|---|---|
| CH1 | price or budget | partly |
| CH2 | value not reached (never set up, never adopted, results not seen) | yes |
| CH3 | missing capability | yes |
| CH4 | product quality (bugs, downtime, speed) | yes |
| CH5 | moved to an alternative | partly |
| CH6 | business event (closed, merged, downsized, champion left) | no |
| CH7 | service or support | yes |
| CH8 | other or unclear | — |

## Stated vs evidenced reason

When the notes, usage details or follow-up say more than the one-line reason, record both.

| Id | Stated reason | Evidenced reason | Evidence |
|---|---|---|---|
| C07 | "too pricey" (CH1) | value not reached (CH2) | notes: setup never finished; 2 logins in 60 days |

Count evidenced reasons in the main table when they exist; keep the stated reasons in a second column so the difference is visible.

## Decided vs cancelled

When the text shows when the customer decided to leave (often weeks before cancelling), record both dates or events. The decision moment is where the fix belongs.

## Signals (heuristics from practitioners, not laws)

- Churn concentrated among new customers points at onboarding or at acquiring the wrong customers.
- Rising churn among long-tenure customers points at core value breaking or a stronger alternative.
- "Price" together with low use usually means value not reached.

## Lost deals (separate table)

Lost deals were never customers. Give them L01… ids and code them in their own table, never counted with cancellations and never given CH codes, tenure bands or a controllable-by-onboarding flag.

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
