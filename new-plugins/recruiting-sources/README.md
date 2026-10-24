# Recruiting Sources

Audit Greenhouse source attribution and report interpretation from application rows, gh_src tracking links and source-quality exports.
For recruiting operations teams using Greenhouse. Needs pasted text or supplied CSV/XLSX exports, tracking links and report settings; no account, keys or setup required for analysis.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes. Build notes, reviews and test records are development evidence, not runtime components.

The analysis workflow uses only task text, attachments and local files you explicitly supply. Supplied tracking URLs and sanitized application payloads are inspected as text; tracking URLs are not opened. The skills do not direct code execution, software installation, API calls, account access, outreach, record changes, publishing or settings changes. Instructions about API form fields describe the evidence to inspect and developer checks; they do not submit applications.

This package has an optional network workflow: when you request a documentation refresh, the assistant may retrieve only named public Greenhouse documentation pages on `support.greenhouse.io`, `developers.greenhouse.io` or `docs.greenhouse.io` and their redirects, using its existing retrieval tools. The reference maintenance sections also instruct maintainers to reopen cited sources before submission and when definitions change. These requests disclose the requested URL and ordinary connection metadata to the destination sites, redirect destinations and the assistant's tool provider. Candidate rows, export contents, candidate details and tracking tokens are not sent in those requests. The supplied-material analysis workflow does not request network access; the documentation refresh does.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

- **audit-source-attribution**: an application exception ledger, with the observed token path and the next evidence needed.
- **interpret-source-quality**: a source comparison separating volume, pipeline progress and hire rate, plus a filter reconciliation.

Paste application IDs, candidate IDs when available, job IDs, source labels, applied dates, migration flags and source-token mappings. For reports, include the export timestamp, visible filters, job scope and stage/milestone layout. Replace candidate names and contact details with stable row IDs. Each skill works with partial inputs and marks the precise missing detail.

Current Greenhouse documentation is embedded in dated references; see the execution and connection scope above for the optional documentation refresh.

The package contains Markdown skills and an SVG icon. Read [PRIVACY.md](PRIVACY.md) for data handling and [BUILD-NOTES.md](BUILD-NOTES.md) for build evidence.
