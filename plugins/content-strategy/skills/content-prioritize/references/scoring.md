# Planning score

Six criteria, each 0, 1 or 2. Total 0 to 12. Label it "planning score, not a traffic forecast". All thresholds are heuristics of this plugin.

| Id | Criterion | 2 | 1 | 0 |
|---|---|---|---|---|
| C1 | Business fit | leads directly to an offer or conversion point the user named | related to such an offer but indirect | no link to an offer |
| C2 | Stage fit | matches a buyer stage the goal needs | adjacent stage: one step away | two or more steps away |
| C3 | New information | a named source the company already holds (own data, customer case, interview, expert) | a source that must be collected first | none: commodity |
| C4 | Demand evidence supplied by the user | two or more kinds (for example sales questions and support tickets) | one kind | none given (never invented) |
| C5 | Effort | 4 hours or less | more than 4, up to 8 hours | more than 8 hours |
| C6 | Reuse | feeds two or more other planned pieces or channels the user named | one | none |

Goal to stage: demo or sales requests → vendor choice and solution aware; awareness or newsletter growth → problem aware; retention or expansion → onboarding and expansion.

Stage steps, in order: problem aware → solution aware → vendor choice → onboarding and expansion. The distance is the number of steps to the nearest stage the goal needs: one step = adjacent (1), two or more = 0.

## Capacity

Hours per week x weeks = total hours. Reserved share for updates and distribution: 20% by default (heuristic; the user can change it). Production hours = total hours x (1 - reserved share).

## Numbers, ties and ranks

- Compare with thresholds before any rounding.
- Totals print as integers. Derived numbers (hours) print with one decimal, rounded half away from zero.
- Order by total (high first), then C1 (high first), then hours (low first), then input order.
- Rank numbers are shared only when total, C1 and hours are all equal: 1, 2, 2, 4.

## Filling the plan

Take topics in order. Commodity topics (C3 = 0) are skipped unless the user asks for them. Add each other topic if its hours fit the production hours left; otherwise it goes to not now and the next topic is tried. Stop when nothing else fits.

Reason for every not-now topic, the first that applies: "commodity" (C3 = 0), "no business fit" (C1 = 0), "over capacity".

Swap option: when a topic left out as "over capacity" has a higher total than at least one planned topic, name the planned pieces that would have to go to fit it, lowest-ranked first, with their totals and hours. The user decides.
