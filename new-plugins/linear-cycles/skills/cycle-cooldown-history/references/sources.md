# Linear source register

Read 2026-10-11. All entries are public first-party Linear documentation and loaded successfully. These are access dates, not publisher revision dates. Reopen these pages before the planned 2026-10-18 submission to check for changes. Rules concern Linear team cycles and exports, not generic sprint tools.

## Cycle graph
URL: https://linear.app/docs/cycle-graph
Sections: How to read a cycle graph; Understanding scope; Assign completed issues to previous cycles; FAQ.
Supporting facts: graph colors distinguish scope, completed and stacked started work. The dotted target flattens on weekends. Scope uses team estimate settings, including defaults for unestimated issues, or counts issues. The FAQ defines success by issue counts, with full completed credit and 25% started credit. It does not establish estimate-weighted success. Closure members completed before the next cycle starts can count back.
Decision: keep weighted graph completion separate from documented issue-count success. Preserve displayed success; point-only totals cannot reconstruct it. Do not add the stacked started height twice.

## Filters
URL: https://linear.app/docs/filters
Sections: Apply filters; Advanced Filters; Added to cycle.
Supporting facts: main filters are in shared URLs; view options, quick filters and Insights filters are omitted. Nested AND/OR groups are supported. Planned includes additions before start and through the first 24 hours; After cycle means more than 24 hours after start, including after end. Added to cycle describes timing, unlike cycle membership.
Decision: preserve filter provenance and test the inclusive boundary using membership events.

## Cycles
URL: https://linear.app/docs/use-cycles
Sections: Cooldowns; Starting day; Start a cycle today; Issues rollover; Auto-add active issues; final FAQ.
Supporting facts: no issues can be assigned to cooldown. Scheduled start is 12:01 AM team time; early start is midnight and ends an active cycle or cooldown. Open closing-cycle work moves forward; cooldown cancellation, completion, backlog and triage transitions are exceptions. Cycle-less completion/started automations send cooldown work to previous/next cycles respectively when enabled. Closed graphs/statistics remain historical snapshots while current lists can change after status, estimate or cycle edits.
Decision: require event history and automation settings; separate rollover from cycle-less auto-add and current rows from snapshots.

## Issue properties — Estimates
Canonical URL: https://linear.app/docs/issue-property#estimates
Discovery URL: https://linear.app/docs/estimates redirected to https://linear.app/docs/issue-properties-home; its Estimate link opened the canonical page.
Sections: Configure estimates; Scale range options; Extended estimate scales; Zero estimates; Estimates in analytics.
Supporting facts: scales/settings are team-level. T-shirt maps to Fibonacci values 1/2/3/5/8, with extended sizes 13/21. Explicit zero differs from unestimated. Blanks count as one by default but this can be disabled. Estimate-enabled graphs use estimate values; otherwise each issue contributes one.
Decision: resolve blank treatment and do not sum incompatible team scales as one velocity.

## Exporting Data
URL: https://linear.app/docs/exporting-data
Sections: Workspace CSV exports; Issue view CSV exports; Copy issues as markdown; Export individual issues as PDFs.
Supporting facts: view exports allow 250 issues for members and 2,000 for admins (owners on Enterprise); guests cannot export. Workspace exports require admins, or Enterprise owners, and download links expire in 12 hours. Documented columns include ID, Team, Status, Estimate, cycle number/name/start/end, Created, Updated, Started and Completed; no added-to-cycle event is listed. Attachments are not included; descriptions may contain links. Individual issue PDFs use absolute event timestamps.
Decision: verify coverage and request membership history instead of interpreting Created or Updated as cycle entry. Never follow attachment links automatically.

## Analysis conventions

The optional point-weighted quarter-credit score (not Linear Cycle Success), scope bridge, duplicate-row handling, sample labels, missing-data markers and output layout are authored analysis conventions, not extra Linear policies. They prevent unsupported joins and make the report explainable. Supplied graph captures remain authoritative for their stated time; reconstructed figures require matched membership/settings. No source here establishes a graph's exact snapshot instant relative to later cooldown edits.

## Fix verification — read 2026-10-11

Reopened all five primary sources. Cycle graph FAQ describes issue-count success; Estimates in analytics describes weighted percentage completion and effort. Keep both measures separate; no unequal-estimate workspace observation was performed. Public README and privacy links independently returned HTTP 404.
