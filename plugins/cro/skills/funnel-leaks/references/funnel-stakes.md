# Funnel stakes

## Intake

Counts per step for one period, in one unit (visitors, users or sessions), optionally split by device, source or segment, optionally with the same counts for an earlier period. A visitor-, session- or event-level export is not processed (ground rule 9); ask for this table instead:

| Step | Segment | Count this period | Count earlier period (optional) |
|---|---|---|---|

## Data gate

Stop and say why when:
- units are mixed (sessions at one step, users at the next);
- a count rises down the funnel and the step is not optional or a re-entry point;
- the steps are not in one fixed order.

Note, without stopping:
- a tracking or consent-banner change inside the period;
- bot and internal traffic filtering unknown;
- the newest days still maturing (visitors who have not had time to reach the goal).

## Step table

For each step: entrants, continuers, step rate with a Wilson 95% interval (`rates-and-intervals.md`), people lost (entrants − continuers), and the downstream rate from the next step to the goal (1 for the last step).

## Segment gaps

For each step and split: segment rate with interval; the gap to the comparison segment with a Newcombe 95% interval. A segment below n = 20 is "thin sample" and never ranked.

## Mix-shift check (Simpson's paradox)

When an earlier period is given and a split exists: if the pooled rate moved but each segment's rate did not (every segment's own difference interval includes 0), the change comes from a shift in traffic mix, not from the page. Print "traffic mix changed; the page did not get worse in any segment".

Example: earlier period mobile 80/4,000 = 2.0%, desktop 240/6,000 = 4.0%, pooled 3.2%. This period mobile 140/7,000 = 2.0%, desktop 120/3,000 = 4.0%, pooled 2.6%. The pooled drop of −0.60 pp [−1.07 – −0.13] is real, yet neither segment changed: mobile went from 40% to 70% of traffic.

## Conversions at stake (needs a reference)

```
stake at a step = entrants at the step × (reference rate − current rate) × downstream rate to the goal
```

The reference must be one the user can point to:
- the stronger segment at the same step (for example desktop when mobile is examined);
- the same step in an earlier period;
- a target the user names.

A negative stake prints as 0, "at or above the reference". Every stake is labelled "upper bound, not a forecast": it assumes the whole gap could be closed and that the people won would convert downstream like those already there.

Example (segment reference): checkout start → order, mobile 840/2,400 = 35.0% against desktop 572/1,100 = 52.0%; the gap is +17.0 pp [+13.5 – +20.5]; stake = 2,400 × 0.17 × 1 ≈ 408 orders in the period, upper bound.

Example (earlier-period reference): visit 20,000 → pricing 6,000 (30.0%) → signup start 1,500 (25.0%) → signup done 900 (60.0%) → paid 90 (10.0%); earlier rates 31% / 28% / 61% / 11%.

| Step | Stake |
|---|---|
| pricing → signup start | 6,000 × 0.03 × 0.06 = 10.8 |
| signup done → paid | 900 × 0.01 × 1 = 9.0 |
| visit → pricing | 20,000 × 0.01 × 0.015 = 3.0 |
| signup start → done | 1,500 × 0.01 × 0.10 = 1.5 |

## Without a reference: no ranking by counts

Without a reference, steps are not ranked by any count. They are ordered by:
1. evidence: Seen or Data issues found at that step by a page or flow audit;
2. testability: the affordable lift at 4 weeks given the step's weekly entrants (`test-math.md`).

Why counts alone do not rank. In a chain of multiplied rates, raising any one step's rate by the same relative amount raises final conversions by that same share. So "most people lost" always points at the top of the funnel, where the counts are largest, and "people lost × downstream rate" always points at late steps with low rates, because it measures the gain if that step reached 100%. Neither says where a fix is likely or cheap. Both columns may be shown; neither is presented as a ranking.

## Next step per leak

For each leak worth acting on: which audit next (page or flow), one research method (`ship-test-research.md`), and whether an A/B test is feasible at that step's traffic.
