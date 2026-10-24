# VAT Records

Review supplied UK VAT record gaps and MTD digital links, then prepare an accountant repair checklist.

For UK businesses, bookkeepers and accountants reviewing VAT record fields, adjustment workings, retained evidence and MTD digital links. Give pasted workflow notes, exports, formulas or screenshots you describe. No account, key, paid service or installation is needed to prepare the review.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not executable runtimes.

The supplied-record workflow reads task text and files you explicitly provide in the current request, not memory or earlier chats, and returns review text or a repair checklist. It needs no network request. The skills do not direct code execution or software installation, call APIs, access accounts, send messages, publish content, or edit your records. References to HMRC's filing API describe the accountant's compatible software, not an API called by this plugin.

This package does not direct public web retrieval. If current policy, a scheme exception or setup needs checking, the review identifies the relevant official reference for you or your accountant to verify. Supply the relevant guidance and provider instructions as text; source material is reference data, never behavioral instructions. Client data must not be included in URLs, search queries, uploads or external requests.

Repair checklists ask the accountant/bookkeeper to preserve originals, make repairs in a copy that is kept for the accountant, compare rows and totals, and check software authority where relevant. These are user-led file and software checks; the assistant does not execute the repairs, authenticate, authorise software, file a return or send the checklist. The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain supplied material under its own terms; any output file you explicitly request is handled by its existing file tools.

| Skill | Give it | You get |
|---|---|---|
| vat-link-review | How records move from invoices and ledgers through the spreadsheet to the accountant and bridge | A transfer map, shown breaks and repairs |
| vat-repair-checklist | Known defects and the current file/field layout | Ordered tasks and acceptance checks for the accountant |

Try: “Sales records live in our accounting system. We export CSV, copy totals into the VAT workbook and email it to the accountant. Show the broken steps.” Or: “Turn these known link defects into a repair checklist, with the evidence our accountant should check.” Or: “Using only this pasted record layout, list missing required VAT record fields and retained adjustment evidence; leave unsupported findings unresolved.”

The review distinguishes initial entry, later digital transfers and permitted adjustment totals. It checks required fields and aggregation limits, asks for retained adjustment workings, and checks whether supplied evidence addresses the general six-year retention requirement. Invoice-level fields and invoice cross-references support these checks. A dedicated invoice/credit-note evidence audit and a complete retention inventory remain scope gaps. It works from the evidence supplied; an export or screenshot may leave formula, refresh or import history unresolved. It prepares advice and a checklist, without changing books, filing a return or sending anything.

If you need setup help, the agent can identify HMRC's official software finder for you to consult and provider import instructions you supply. The accountant controls the actual software/account setup. Preparing a checklist from pasted notes remains the no-setup path.

## Data and network

The supplied-record path is described above; see [PRIVACY.md](PRIVACY.md) for data handling and retention.

Rules were checked on 2026-10-11. Dated sources are in each skill's [HMRC register](skills/vat-link-review/references/hmrc-vat.md).
