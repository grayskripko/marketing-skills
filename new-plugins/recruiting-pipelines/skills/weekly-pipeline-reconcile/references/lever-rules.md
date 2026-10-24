# Lever rules and provenance

Read 2026-10-11. These are public official Lever sources checked for this build, not a future verification for the planned 2026-10-18 submission. Publisher revision dates were not reliably exposed in retrieved content. Reopen these URLs near submission and after changes to export schemas or metrics.

## Sources and deciding field rules

### Developer documentation

URL: https://hire.lever.co/developer/documentation
Sections: Opportunities; List all opportunities; Pagination; Lists; Confidential Data; Responses and Errors; Timestamp.
Read 2026-10-11. Direct page and full documentation body loaded.

- Person key: `contact`; candidacy key: opportunity `id`. Legacy candidate IDs can be opportunity IDs. Use `/opportunities`, not deprecated candidate endpoints, to interpret supplied captures.
- Archive attributes: nested `archived.archivedAt` and `archived.reason`. The same documentation's response examples flatten `archivedAt` and `archiveReason`. Preserve actual supplied schema and flag conflicts; don't require a single representation.
- `owner` is the opportunity-owner user ID. The documented list parameters do not include owner filtering. Expanded contact/owner/stage objects require ID normalization.
- `lastAdvancedAt` is current-stage entry; `stageChanges` carries stage-change events with `toStageId`, `toStageIndex`, event `updatedAt` and `userId`. `lastInteractionAt`, opportunity creation and opportunity update fields describe different clocks.
- `updated_at_start/end` filters any changes, unlike the returned `updatedAt` attribute's selected-field update coverage. `advanced_at_start/end` selects current-stage advancement. Creation, archival and advancement endpoints use inclusive time bounds; choose an explicit analysis boundary convention; half-open weekly windows, if chosen, are not an API default.
- `archived` omitted includes both states; false selects active; true archived. `confidentiality` omitted defaults non-confidential; all includes both only with appropriate access. Confidential access is controlled separately from endpoint permission.
- List size defaults to 100; allowed `limit` is 1–100. Follow `hasNext` and returned `next` as the next request's `offset`, preserving the query's other settings. Offset tokens are opaque, not page numbers.
- 400: missing/malformed parameters. 401: invalid API authentication. 403: account settings do not authorize operation. 404: unknown API action/object. 429: rate limit. None establishes a zero-row population. Default API-key rate limits are 10 requests/second steady and bursts up to 20, explicitly variable; supplied interrupted captures stay partial.
- Timestamp format is Unix epoch milliseconds. Event timestamps must not be confused with similarly named object timestamps.

### Recruiter Operations dashboard

URL: https://help.lever.co/s/article/Visual-Insights-Recruiter-Operations-dashboard
Read 2026-10-11. Direct URL loaded the Help Center application shell; official indexed article text was retrieved with targeted web searches and included the sections below. Search-relative publish/crawl dates are not treated as publisher revision dates.

Sections: Metrics; Current Operations; Current Operations - Team View; Performance; Average Time in Stage for Active/Archived Opportunities.

- Current Operations is opportunity-owner scoped to the viewing user; Team View is separate. Active opportunity tables exclude archived records. Posting ownership and opportunity ownership can differ.
- Charts exclude confidential-posting data. Applied filters require refresh; chart-menu Download data supplies chart exports. Stage/milestone grouping affects the displayed population.
- New opportunities is the Lead/Applicant section count, not necessarily creations in the selected week. Performance > Average Time in Stage for Archived Opportunities uses viewer-owned opportunities archived during the date range; use each other chart's specific population and date definition instead of the page-wide summary.
- Performance > Offers by Status uses offers on viewer-owned opportunities as of the range end. Signed/Declined counts require entry into that status within the range. This definition does not impose the page summary's archive-only cohort.
- Your Average Time to Complete Feedback Over Time uses interviews you performed and completed feedback for within the range; duration runs from interview end to feedback completion. Its cohort is interview/feedback events, not archived opportunities.
- Source rechecked 2026-10-11 via official indexed article text: the page introduction and chart-specific data-set definitions conflict. The specific definition governs the named chart.
- The Current Operations viewer-owned active-stage-average chart has stage-time prose but pipeline-days secondary-dataset text. Team View's same-named chart lists stage days; neither specifies how repeat visits are counted. The source does not provide an unambiguous uninterrupted-stage algorithm. Treat a computed current-stage mean as distinct unless the supplied metric definition supports equivalence.

### Hiring Manager dashboard

URL: https://help.lever.co/s/article/Visual-Insights-Hiring-Manager-dashboard
Read 2026-10-11. Direct URL loaded the application shell; official indexed body retrieved, including both All Opportunities in Pipeline tables.

All Opportunities in Pipeline by Posting and by Requisition list active opportunities associated with the viewer's hiring-manager scope, cap the listed rows at 250 and ignore the date-range filter. A full table at 250 is not proof that the pipeline contains exactly 250. Keep this scope distinct from opportunity-owner scope.

### Visual Insights landing page

URL: https://help.lever.co/s/article/Visual-Insights-Landing-Page
Read 2026-10-11. Direct URL loaded the application shell; official indexed body retrieved.

Recently Viewed stores dashboard identity, applied filters and access date/time; reopening restores the filters. Use supplied Recently Viewed details to recover comparison provenance. Only dashboards available to the user's role appear. This provenance is not proof of when underlying data was last refreshed.

## Analysis conventions

These are this plugin's rules of thumb, not Lever policies: exact-duplicate removal, unknown-state bucket, a disjoint count bridge, elapsed 24-hour-day default, ranking without invented thresholds, and reporting an average only over calculable opportunities. Missing/contradictory evidence is reported as unresolved. A historical snapshot needs state evidence at its cutoff. No standard aging SLA or hiring-quality benchmark is asserted.
