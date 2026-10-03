# Dated items

## Kinds

| id | Kind | Examples |
|---|---|---|
| RF-01 | absolute dates and years | "in 2023", "since March 2022", "© 2024" |
| RF-02 | relative time | "last year", "recently", "this autumn", "new", "upcoming", "two years ago", "this quarter" |
| RF-03 | statistics and survey figures | "72% of members", "a 2023 survey" |
| RF-04 | limits, plans, versions, opening hours | "10 hours a month", "version 2", "open until 8 pm" |
| RF-05 | people and job titles | "our coordinator, Sam" |
| RF-06 | product, feature and organisation names | a renamed tool, a merged team |
| RF-07 | links and references | listed only; this plugin does not open them |
| RF-08 | future events that may be past | "coming soon", "will launch", "arrives this autumn" |

## Converting relative time

Reference = the publish date. Seasons assume the northern hemisphere unless stated; say which was assumed.

| Phrase | Converts to | Example, published 10 June 2024 |
|---|---|---|
| last year | reference year − 1 | 2023 |
| this year | reference year | 2024 |
| next year | reference year + 1 | 2025 |
| X years ago | reference year − X | "two years ago" = 2022 |
| this spring / summer / autumn / winter | that season of the reference year; if it had already ended by the publish date, it was a slip, query | autumn 2024 |
| next spring | the first spring after the publish date | spring 2025 |
| this quarter | the quarter containing the publish date | Q2 2024 |
| recently, new, newest, latest, soon, upcoming, now | cannot be converted | always Check, with a query for the date; never a computed date |

After conversion: if the converted point is before today's date and the sentence speaks of it as future, the item is Stale, computed. Rewrite only the time words ("Last year" → "In 2023"); an event that may or may not have happened becomes a query, not a guess.

## Statuses

| Status | Set by | Text change |
|---|---|---|
| Current | the user confirms | none |
| Stale, computed | conversion against dates | time words only; events become queries |
| Stale, per your facts | a value the user gave | replaced, source named in the ledger |
| Check | no information | kept, plus `[UPDATE NEEDED: what and where to find it]` |

The model's own knowledge never sets Stale. It may add "may have changed; check". An undated statistic is at least Check: ask for its source and year.
