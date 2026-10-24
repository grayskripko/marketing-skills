# GA4 reporting rules — official source register

Read 2026-10-11. The linked Google Help pages were retrieved on that date and returned HTTP 200 with the stated title. No article revision date was exposed in the retrieved text. Summaries are paraphrases; section names identify the supporting passages.

The supplied URLs are entries 1–5. Entries 6–15 add deciding field, filter, retention, quality and rate rules. Summaries are paraphrases; section names identify the supporting passage. Core deciding rules are inline in both skills.

## 1. Acquisition scope

URL: https://support.google.com/analytics/answer/14731736?hl=en
Title: User acquisition report vs. Traffic acquisition report. Read 2026-10-11.
Support: “Scope”, “Dimensions”, “Compare metrics across reports”. First-user traffic dimensions and session traffic dimensions allocate activity differently. A user first acquired organically can have later activity in another session channel. Similar engagement/revenue metrics therefore have different channel-row values. Session attribution remains non-direct last click, with the other-key-event lookback setting (90-day default). This decides whether a gap is a valid comparison; identical channel labels alone are insufficient.

## 2. Sampling limits and estimates

URL: https://support.google.com/analytics/answer/13331292?hl=en
Title: About data sampling. Read 2026-10-11.
Support: “Why you see data sampling”, “What are the limits”, “What about unsampled data”. Sampling selects data and scales results; the quality icon gives the percentage used. Standard event-level queries have a 10-million-event quota. Analytics 360 initially uses 100 million; Explore can request more detailed results up to 1 billion. Country filtering can still cause sampling on very large data sets. HLL++ estimates distinct users and sessions even without sampling. Do not rescale an exported estimate or declare a small gap a tracking fault.

## 3. Withheld rows

URL: https://support.google.com/analytics/answer/9383630?hl=en-GB
Title: [GA4] About data thresholds. Read 2026-10-11.
Support: “What you'll see”, “When data thresholds are applied”, “What you can do”. System-defined thresholds cannot be adjusted. The indicator identifies affected cards. Demographics, demographic audiences and search-query information can have withheld rows at low counts. Increasing the queried date range can help availability, but changes the reporting period. A hidden row is not zero. Avoid inferring suppressed demographic values from aggregate differences. BigQuery excludes Google signals data and is not an identical replacement surface.

## 4. Attribution model meanings

URL: https://support.google.com/analytics/answer/10596866?hl=en
Title: Get started with attribution. Read 2026-10-11.
Support: “Overview”, “Data-driven attribution”, “Paid and organic last click”, “Google paid channels last click”. The overview lists data-driven, paid-and-organic last click and Google-paid-channels last click attribution models. Direct receives no credit unless the full path is direct. Data-driven models distribute fractional credit. First click, linear, time decay and position-based models have been unavailable since November 2023. The overview says conversions can be reattributed up to 7 days; entry 11 separately states up to 12 days for key-event credit. Do not transfer the attribution-report model list to an assertion about every property's selectable reporting setting.

## 5. Sessions

URL: https://support.google.com/analytics/answer/9191807?hl=en
Title: About Analytics sessions. Read 2026-10-11.
Support: “What counts as a session”, “How the number of sessions is calculated”, “How session attribution works”, “Differences in session counts”. Default inactivity timeout is 30 minutes and can be configured; it is not a maximum session length. Session IDs are estimated for session counts using HLL++. Session attribution stays non-direct last click with the other-key-event lookback setting (90-day default). session_start event count is not a guaranteed interchangeable Sessions metric. For raw event analysis, session ID alone is not globally unique; it needs a user identifier, which this aggregate workflow does not request.

## 6. Attribution setting scope and timing

URL: https://support.google.com/analytics/answer/10597962?hl=en
Title: Select attribution settings. Read 2026-10-11.
Support: “Reporting attribution model”, “Fractional credit”, “Key event lookback window”. Reporting model changes apply to historical and future event-scoped key-event/revenue reporting. First-user and session traffic dimensions are unaffected. Source, Medium, Campaign and Default channel group are examples of event-scoped fields. Key events, Total revenue, Purchase revenue and Total ad revenue can show fractional allocation with those dimensions. Acquisition key events first_open/first_visit default to 30 days, with 7 allowed; other key events default to 90 days, with 30/60 allowed. Lookback changes apply going forward and also affect session attribution. The page's introductory role wording differs from its detailed permission instruction; this plugin neither guides nor performs settings writes.

## 7. Reports versus Explore

URL: https://support.google.com/analytics/answer/9371379?hl=en
Title: Data differences between reports and explorations. Read 2026-10-11.
Support: “Supported fields”, “Data filtering”, “Segments and comparisons”, “Date range”, “Behavioral modeling”, “Processing time”. Explore filters are case-sensitive with explicit match types. Report table Search uses case-insensitive contains; this is not the top search field or Add filter button. Opening a report/comparison in Explore can drop unsupported fields, changing the selection. Explore date availability is restricted by retention. Modeling and differing processing times can affect a comparison, but a numerical gap alone does not identify either as its cause.

## 8. Grouped dimension values

