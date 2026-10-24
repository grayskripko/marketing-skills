# Recruiting Pipelines

Explain why your Lever dashboard and spreadsheet counts disagree, and what changed in this week's recruiting pipeline. Match person and opportunity IDs, archive states, owners and report settings across supplied exports.
For recruiting operations teams checking weekly Lever reports. Needs pasted rows or selected CSV/JSON exports, the reporting cutoff and dashboard settings. No account, installation beyond the plugin, credentials or paid API is needed for analysis of supplied data.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon, with Markdown/text/JSON development evidence. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

Routine analysis uses only text, attachments and local export files you explicitly supply. Neither skill directs code execution, software installation, live Lever API calls, account access, uploads, message delivery, publication or settings changes. The skills read their bundled reference text; API field and pagination examples explain supplied captures rather than authorize live requests.

If you explicitly ask to refresh knowledge, either skill may use your assistant's existing web tool to retrieve only these official documentation URLs and the two origins' robots.txt:

- https://hire.lever.co/developer/documentation
- https://help.lever.co/s/article/Visual-Insights-Recruiter-Operations-dashboard
- https://help.lever.co/s/article/Visual-Insights-Hiring-Manager-dashboard
- https://help.lever.co/s/article/Visual-Insights-Landing-Page
- https://hire.lever.co/robots.txt
- https://help.lever.co/robots.txt

This optional refresh makes network requests. The sites and the assistant's tool provider receive the requested URLs and ordinary connection metadata, never export rows, candidate identifiers or private task context. The skills respect access restrictions, stop at off-origin redirects and do not substitute an unapproved search. If a page returns an application shell or no usable article, the answer identifies the failed refresh and continues with dated bundled references where useful. The references also recommend reopening these sources near submission and after schema or metric changes; this is documentation retrieval, not a Lever account connection. Repository and support links identify package information, not recruiting-data destinations.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and tool activity under its own terms. Any local output file you explicitly request is created by your assistant's existing file tools, not by a bundled program; the skills do not direct file creation or persistent monitoring.

## Skills

- **weekly-pipeline-reconcile** — explain weekly opportunity-count changes and dashboard/export differences, keeping distinct people and candidacies separate.
- **current-stage-aging** — rank active opportunities by elapsed time in their current stage, apply your threshold and identify unusable timestamps.

## Inputs and results

Supply opportunity IDs, contact/person IDs if people counts matter, stage IDs/names, archive state, opportunity owners and the capture time. For dashboard comparisons, include the dashboard, page, chart/table, signed-in user or team scope, filters and refresh/export time. For aging, include current-stage entry timestamps and an as-of time with timezone. Redacted IDs are sufficient if they remain consistent across files.

A weekly reconciliation returns supported totals and an opportunity-level change table. Stage aging returns ages, the denominator used for averages and timestamp exceptions. Partial exports produce partial totals and the exact evidence needed to finish the comparison. Supplied snapshots do not by themselves establish every movement during the week.

## Source notes

The dated source registers are in each skill’s `references/lever-rules.md`. Built against sources read 2026-10-11. The optional refresh scope is disclosed above.
