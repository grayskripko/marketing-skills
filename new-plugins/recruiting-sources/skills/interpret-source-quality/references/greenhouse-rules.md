# Greenhouse report evidence

All pages loaded successfully; read 2026-10-11. Publisher updates: 2026-03-02 (quality 14:09, troubleshooting 14:20, custom source 14:08). Scope: Greenhouse Recruiting essential reports; Core, Plus and Pro tiers. Quality report access: Job Admin and above.

| Source | URL | Supporting section / decision |
|---|---|---|
| Candidate quality by source report | https://support.greenhouse.io/hc/en-us/articles/203940929-Candidate-quality-by-source-report | Report definition, Filters, visualization: quality tracks pipeline distance; default applied-date range is current year. |
| Troubleshoot a report | https://support.greenhouse.io/hc/en-us/articles/13710986142107-Troubleshoot-a-report | Migrated candidates, user permissions, emailed links: default migration exclusion, job visibility and 24-hour link expiry. |
| Add custom source | https://support.greenhouse.io/hc/en-us/articles/200721664-Add-custom-source | Each custom source requires a sourcing strategy. |

Additional verified source: [Comparing cohort, activity, and snapshot reports](https://support.greenhouse.io/hc/en-us/articles/213332286-Comparing-cohort-activity-and-snapshot-reports), read 2026-10-11; updated 2026-09-03 15:11. Candidate quality by source belongs to cohort reports; Number of hires belongs to activity reports. Equal date ranges do not establish equal candidate populations.

## Source conflict

The quality page says sourcing strategies are fixed; the custom-source page links to adding strategies. This package does not assert whether strategies can be modified. Both support grouping sources by strategy.

## Analysis conventions

These are this package’s rules of thumb, not additional platform definitions: preserve reported quality when raw calculation inputs are absent; separate candidate/application grain; reconcile cohort before rates; treat zero denominators as undefined; do not infer causes, individual merit or ROI from report values. The documentation’s endpoint examples define quality conceptually, not an implementation formula for mixed job pipelines, skipped stages or weighted rollups.

## Maintenance

Reopen sources before the planned 2026-10-20 submission and on metric changes. A 2026-10-11 retrieval does not establish later source state.
