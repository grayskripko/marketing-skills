# Official measurement sources

Verified by opening each page on 2026-10-11 (read 2026-10-11). Google provides no last-edited date on these pages. Verification describes the content observed today; use updated official text when a later report needs a current rule. All sources concern Google Search Console. Rules below are paraphrased. The cell ledger and output order are authored workflow choices, not Google fields.

| Source | Supporting section and deciding knowledge |
|---|---|
| [Generative AI performance report (Search)](https://support.google.com/webmasters/answer/16984139?hl=en) | Rollout note: August 31, 2026 worldwide. What's included: AI Overviews and AI Mode, excluding Labs. Chart/table: property chart except URL filter; pages by page, other documented dimensions by property. Data is included in Web performance. Missing report: insufficient impressions or exclusion; no threshold stated. |
| [Performance overview](https://support.google.com/webmasters/answer/7576553?hl=en) | Exporting: UI `~` and `-` become numeric zeros. Metric definitions: CTR is clicks divided by impressions. This ordinary Search report is distinct from the dedicated AI report. |
| [Troubleshooting discrepancies](https://support.google.com/webmasters/answer/17010575?hl=en) | Table limit: 1,000 rows. Query privacy omissions affect query data. Filtering match/non-match totals may fail to add to the unfiltered chart due to omissions and truncation. A gap alone does not reveal its exact cause. |
| [Advanced filtering and comparison](https://support.google.com/webmasters/answer/17011165?hl=en) | Comparison notes: one comparison at a time; rare rows can show `~`; filtering by the rare value should show both comparison values. Regex: RE2, partial match, insensitive by default; `^`, `$` and `(?-i)` change behavior. Multiple simultaneous filters are supported. |
| [About the data](https://support.google.com/webmasters/answer/17011364) | Aggregation: one property impression for repeated property results versus separately counted unique URLs. Freshness: dotted data is preliminary and can change. Exporting confirms unavailable symbols become zeros. |
| [Dimensions and data groupings](https://support.google.com/webmasters/answer/17011259) | Pages: most metrics accrue to the canonical URL. Dates: PT; 24-hour view uses browser local time. Sunday–Saturday weeks, calendar months, and partial boundary periods. Multimodal ordinary Search has no text query dimension. |
| [Search generative AI control](https://support.google.com/webmasters/answer/16908024?hl=en) | Settings → Search generative AI; Include, Exclude and Inherit. Inheritance follows the closest manually configured parent; otherwise the top-level domain. Current control is eligibility evidence, not a measured historical impression count. Read 2026-10-11. |
| [Impressions, position and clicks](https://support.google.com/webmasters/answer/7042828?hl=en) | AI Mode: follow-up is a new query; standard impression counting applies. AI Overviews: standard impression counting and one shared position for links. Canonical credit has exceptions; do not invent URL mappings. |

## Reconciliation conventions

Preserve raw exported values and original UI symbols, distinguish absent/blank/unavailable/confirmed-zero/uncertain-zero cells, and calculate only on supported comparable values. These are data-preservation decisions. A page subtotal cannot recover unknown overlap. Percent change uses the old value as denominator and is undefined at a confirmed zero baseline.

## Source-addressed report conventions

Read 2026-10-11. Exact cell joins, duplicate/conflict handling, null usable values, requested ledger fields and calculation-to-source links are authored workflow choices. They preserve evidence across files; they are not Google export columns. A separately captured URL-filtered view is kept separate because Google changes chart aggregation when a URL filter is active (Generative AI report, Reading the chart). The rare-row recovery step is supported by Advanced filtering and comparison, Comparison limits and notes; it does not assert that a fresh capture will always return a number.