URL: https://support.google.com/analytics/answer/13331684?hl=en
Title: About the (other) row. Read 2026-10-11.
Support: “What is the (other) row”, “Why you see the (other) row”, “What are the limits”. Less-common dimension values can be condensed when the underlying table reaches its row limit. Limits vary by property type, report and query complexity. More than 500 dimension values is high-cardinality guidance, not a hard maximum or a universal table row limit. Keep grouped values separate from known channels and retain them when explaining visible row coverage; never distribute them without evidence.

## 9. Missing dimension value meanings

URL: https://support.google.com/analytics/answer/13504892?hl=en
Title: What the value (not set) means in your reports. Read 2026-10-11.
Support: introduction, “Session source / medium dimension”, “Landing page dimension”, “Custom parameters”. (not set) means Analytics lacks a value for the selected dimension. Session source/medium can show it when session_start is missing, and that traffic becomes Unassigned in the default channel group. A missing page_view can yield a (not set) landing page. New custom parameters may show (not set) in their first 24 hours. These are specific diagnostic leads; supplied exports alone do not establish a client's implementation fault. Preserve the dimension context rather than relabeling every (not set) as direct.

## 10. Retention

URL: https://support.google.com/analytics/answer/7667196?hl=en
Title: Data retention. Read 2026-10-11.
Support: “Google Analytics properties”, “Reduce or increase the retention period”. Standard event/user retention choices are 2 or 14 months; 360 has longer options for other event data. Demographics retain 2 months regardless of settings. Large/XL properties can be limited to 2 months. Retention affects explorations and funnel reports, not standard aggregated reports, including their primary/secondary dimensions and comparisons. Deleted data cannot be recovered by increasing retention. An empty old exploration does not prove absence of activity.

## 11. Freshness and late credit

URL: https://support.google.com/analytics/answer/11198161?hl=en
Title: Data freshness. Read 2026-10-11.
Support: introduction, “Intraday”, “Daily”, “Limitations”. Processing can take 24–48 hours. Standard intraday is typically 2–6 hours, with stated property/query coverage; these are typical intervals. Intraday event-scoped traffic fields can have gaps and use paid-and-organic last click until daily processing applies the selected model. Daily key-event attribution credit can change up to 12 days after recording. Reports and Explore may not synchronize. For this job, preserve export timestamps and label recent credit as revisable using this specific 12-day key-event guidance; do not use the overview's 7-day conversion statement as a blanket finalization rule.

## 12. Engagement rates

URL: https://support.google.com/analytics/answer/12195621?hl=en
Title: [GA4] Engagement rate and bounce rate. Read 2026-10-11.
Support: definitions and examples. An engaged session meets the engagement-duration criterion, has a qualifying key event, or has at least two page/screen views. `first_visit`, `first_open` and `session_start` do not qualify a session as engaged merely by being marked as key events. Use exported engaged-session counts rather than reconstructing them from raw key-event totals. The default duration is 10 seconds; use supplied timer settings where relevant. Engagement rate is engaged sessions divided by sessions. Bounce rate is the complement. Calculate overall rates from overall numerators and denominators instead of averaging row rates.

## 13. Distinct user fields

URL: https://support.google.com/analytics/answer/12253918?hl=en
Title: [GA4] Understand user metrics. Read 2026-10-11.
Support: “Differences at a glance”, “Differences in depth”. Total users, Active users, New users and Returning users are different fields. Not every new user is active; new users can exceed active users. Keep exact exported metric labels. Distinct counts cannot be added across overlapping groups or dates to obtain a unique monthly population. The detailed table also lists collected web `first_visit` as an Active users trigger. With matched web-only, device-based scope, a lower Active users count than New users needs reconciliation rather than an explanation based solely on short visits. This inference does not identify a tracking cause. Entry 13 rechecked 2026-10-12; both the general statement and detailed definition remain on the linked page.

## 14. Key-event counting

URL: https://support.google.com/analytics/answer/13366706?hl=en
Title: Change the counting method of key events. Read 2026-10-11.
Support: “About counting methods”, final note under “Change the counting method”. Once per event counts each trigger; once per session counts a selected key event once within the session. Most events default to once per event; migrated Universal Analytics goals can default to once per session. Setting changes affect future key events only. Preserve the supplied method and change date; do not rewrite historical counts as though the new method applied then.

## 15. Session rates and revenue definition

URL: https://support.google.com/analytics/answer/12923437?hl=en
Title: [GA4] Traffic acquisition report. Read 2026-10-11.
Support: metric table, “Session key event rate” and “Total revenue”. Session key event rate is sessions containing a key event divided by total sessions. Use the selected-event numerator when the report selects one event. Total revenue includes purchases, in-app purchases, subscriptions and ad revenue, minus refunds; it is not automatically purchase revenue. Preserve the exported revenue label and currency and do not reinterpret total revenue as the selected purchase event's revenue.

## Authored workflow choices

The comparison table, one source per metric/scope, a usable partial report before one question, and the requested input checklist are authored workflow choices (this plugin's rule of thumb), not Google requirements. Arithmetic identities follow the supplied inputs. The event/session distinction follows entries 14–15; do not manufacture the session numerator from event totals. Quality unknown remains unknown.
