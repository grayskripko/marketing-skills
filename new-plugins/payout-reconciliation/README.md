# Payout Reconciliation

Match payment settlements to bank deposits and explain the clearing balance from supplied exports. For bookkeepers and small-business owners preparing reconciliation notes for accountant review.

Start with Stripe CSV exports. You need authorized processor and bank exports; a ledger comparison also needs ledger rows and balances. Downloading new Stripe reports requires access to your existing account. Pasted rows work without account access, a connector, keys or a paid API.

## What this package runs and connects to

The three skills analyze task text, attachments and authorized local files you explicitly supply, plus bundled report notes. They do not direct web searches, URL retrieval, API calls, credential handling, account connections, message delivery, payments or ledger edits. Stripe documentation and GitHub support URLs identify sources or support pages; they are not retrieval instructions. Paste relevant content when a link alone does not supply the evidence.

This is not a strict pasted-text-only, no-execution workflow. CSV/XLSX reading, OCR for scans and exact calculations on many rows use your assistant's existing tools, which may execute host-managed code and create temporary or requested output files. No skill specifies a shell command, installer, dependency installation or API endpoint. The skills return reconciliation text and tables; removing duplicate rows means excluding them from analysis, not overwriting source files.

`choose-settlement-exports` can explain which Stripe reports and CSV sections you should download. You perform that optional download in your existing authorized Stripe account; it involves your browser, Stripe and Stripe's account permissions. The assistant does not log in or download reports for you. Pasted headers and rows remain the no-setup alternative.

The runtime instructions, reference text, JSON platform metadata and static SVG provide no executable runtime, hooks, MCP or LSP server, connector or background process. Both platform manifests are metadata. However, this working folder also contains development material: `tests/run-eval.py` is an executable evaluation harness, not a skill entry point. If manually run, it invokes the local Codex CLI nine times with test prompts and skill text, uses the CLI's configured model service, and writes inputs, answers, logs and mappings. It still targets the historical `settlement-reconcile` path. Do not treat this folder as a clean no-code release: exclude development tests, review records and build notes from a submission artifact as described in the packaging guidance.

The publisher operates no task-data collection, telemetry or storage service for these skills. Your assistant provider processes and may retain conversations, uploads, tool execution and generated files under its own terms. Any output file you explicitly request is created by your assistant's existing tools, not by a bundled reconciliation program.

## What you get

| Skill | Give it | You get |
|---|---|---|
| choose-settlement-exports | report headers, payout mode and question | exact files and fields needed |
| match-payouts-to-bank | itemized activity, payout records and bank rows | settlements linked to source rows, deposits, differences and possible matches |
| explain-clearing-balance | processor balances/activity, ledger rows and outstanding items | calculation from opening to ending balance and evidence explaining money still at the processor or on its way to the bank |

## Examples

- “Which exports do you need for our automatic payouts in September?”
- “Match these payouts to the bank and explain the fees and refunds.”
- “Why is the clearing account not zero at month end? Here are the balances and outstanding payouts.”

## How it works

A clearing account tracks money passing between the processor and bank.

Every match names its original rows. Fees and refunds count once. Equal amounts alone do not confirm a match. Each currency has separate totals. For manual and instant payouts, match the payout to the bank without claiming which sales funded it. If a required balance is missing, show the calculations possible and name the missing balance.

The assistant needs file-reading tools for CSV/XLSX and tools that calculate amounts exactly when processing many rows. Scans need text recognition (OCR) or readable transcriptions. The package contains instructions. It does not read spreadsheet files or scanned documents by itself. Paste small tables when those tools are unavailable. For other processors, supply the column definitions so the format can be checked. Those formats have not been verified.

Have an accountant review the reconciliation notes before adjustments. The assistant does not post entries, move money, decide tax or when to record revenue, or certify that the accounts are ready to close. Give the business name, period, accounting basis and jurisdiction when known. Missing details stay marked unknown.

## Data and network

The skills do not direct network fetches, credential handling, account connections or external sends. Optional user-led Stripe downloads, assistant-provider processing and the manually invoked development harness have the separate boundaries described above. Only user-supplied records and bundled reference notes are analyzed. Redact customer details and full bank identifiers; keep transaction references needed for matching. The AI host processes uploads under its own terms and may save conversations and generated files. This instruction package runs no separate service and keeps no separate data store. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Issues](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
