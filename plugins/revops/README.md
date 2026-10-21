# RevOps Metrics & Forecast Accuracy

Revenue operations (RevOps) numbers you can recompute from data you paste. Each figure shows its calculation; rates from small samples are shown as k of n with a range.

Example: your CRM says deals at Stage 3 win 60% of the time. Your closed deals say 28%.

| Stage | Stated | Closed deals that reached it | Won | Observed | 95% range |
|---|---|---|---|---|---|
| Stage 3 | 60% | 50 | 14 | 14 of 50 (28.0%) | 17.5% – 41.7% |

## What it does

| Skill | Give it | You get |
|---|---|---|
| stage-calibration | stage probabilities, closed-deal counts or rows, stage definitions | observed win rate per stage as k of n with a range, open deals left out, and a review of each stage definition you supply |
| arr-bridge | revenue by account by period | a bridge that reconciles to the reported end, gross and net revenue retention (GRR, NRR) over the starting accounts |
| forecast-backtest | past forecasts and what actually closed | signed error per period, average miss and whether each method ran high or low; each period shown when there are few |
| revenue-plan | a target with your rates or team | deals, opportunities, SQLs and leads per month shifted by the cycle, coverage, team capacity |
| funnel-math | lead or deal rows with dates | conversion by entry cohort as k of n; time between steps; time to first contact against your target; source or segment comparisons; velocity |

## Examples

- "Our Stage 3 is set to 60%. Last year 50 closed deals reached it and 14 were won. Is 60% right? Show the math."
- "Which forecast was closer? Actual / forecast A / forecast B per quarter (k): 420/520/440, 510/590/470, 0/60/30, 460/560/480."
- "Target $600k new ARR next quarter. Avg won deal $18k, won 22% of opps, SQL→opp 40%, cycle 60 days. SQLs per month?"

## How it works

Each skill gives the answer first, then the calculation behind it. It first checks whether your inputs can all be true together and leads with any conflict. Your numbers are kept as given and there are no benchmarks.

## Data and network

Network scope: this plugin fetches nothing and runs no web search. It works only on data you paste or attach, runs no scripts of its own, changes no files or settings unless you ask, and uses the assistant's code or spreadsheet tool to compute the tables it shows.

## Personal data

Exports can contain owner or contact names. The skills do not need them; remove those columns before pasting. See PRIVACY.md.

## What it will not do

Walk through deals one by one, run what-ifs on a single deal slipping, clean CRM fields, write forecast commentary, prioritise individual leads, rank people for dismissal, give financial or accounting advice, or quote benchmark figures.

## Troubleshooting

If a figure depends on an input you did not give, it is shown as a range at that input's bounds. A wide range on a rate means the sample is small.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.
