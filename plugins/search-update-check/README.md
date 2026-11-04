# Search Update & Traffic Drop Check

Find out whether a Google core update, spam update, a Google Search incident or a Search Console reporting error lines up with the dates your organic traffic, clicks, impressions or rankings fell or rose. The plugin checks your dates against Google's own dated pages and says which case fits, with Google's source link and an as-of date on every answer. It also says whether an update is rolling out now, before a launch or migration, and lists Google's confirmed updates since November 2021.

An independent tool: not affiliated with, endorsed by or sponsored by Google.

## What it does

- **traffic-drop-google-update:** matches the dates of a drop or rise with Google's confirmed ranking rollouts, Search Console data anomalies (days when Google says its reports were wrong) and Google Search ranking, serving, indexing or crawling incidents. It says which of four cases fits: a Search Console reporting error, a Google incident, dates that overlap a Google update, or nothing on Google's side. A reporting error counts only when it affects the metric and report you are looking at. For an overlap it gives the checks that separate the update from site causes, and runs them on your data if you paste it.
- **core-update-rollout-status:** whether a Google update or Search incident is live today, when the last core and spam updates ended, what that means for the before/after numbers of a launch, migration, redesign, content pruning or SEO test, and what to watch during and after the change. There is no «safe» or «unsafe» verdict: an update makes the result of a change harder to read, and you choose.
- **google-update-history:** Google's confirmed ranking updates for a period or of one kind, with rollout start and end dates and Google's link, as a table for a report, chart annotations (rows, CSV or shaded bands on a plot) or a short paragraph for a client.

## Examples

- My organic traffic dropped about 30% around May 25. Was that a Google update?
- We're migrating to a new domain next week. Is Google rolling out an update right now?
- List Google's core updates since 2025 with start and end dates for my client report.

## How it works

Example: Search Console clicks on web search fell from 25 May 2026. The check finds the May 2026 core update, which Google's dashboard lists as rolling out from 21 May to 2 June 2026, so the fall began on day 5 of the rollout. The answer says the timing fits, that overlap alone does not show the update was the cause, and gives the checks that separate it from site causes (whole site or a few templates, Google against other traffic sources, a site change near the date). A fall in web search clicks on 14 August 2026 is not explained by Google's logging error of 13 to 17 August 2026, because that error affected only impressions in the Generative AI report.

Answers never say an update «hit» or «penalized» a site. Only events with a Google source link are confirmed; volatility scores and rumours are never presented as updates.

## Data and network

The plugin connects to one service: a read-only data server at https://black-vector.com/mcp/search-updates, run by the plugin author. It holds Google's public event dates and nothing about you:

- confirmed ranking updates from Google's Search Status Dashboard ranking history, from November 2021;
- Google Search ranking, serving, indexing and crawling incidents from the same dashboard (for example «Ranking is experiencing an ongoing issue», which is an incident, not an update);
- the entries of Google's «Data anomalies in Search Console» help page.

A daily job reads Google's dashboard data and the data anomalies page and merges new or changed entries; no AI model is involved. Every answer from the server carries the date it was last refreshed and the Google page each item comes from.

Each call carries only the tool name and its inputs: dates and, optionally, an update kind. The skills never send your site address, URLs, numbers or text. The server needs no account, sign-in or setup. It does not fetch anything for you, and no skill runs web searches or calls any other service on its own. If you paste Search Console or analytics data, the assistant reads it in the chat; it is not sent to the server.

What the server keeps: see the [privacy policy](PRIVACY.md).

## Troubleshooting

- **«The Google update data could not be reached»:** the server did not answer. The answer still gives the checks that do not need dates and the two Google pages to check by hand: the Google Search Status Dashboard (https://status.search.google.com) and «Data anomalies in Search Console» (https://support.google.com/webmasters/answer/6211453).
- **«The data is from <date>»:** the server could not read Google's pages since that date; events after it are not covered.
- **«Not covered for these dates»:** Search Console data anomalies are kept only for the months Google's page lists, and incidents start in 2023; ranking updates start in November 2021.

## Limits

Google confirms only some ranking changes, and dates that overlap are a lead, not proof. A manual action is not an update; it shows in Search Console under Security & Manual Actions.

## Questions and feedback

If a skill works wrongly for your task, tell me in GitHub Discussions — I read every message: https://github.com/grayskripko/marketing-skills/discussions

Bug reports also work in GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

Sergey Skripko

## License

MIT. See LICENSE.
