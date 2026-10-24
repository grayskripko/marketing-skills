# Campaign import knowledge register

Verified/read 2026-10-11. These pages loaded as official Google Analytics Help documents; no revision date was displayed. Verification is as of the read date, not a claim about future documentation.

## Campaign fields and join behavior

URL: https://support.google.com/analytics/answer/10071305?hl=en
Title: Import campaign data. Read 2026-10-11; live page uses this name rather than Cost data import.

Deciding facts: daily aggregation; required source, medium, date; ISO dates after 2013 through today; at least one metric among clicks, cost, impressions. Cost needs ISO 4217 currency via source mapping or static currency. Campaign ID/name are recommended optional fields. Term/content cannot be imported. Headers follow configured schema. Exact UTM matches matter; unresolved dynamic macros cannot be mapped. Duplicate keys should be removed. Latest same-key values replace earlier ones. Query-time joins can enrich processed events. Match rate uses imported-row joins over imported rows and the most recent two years; % imported uses accepted rows over file rows. Imported metrics may report without a join. Report availability can take 24 hours. Keep configured optional identities in comparisons. The illustrative template omits currency; the currency requirement and static mapping section decide cost readiness.

Supported repair mapping: `date`, `utm_source`, `utm_medium`, at least one of `clicks`, `cost`, `impressions`; optional `utm_id`, `utm_campaign`; cost additionally needs a mapped currency field or static currency. These are field targets, not an order imposed on every file: preserve the chosen source headers and mapping. `customer_email` is outside the documented campaign field table. Source: the Dimensions, Metrics and currency-mapping sections of the campaign URL above, read 2026-10-11.

## CSV and date interpretation

URL: https://support.google.com/analytics/answer/16308305?hl=en
Title: Prepare your data for import. Read 2026-10-11; applies to supported import sources described as open beta.

A file needs an extension and a header first line. Dates can be normalized from supported formats. Slash format is MM/DD/YYYY: 02/01/2026 can be processed as February 1 despite a different intention. Detection of DD/MM/YYYY can fail the import. Emit confirmed dates as YYYY-MM-DD. General connector timestamp formats do not replace campaign daily date requirements. Refresh guidance concerns scheduled connected sources, outside this package's workflow.

## Schema and replacement

URL: https://support.google.com/analytics/answer/14243300?hl=en
Title: Understand import sources. Read 2026-10-11.

The schema supplies join dimensions and imported values. Reimports append new keys and overwrite existing same-key data. Saved field mappings cannot be edited; changing fields involves a new source configuration. The general join-key discussion is not permission to impose one universal key on every campaign mapping. Inspect the user's chosen campaign schema instead. Salesforce-specific fields and permissions do not apply here.

## Validation statuses and coverage

URL: https://support.google.com/analytics/answer/17231531
Title: Campaign data import validation report. Read 2026-10-11.

Joined means linked campaign data. No campaign data can mean absent import or incorrect join. No Analytics data means imported data reported without collected Analytics data. Default view is session scoped, filtered to paid manual traffic, excluding Google sources and search mediums; filter can be removed. Coverage denominator is rows with collected Analytics data, unlike imported-row match rate. Status uses positive cost/clicks/impressions values; all-zero imported rows cannot be diagnosed from that signal alone.

## UTM identity

URL: https://support.google.com/analytics/answer/10917952
Title: URL builders: Collect campaign data with custom URLs. Read 2026-10-11.

UTM values are case sensitive. utm_id maps to campaign ID, utm_campaign to name, utm_source to source, utm_medium to medium. Missing tagging can produce (not set). Session traffic-source dimensions expose collected campaign values. Landing page + query string and Page path + query string omit UTMs; Page location retains them. These URL rules do not make every UTM field an allowed campaign-import column.

## Currency support

URL: https://support.google.com/analytics/answer/9796179
Title: Currency reference. Read 2026-10-11.

Google lists supported currency codes, including USD, EUR and ARS. Use the supplied ISO code or configured static mapping, not a symbol or inferred country. This page describes monetization currency behavior; do not apply its transaction conversion timing to campaign imports. It contains legacy currencies, so it is not an exhaustive current ISO validation authority. Unknown currency eligibility needs current source or mapping evidence.

## Authored data-quality decisions

These are workflow rules of thumb, not Google parser error codes: hold unexplained negative metrics or fractional counts; require valid populated metrics and hold additional blank selected metrics absent a supplied blank-allowed mapping; quarantine every member of conflicting duplicate groups; aggregate only confirmed disjoint daily components in one currency; preserve source references and inputs; keep valid-but-unmatched rows in the candidate; distinguish register intention from observed session keys. Never claim an undocumented file-size limit, integer range, error code or correction outcome. Explain any supplied literal platform error using its exact message and mapped field evidence; report an unknown code as unresolved.
