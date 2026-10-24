# SF425 Reporting

Map a supplied NIH award ledger to draft SF425 fields, preserving accounting basis, PMS cash-field treatment, SNAP exceptions and annual/final reporting dates.
For NIH grant accountants and sponsored-programs staff. Needs pasted text or ledger exports, the Notice of Award, reporting dates, and available PMS cash snapshots. No keys, accounts, installs or paid APIs are needed for drafting.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Supply | Receive |
|---|---|---|
| draft-sf425 | ledger, stated cash/accrual basis, award terms, PMS snapshot | draft field table with source rows, calculations, reconciliation issues and missing details |
| plan-sf425-dates | budget and competitive-segment dates, SNAP status, recipient type, approved extensions | annual/segment-final calendar with dates and the award terms that decide them |

Paste CSV rows or attach a readable export. Separate each award and PMS document; include the export cutoff and whether totals are cumulative. Include credits, payable balances, open obligations, recipient contributions, program income treatment and indirect-rate details when relevant. Summaries work when their scope and totals are stated. Redact payroll names, bank details and unrelated identifiers.

The draft retains PMS-populated lines 10a–10c instead of reconstructing them from an accrual ledger. It distinguishes expenditures from outstanding obligations, flags incomplete final balances, and leaves certification for the award's authorized official. For annual NIH reports, the budget period controls coverage and the calendar quarter controls the deadline. A current official-source mismatch in annual dates is shown when it affects your calendar.

## Sources and network

Official GSA, NIH, eRA and PMS knowledge is embedded in [the dated source register](skills/draft-sf425/references/sources.md). During drafting, network requests: none. The assistant reads supplied text/files and these packaged references. The package contains instructions, reference text and an SVG icon; no connectors, executable services or telemetry. Optional requests to research a newer policy are separate from these export-based skills.

## Files

[Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Build record](BUILD-NOTES.md) · [Review](REVIEW.md) · [Validation results](tests/RESULT.md)

Support: https://github.com/grayskripko/marketing-skills/issues
