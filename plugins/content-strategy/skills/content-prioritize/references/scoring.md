# Planning score

Six criteria, each 0, 1 or 2. Total 0 to 12. Label it "planning score, not a traffic forecast". All thresholds are heuristics of this plugin.

| Id | Criterion | 2 | 1 | 0 |
|---|---|---|---|---|
| C1 | Business fit | leads directly to an offer or conversion point the user named | related to such an offer but indirect | no link to an offer |
| C2 | Stage fit | matches a buyer stage the goal needs | adjacent stage: one step away | two or more steps away |
| C3 | Evidence readiness | supplied material supports the proposed central claim | relevant material exists but the claim needs verification or collection | no relevant support supplied |
| C4 | Demand evidence supplied by the user | two or more kinds (for example sales questions, support tickets, interviews where customers raised the topic unprompted) | one kind | none given (never invented) |
| C5 | Effort | 4 hours or less | more than 4, up to 8 hours | more than 8 hours |
| C6 | Reuse | feeds two or more other planned pieces or channels the user named (a planned piece counts without named channels) | one | none |

Goal to stage: demo or sales requests → vendor choice and solution aware; awareness or newsletter growth → problem aware; retention or expansion → onboarding and expansion.

Stage steps, in order: problem aware → solution aware → vendor choice → onboarding and expansion. The distance is the number of steps to the nearest stage the goal needs: one step = adjacent (1), two or more = 0.

## Capacity

Calculate availability only from known hours and horizon. Hours per week x weeks = total hours. Reserve: the share and purpose the user names; otherwise 20% for edits and distribution (a provisional planning allowance). Writing hours = total hours x (1 - reserve share). Reserved hours are used only for their stated purpose; leftover hours are shown as spare. Unknown capacity calls for one bounded first assignment and an actual-time checkpoint, not assumed staffing or quarterly totals.

## Numbers, ties and ranks

- Compare with thresholds before any rounding.
- Totals print as integers. Derived numbers (hours) print with one decimal, rounded half away from zero.
- Order by total (high first), then C1 (high first), then hours (low first), then input order.
- Rank numbers are shared only when total, C1 and hours are all equal: 1, 2, 2, 4.

## Filling the plan

Take topics in order. Topics without relevant support are deferred unless the user requests a useful supported synthesis or evidence-gathering step. Publish result-based pieces only after the central result is verified. Add work only when its hours fit the available production time; otherwise defer it. With unknown capacity, give a first assignment rather than a timed calendar.

Reason for every not-now topic, the first that applies: "generic: no evidence of your own" (C3 = 0), "no business fit" (C1 = 0), "over capacity".

Swap option: when a topic left out as "over capacity" has a strictly higher total than at least one planned topic (ties do not count), name the planned pieces that would have to go to fit it, lowest-ranked first, with their totals and hours. Recheck the swapped plan like the main one: hours within the writing hours, pieces counted right. The user decides.
