# Expense Reimbursements

Write an employee expense reimbursement policy and check receipts for missing evidence.
For people managing US employee reimbursements under an accountable plan; other countries and actual payment execution are outside current scope.
Policy drafting covers accountable-plan substantiation, business-purpose evidence, advances, excess-return handling, and receipt exception review.
Needs your reimbursement rules and expense records: paste text, provide an export, or describe what a screenshot shows. No accounts, keys, paid APIs, or setup are required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The Claude and Codex manifests are platform metadata, not server launch configurations.

These skills analyze task text, attachments, and local files that you explicitly supply, using the bundled reference. They do not instruct the assistant to run code, install software, call APIs, send messages, publish content, or change account settings. They are not strictly offline: when a rule or rate needs refreshing, the assistant may fetch public IRS pages/PDFs at `irs.gov` or federal regulation pages at `ecfr.gov`, plus those sites' `robots.txt`. Redirects stay within those domains and fetching restrictions are respected. Private employee, receipt, and company facts must never be included in network queries or requests. If retrieval fails, supply an official excerpt and leave unresolved dates or rates marked. Source-register URLs support this optional refresh; GitHub repository and support URLs are informational links, not account connections or automatic issue submissions.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Public-source requests go to the allowed source sites through your assistant's existing retrieval tools. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Ask for | You get |
|---|---|
| “Make these rules into a staff expense policy.” | A policy draft with the supplied limits preserved and unresolved decisions marked. |
| “What is missing from these receipts?” | A row-by-row evidence list separating company approval, business records, and payroll concerns. |
| “What is left from this travel advance?” | A reconciliation of supported expenses, returned money, and unresolved amounts. |

The two skills are `expense-policy-draft` and `expense-evidence-review`. A request for both a policy and a receipt check can use both.

The embedded reference covers the three accountable-plan conditions, timing safe harbors, lodging and $75 receipt rules, mileage records, 2025 and 2026 mileage rates, and excess advances. Company meal reimbursement is kept separate from the employer's meal deduction. Federal rules do not set a universal private-employer reimbursement rate or determine state reimbursement duties.

Start with the policy, employee expense rows, travel dates, amounts and currency, business purpose, payer, approvals, and any advance or refund. Employee aliases are enough. For a screenshot description, say which fields are visible and which are unclear; a described image cannot establish unseen details. You can ask the assistant to help you choose relevant columns from your existing export. It does not connect to an expense system.

## Data and network

Reads only the material you supply for this task and the bundled reference. No automatic network requests. If a rule or rate needs refreshing, the assistant may fetch public IRS pages/PDFs at `irs.gov` or federal regulation pages at `ecfr.gov`, plus those sites' `robots.txt`. It follows redirects only within those domains and respects fetching restrictions. No private expense data is included in a search query or request. If access fails, it can use an official excerpt you paste and mark the unresolved date or rate.

No telemetry, account access, payments, payroll edits, or tax filings. This is a set of instructions and reference text, with no executable scripts or service. Your assistant processes the conversation under its own terms. See [PRIVACY.md](PRIVACY.md).

Sources were checked on 2026-10-11: Publication 15 (2026), Publication 463 (2025, the current edition at that check), and current federal reimbursement regulations. The 2025 publication's mileage rate is not used for 2026 travel. See the [source register](skills/expense-policy-draft/references/us-accountable-plan.md) for effective periods and update instructions. Per diem dollar calculations require a current official rate table and the employer's method; none is assumed.

Scope excludes personal tax returns, contractor reimbursements, state reimbursement mandates, and benefit valuation. Policy drafts and evidence findings do not adopt a policy or authorize a payment.

MIT. See [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
