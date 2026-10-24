# Gradebook Reporting

Recompute Google Classroom overall grades from exported scores, categories, weights and excused states, with a discrepancy ledger.
For teachers and course administrators checking their gradebook against a spreadsheet or report.
Needs pasted rows or a supplied CSV/Sheets export, grading settings, assignment points and student-specific states. No Classroom account connection, API key, extra software or paid API is needed to analyze supplied exports.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The .claude-plugin and .codex-plugin directories contain platform metadata, not executable servers. Development notes and evaluation records currently accompany this working folder; exclude them from the submitted release package.

These skills analyze only task text, attachments, and local files that you explicitly supply, using the assistant's existing file-reading tools and bundled references. They do not direct software installation, web search, URL or robots.txt retrieval, API calls, account access, message delivery, grade publication, or settings changes. API-shaped exports are supplied data, not requests to the Classroom API. Source and support URLs identify references, not retrieval instructions; supply the relevant content rather than a URL alone.

No executable code is bundled. The assistant may use its existing local calculation tools, which can execute calculations on supplied data, and its file tools to create a report you explicitly request. Execution and temporary files are managed by your assistant provider. This is therefore a supplied-material workflow with host tool use, rather than a strict no-execution workflow. No plugin-directed network request is needed for grade analysis. The export instructions below describe a separate user action in Google Classroom: downloading a CSV or copying grades to Google Sheets uses your Google account and Google's services; the skills do not perform that action.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Request | Result |
|---|---|---|
| recompute-classroom-grades | Work out these overall grades | Student totals, category workings, included/excluded rows and unresolved inputs |
| reconcile-classroom-grades | Explain why these reported grades differ | Recomputed values, percentage-point differences and a row-linked discrepancy ledger |

These skills calculate or compare grades. For CSV formatting or cleanup alone, use a general spreadsheet workflow.

Use student aliases. Include class and period scope, export timestamp, grading mode, category weights, scores, maximum points, excused flags, draft/returned status and the reported total when available. Missing fields remain visible; the report can still calculate supported subsets.

For an export, on a computer open Classwork, an assignment, then Student work. In Settings choose Download all grades as CSV or Copy all grades to Google Sheets. Download these grades as CSV covers only that assignment. Supply grading settings and excused-state evidence separately if absent from the export. A screenshot or pasted settings text is enough.

The [source register](skills/recompute-classroom-grades/references/google-grading-rules.md) covers grading modes, absent-category weight normalization, missing-work draft scores, API export state gaps, grading periods and grade-field precision. Unequal-point category arithmetic is shown as separate scenarios when the supplied evidence does not establish the category method.

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See LICENSE.
