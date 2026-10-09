# RevOps Metrics Kit

Revenue numbers you can recompute. Every figure comes with its formula, and every rate with its sample size and a 95% range, calculated from data you paste.

Example: your CRM says deals at Stage 3 win 60% of the time. Your closed deals say 28%.

| Stage | Stated | Reached | Won | Observed | 95% range | Verdict |
|---|---|---|---|---|---|---|
| Stage 3 | 60% | 50 | 14 | 28.0% | 17.5% – 41.7% | stated outside range |

## What it does

| Skill | Give it | You get |
|---|---|---|
| stage-calibration | stage probabilities, closed-deal counts or rows, stage definitions | observed win rate per stage with a 95% range, open deals left out, and a ten-point check of your written stage definitions |
| arr-bridge | revenue by account by period | a bridge that reconciles to zero, gross and net revenue retention (GRR, NRR) over the starting customers, customer-count churn |
| forecast-backtest | past forecasts and what actually closed | how far each method missed each period, its average miss and whether it ran high or low, and a warning when there are too few periods |
| revenue-plan | a target with your rates or team | deals, SQLs, leads and people per month with lag, coverage, capacity gap |
| funnel-math | lead or deal rows with dates | conversion by the month or quarter leads came in, with a 95% range; time to first contact by source; segment view; velocity |

## Examples

- "Our Stage 3 is set to 60%. Last year 50 closed deals reached it and 14 were won. Is 60% right? Show the math."
- "Which forecast was closer? Actual / forecast A / forecast B per quarter (k): 420/520/440, 510/590/470, 0/60/30, 460/560/480."
- "Target $600k new ARR next quarter. Avg won deal $18k, won 22% of opps, SQL→opp 40%, cycle 60 days. SQLs per month?"

## How it works

Each skill gives the answer first, then the calculation behind it and a short check of whether the data can be trusted. Your numbers are never changed and there are no benchmarks. Results are grouped by stage, segment, source or period; per-person figures only on request, under anonymous labels.

## Data and network

Network scope: this plugin fetches nothing and runs no web search. It works only on data you paste or attach, runs nothing and changes no files or settings unless you ask, and may use the assistant's code or spreadsheet tool to compute the tables it shows.

## Personal data

Exports can contain owner or contact names. The skills ignore them and never repeat them; remove those columns before pasting if you can. See PRIVACY.md.

## What it will not do

Walk through deals one by one, run what-ifs on a single deal slipping, clean CRM fields, write forecast commentary, prioritise individual leads, rank people for dismissal, give financial or accounting advice, or quote benchmark figures.

## Troubleshooting

"Not checked" names the missing column. A wide 95% range means too few records.

## Support

Open an issue at https://github.com/grayskripko/marketing-skills/issues.

## License

MIT, see LICENSE.
