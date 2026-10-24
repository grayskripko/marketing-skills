# Payroll Taxes

Builds a US federal payroll tax deposit and filing calendar from your payroll records and IRS notices.
For US employers and payroll staff. Needs the tax year, required return form, payday liabilities, lookback return totals and relevant notice text. Paste text or exports, attach selected records, or describe the screenshot. No account, paid API or installation is needed for this input path.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon, with development notes and text evaluation records also present in this working folder. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes. Installing it does not run a program or connect an account. The skills do not direct code execution or software installation.

These skills analyze task text, attachments and local files that you explicitly supply, and direct your assistant's existing web/search tools to verify public guidance. They may retrieve IRS publications, form instructions, tax calendars and disaster-relief pages on `irs.gov`, plus relevant SSA employer guidance on `ssa.gov`, following only necessary official links and redirects on those domains. Search queries contain public rule names, forms, years or public relief locations, never private payroll data or notice text. Searches are processed by the assistant's search provider; retrieval discloses the requested URL and ordinary connection metadata to the official site and the assistant's tool provider. This workflow therefore makes network requests. If retrieval is unavailable, the assistant keeps a useful draft, marks affected dates provisional and asks for the applicable official excerpt.

No account login, uploads, payments, tax filings, message delivery, calendar writes or account-setting changes are authorized. Checklist actions such as filing returns or furnishing W-2s are tasks for the user, not actions performed by the plugin. The assistant may explain how you locate records or export a payroll-provider report; it does not access that provider. The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation and selected files under its own terms. A local checklist file is saved only at a destination you request, using your assistant's existing file tools, not a bundled program. See [PRIVACY.md](PRIVACY.md).

## Skills

The embedded calendar rules cover original periodic Forms 941, 940, 943, assigned 944 and W-2/W-3 obligations. Other payroll forms and correction calendars require their own current official instructions; stated IRS notice deadlines and requested response tasks are extracted, while substantive notice disputes remain outside these checklists.

- **Payroll deposit checklist:** derives deposit dates, schedule changes, holiday adjustments, small-balance exceptions and FUTA carryforward.
- **Payroll filing checklist:** lists return deadlines, conditional filing alternatives, reconciliation records and notice-response actions.

Example request: “We file 941. Here are our lookback totals and payday taxes. Build the federal deposit and filing checklist for Q4, using this IRS notice.” Mask SSNs, full EINs and bank details; employee-level data is normally unnecessary. If records are missing, the assistant can walk you through locating the relevant return totals and exporting your provider's liability-by-payday report. It does not connect to the provider.

Rules are sourced from IRS publications and instructions checked October 11, 2026. Publication 15 and W-2/W-3 instructions are 2026; 941 instructions are March 2026. The current 940, 943 and 944 pages still show 2025 instructions. Year-specific facts and relief must be checked before finalizing later deadlines. No state calendar, contractor reporting, wage calculation, filing, payment or calendar-account updates are provided.
