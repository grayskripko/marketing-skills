# Metric definitions

Print the definitions box before any rate, with the user's own values where given. Every default is editable and labelled.

## Definitions box

| Term | Default | Source |
|---|---|---|
| Question | a thread starter with is_question = 1 | the user's rule |
| Staff | is_staff = 1 | the user's rule |
| Response | the first reply in the thread by a human who is not the asker (is_bot = 0) | R-TTFR |
| Newcomer | a member whose join_date and first post both fall inside the period | the user's rule |
| Reply window | 7 days after the newcomer's first post | heuristic of this plugin |
| Return | a second post within 30 days of the first | heuristic of this plugin |
| Active member | the user's own rule, stated in words; no default | ground rules |

## Metrics

| # | Metric | Formula | Notes |
|---|---|---|---|
| 1 | Unanswered share | questions with no human response / questions | Wilson interval |
| 2 | Time to first human response | median and 75th percentile of (first human response − question time), over answered questions; also the share of first responses written by staff | R-TTFR; bots excluded |
| 3 | Newcomer reply rate | newcomers whose first post got a human reply within the reply window / newcomers who posted | Wilson interval |
| 4 | Newcomer return by reply | return rate for replied vs not replied, each with k/n and Wilson interval, and the difference with its Newcombe interval | "association, not proof" |
| 5 | Staff share | staff replies / human replies; staff thread starters / thread starters | Wilson interval |
| 6 | Concentration | share of non-staff human posts by the top 1% and top 10% of non-staff posters (round the poster count up); contributor absence factor (smallest number of members making half of non-staff posts) | R-CAF; "your community's own split; 90-9-1 is rough and varies" (R-NNG) |
| 7 | Join-month cohort table | per join month: joined → posted → got a reply in the window → returned, each step k/n with interval | "thin sample" where n < 20 |

Comparison only with the same community's earlier periods. No outside benchmarks.

## Read-out

At most three findings, ordered by size of the effect with its interval. Each: the number, what it means in one sentence, one action, the number that should move, the date to measure again, and one SPACES outcome (R-SPACES: Support; Product ideation and feedback; Acquisition and advocacy; Content and contribution; Engagement; Success).

"Not knowable from this export" box: why people leave, satisfaction, outside reputation, anything that needs message text, outside traffic or revenue.
