# GA4 Imports

Prepares a GA4 cost or campaign import CSV from your daily ad exports and UTM register. Returns the candidate CSV, rejected rows and a check of whether its campaign values match your supplied Analytics export.
For marketing analysts importing cost, clicks or impressions. Provide your exports, campaign register and chosen field mapping. No connected account, API key, paid service or additional software is required to prepare the files.

| Skill | Ask it to | Result |
|---|---|---|
| ga4-map-campaign-import | Turn daily exports into my campaign import CSV | Mapped candidate, excluded rows with repairs, join-readiness verdict |
| ga4-check-import-joins | Check whether my candidate will join | Reviewed candidate, rejected-row ledger, observed matches and unresolved join evidence |

Provide exact headers and mappings, daily date convention and timezone, currency mapping or static currency when cost is included, and the campaign register. An Analytics session export covering the same dates makes observed join comparison possible. Earlier import rows make replacement comparison possible.

Example: “Turn this daily ad export into my chosen campaign schema. Keep the campaign IDs as text. Use the supplied UTM register and static EUR mapping. Return the candidate CSV and rejected rows.”

The workflow preserves historical campaign identities. It handles ambiguous dates, unresolved macros, duplicate keys, currency gaps and replacement collisions. Candidate format validity and observed join coverage are reported separately. It prepares campaign imports only; user, item and event imports are separate jobs. No data is uploaded.

## Data and network

Network fetches: none. The skills read supplied conversation text, user-selected local exports and bundled references. They may create requested candidate and ledger files locally using the assistant's file tools. No connector, login, telemetry or background storage is included. See [PRIVACY.md](PRIVACY.md).

## Knowledge

Official Google field, matching and report rules are bundled in [campaign-rules.md](skills/ga4-map-campaign-import/references/campaign-rules.md), verified on 2026-10-11. The supplied schema determines output headers. A missing detail is marked next to the affected output.

Support: https://github.com/grayskripko/marketing-skills/issues
