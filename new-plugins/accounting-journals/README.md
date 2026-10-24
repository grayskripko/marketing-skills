# Accounting Journals

Checks Xero manual journal CSV files before import against the selected native or Conversion Toolbox route, template, account codes, tax names and tracking options.
For bookkeepers and finance teams reviewing an import file before using Xero.
Needs pasted journal rows or readable exports, the chosen route, its current template and destination account, tax and tracking lists. Preflight needs no account connection or paid API; importing afterward requires the user's own Xero access.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes. Installing it does not run a bundled program or connect an account.

Preflight uses task text, attachments and readable local files you explicitly supply. These skills do not direct code execution, shell commands, software installation or API calls. They can return a complete proposed corrected CSV when requested; any requested output file is created by your assistant's existing file tools, not by a bundled program.

This is not a strictly offline workflow: optional source refresh uses the assistant's existing web/search tools to retrieve linked official Xero Central articles or a user-supplied official Xero documentation/template URL, the site's robots.txt and redirects that remain within official documentation. If a page returns an empty text shell, searches for official article titles may retrieve indexed text. The skills also direct verification of regional rules/templates when current rules are needed or supplied settings conflict. Requests disclose public documentation URLs or titles and ordinary connection metadata to the documentation sites and the assistant's web/search providers; private journal rows must never appear in requests. If retrieval fails, the skills use the dated bundled references and identify the affected unresolved rule. Supplied-text preflight can use those references without retrieval.

The skills can explain user-led template download, organisation selection/connection and import/preview steps in Xero or Conversion Toolbox. These are separate actions in the user's own account; the plugin does not authenticate, access ledger data, create accounts, upload journals, post entries, send messages or change account settings. Approved Toolbox import posts to the ledger, so it remains a separate user action.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Homepage, support and privacy links identify package information; the Xero source links above are actual optional retrieval destinations.

- **Native journal preflight:** checks grouping, signed amounts, regional dates, the 300-line file limit, exact account/tax/tracking values and draft versus posting readiness.
- **Conversion Toolbox journal preflight:** checks number-based grouping, one/two amount columns, source-to-destination mappings, route-specific dates and draft/approved preview settings.

Return row-specific findings, proposed corrections and debit/credit totals for each journal. Keep the original data and journal intent. If the route is missing, provide useful arithmetic and ask which route to use. Supply complete files for a complete-file verdict; a pasted sample covers only that sample.

Use the native template downloaded from the destination organisation. For Toolbox, supply its template or actual headers plus field, account, tax and tracking mappings. Include organisation country, base currency and intended journal boundaries. For tax-bearing rows, include the amount basis. Include any error message and flag old or incomplete reference lists. No credentials are needed.

Version 0.1.0. Public Xero sources checked 2026-10-11. The source register in each skill records route scope and freshness.
