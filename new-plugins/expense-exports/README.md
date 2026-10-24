# Expense Exports

Explain why Brex says exported when expenses are missing from QuickBooks or another ERP. Use batch history, downloaded CSV, ERP rows, required GL fields and export-type changes.
For finance operations teams closing books from Brex records. Needs pasted batch history, downloaded CSV or readable exports, ERP rows, required-field settings, and any export-type change dates. No account connection or setup is required.

## What this package runs and connects to

This package provides Markdown skills and reference text, JSON metadata, and a static SVG icon. It bundles no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The current folder also contains development notes and evaluation records; those are not runtime components and should be kept outside the submitted release folder.

The skills analyze task text and readable files you explicitly supply. They permit your assistant’s existing web tool to retrieve public Brex help pages linked in the source registers or supplied by you to verify changed rules. Both source registers also instruct reopening relevant pages before the planned submission and when supplied errors or UI differ. This optional retrieval makes network requests to Brex (the bundled links use `https://www.brex.com/support/`). The requested URL and ordinary connection metadata are disclosed to the destination and the assistant’s tool provider; expense rows, names, account identifiers, credentials, and other private task context must not be included in requests. If retrieval is unavailable, supply the relevant help text and identify any rule that remains unverified.

The skills do not instruct code execution, software installation, web search, API calls, account connections, message delivery, publishing, or account mutations. They return workpapers and proposed correction plans. Advice to refresh mappings, import CSV rows, export payments, change fields or forms, or close externally paid bills describes actions you perform in your normal Brex or ERP workflow; the plugin does not perform them. No file-writing tool is prescribed by the skills. Any output file you explicitly request uses your assistant’s existing file tools.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments, tool requests, and generated files under its own terms. The GitHub support link is a reference, not an instruction to retrieve or send anything.

## Skills

- **reconcile-expense-exports**: explain which expenses are present in the supplied ERP records, downloaded only, failed, or unresolved; produce a delivery workpaper with the next action.
- **preflight-expense-export**: identify missing fields, mapping errors, and reimbursement export-type cutover problems; produce a correction plan before retrying.

Paste headers with rows and identify the ERP company, entity, currency, period, export route, and extraction time where available. Batch details and error text help distinguish missing delivery from missing preparation. Omit employee names and account details that the comparison does not need.

## Files and network

The skills read supplied text and files. They can fetch only the public Brex help pages linked in their source references, and Brex help pages the user supplies, to verify changed rules. Fetches contain no expense rows, names, account identifiers, or credentials. No web search, telemetry, account login, API, or connector is required. Outputs are workpapers and correction plans; account changes are performed in the user’s normal Brex and ERP workflow.

Source observations are dated 2026-10-11. The source register separates observed content from publication dates.
