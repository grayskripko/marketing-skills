# Official LinkedIn reporting knowledge

Verified by live page reads on 2026-10-11 for the planned 2026-10-19 submission. Dates below are actual read dates, not future submission dates. These are public documentation observations; match rules to the supplied historical settings. Read all core rules in SKILL.md before using details here.

## Attribution Model view

URL: https://www.linkedin.com/help/lms/answer/a7132084
Read 2026-10-11. Loaded title: Attribution Model metrics for leads and conversions in Campaign Manager. Page shows “9 months ago,” not an exact update date.

Scope: Campaign Manager Attribution Model columns. Direct Leads counts submissions; data-driven Leads covers funnel contribution over 180 days. Data-driven Conversions covers Insight Tag, Website Actions and CAPI sources over 90 days. Data-driven metrics can take 36 hours, rarely longer; Leads refreshes in real time. Filtering selected entities can change the comparison because attribution includes contributions to leads submitted elsewhere in the account. Clear filters and end the range at least two days before today for a useful comparison. Available at campaign, ad-set and ad levels. This view cannot be exported; paste the visible table. Standard and data-driven conversions can differ with Each ad set conversion rules.

## Conversion credit

URL: https://www.linkedin.com/help/lms/answer/a426349
Read 2026-10-11. Loaded title: LinkedIn conversion attribution model. Page shows “11 months ago.”

Scope: conversion-action attribution settings. Each ad set credits every associated ad set with an interaction inside the conversion window. Last ad set credits the latest eligible ad set. For most categories, repeated events count once per member, conversion action and ad set within the lookback window; this is not account-wide deduplication. Purchase and Add to Cart can count repeated events. The comparison guidance below supplies this precise counting scope. Some conversion measurement uses predictive models or on-device tracking. This is distinct from data-driven attribution credit. Aggregate credits do not establish unique people or overlap; that conclusion is an analytical constraint, not a claimed additional platform rule.

## API field schema

Required URL: https://learn.microsoft.com/en-ca/linkedin/marketing/integrations/ads-reporting/ads-reporting-schema?view=li-lms-2026-02
Also verified: https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting-schema?view=li-lms-2026-04
Read 2026-10-11. Both loaded Metrics Available in LinkedIn Ads Reporting; supplied view shows update 2026-09-16. Shared relevant field definitions were present in both views. A query-string version is not proof of an export's request-header version.

`oneClickLeads` counts One Click Lead Gen leads. `qualifiedLeads` counts advertiser-shared qualified leads; `costPerQualifiedLead` is local-currency spend divided by qualified leads. Website conversions count desired actions after ad clicks/views and can use group attribution or estimation. Post-click and post-view fields retain those distinctions. `dateRange` dates are UTC and inclusive. Viral conversion and lead fields are separate. Preserve source labels and reporting grain; mapping API names to current UI entities requires supplied evidence. Conversion value is advertiser-defined. An export's missing field is not automatically its schema default.

## API report limits and missing data

URL: https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?tabs=http&view=li-lms-2026-04
Read 2026-10-11. Loaded Reporting - LinkedIn; update 2026-06-24.

No pagination; maximum 15,000 elements. An empty response means no activity OR absent read access. Professional demographic results keep top 100 values per creative/day, suppress fewer than 3 events, lag 12–24 hours and are approximate. Prefer whole-period, desired-level queries over summing approximate demographic breakdowns. Performance retention is ten years, demographics two years; ALL ranges outside daily retention may round to month boundaries. Compare returned ranges.

Error meanings for supplied export logs: 400 MISSING_FIELD = required query argument missing; INVALID_VALUE_FOR_FIELD = invalid argument; START_DATE_AFTER_END_DATE = reversed dates; DATE_TOO_EARLY = outside retention. 403 USER_NOT_AUTHORIZED = access/reporting permission failure. 414 REQUEST_URI_TOO_LONG = use query tunneling. 429 TOO_MANY_REQUESTS = exceeded metric request load; reduce requested fields. Empty or failed exports are missing evidence, not zero totals. This package interprets logs; it does not call the endpoint.

## Current conversion windows and repeat events

URL: https://www.linkedin.com/help/lms/answer/a426359
Read 2026-10-11. Loaded LinkedIn conversion window; update “1 month ago.”

Ordinary windows: 1, 7, 30 or 90 days. The page states a 90-day click/view default for most conversions; do not assume that applies to a supplied historical action. CAPI/CSV allows 180/365 days for Submit Application, Purchase, Add to Cart, Qualified Lead, Marketing Qualified Lead, Sales Qualified Lead and Lead categories. Purchase/Add to Cart count repeated member events, unlike most types. Window edits affect subsequent counting, not historical counts. Event-registration click/view windows increased to 30 days in April 2025. Do not replace fixed data-driven windows with conversion-action windows.

## Modeled conversion measurement

URL: https://www.linkedin.com/help/lms/answer/a546228
Read 2026-10-11. Loaded Using modeled conversions to measure conversions for LinkedIn Ads; update “11 months ago.”

Machine learning estimates conversions when individual observation is unavailable; available first-party individual data supports deterministic measurement. Modeled conversions are already in the same reporting dimensions/metrics as other conversions. No separate modeled count or percentage can be inferred from a standard-versus-data-driven gap.

## Comparison checks and conflicting guidance

URL: https://www.linkedin.com/help/lms/answer/a420207
Read 2026-10-11. Loaded Compare Campaign Manager conversions with third-party reporting; update “11 months ago.”

Useful supported checks: conversion-action association to ad sets, matching conversion pages/URL rules, lookback differences and category-specific repeated-event handling within the same ad set. Conversions across ad sets are not deduplicated by the ordinary-category repeat-event rule; apply the supplied Each ad set or Last ad set attribution setting separately. A mismatch alone does not prove any of these caused it. The page lists only 1/7/30-day windows, whereas the newer dedicated window page includes 90 and selected 180/365-day options. Use the newer dedicated source for allowed windows. Its broad cookie discussion should not override the dedicated modeled-measurement guidance. Do not carry these older claims into a client explanation as established causes.

## Authored analysis choices

Compare compatible scopes, exclude total rows from detail sums, retain blanks, show formulas, avoid guessing overlap and separate possible mechanisms from proven causes. These are analysis procedures chosen for this job, not additional LinkedIn policies or numerical platform limits.

Fix verification 2026-10-11: reopened conversion attribution, third-party comparison and modeled-measurement sources. The comparison explicitly scopes ordinary-category repeat counting to the same member, action and ad set. Comparison and modeled-measurement pages both display “11 months ago”; their relative chronology is not established.
