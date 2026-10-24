# MTD Income Tax

Turn my income and expense export into a checked pack for my next UK quarterly update.
For sole traders and landlords preparing UK MTD Income Tax updates. Needs pasted records, CSV/spreadsheet exports, or screenshot descriptions, plus the tax year and update-period choice. No keys, account access or paid API are required to prepare the pack.

Confirm your MTD participation or HMRC notice. If eligibility is unresolved, the skills guide you through current HMRC qualifying-income and exemption checks alongside the record pack. They also document the digital source and transfer route, categorize transactions, repair corrections and prepare a year-end handoff for deferred expenses and annual adjustments.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON platform metadata, and a static SVG icon, with Markdown/JSON/CSV development and evaluation records also present in this working folder. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata, not a runtime.

This is not an offline-only workflow. Both skills instruct the assistant to verify public HMRC guidance when the tax year differs or is later, current policy is requested, or source/software wording conflicts; eligibility questions use current HMRC eligibility and qualifying-income guidance. Setup help uses the public software guidance and finder. The repair skill also directs obtaining current amendment guidance or accountant advice if a tax return has already been submitted. Using the assistant's existing web tool, public retrieval is limited to `www.gov.uk` and the linked finder at `www.tax.service.gov.uk/find-making-tax-digital-income-tax-software/how-to-find-software`, including redirects within those hosts. Requests disclose the public URL and ordinary connection metadata to those sites and the tool provider; user records must never appear in requests or search queries. These public guidance URLs are retrieval destinations, not just citations. GitHub publisher/support links are informational links, not skill-directed connections.

The assistant works from records, exports, screenshot descriptions and templates you supply, may read user-designated local files, and may write pack files you explicitly request using its existing file tools. In the repair workflow, proposed source changes remain a handoff until you authorise editing the actual source file. The skills show formulas and inputs; they do not direct running code, shell commands, installing software, or calling submission APIs. They give user-led instructions for choosing and authorising compatible software, correcting digital records, importing/exporting CSVs or using supported digital links, comparing software previews, and submitting or resending updates in that software. The plugin does not connect to an account, handle credentials, submit to HMRC, send messages, or claim acceptance.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Requested output files and authorised source edits are managed by the assistant's existing tools, not a bundled program.

Two skills:
- **prepare-quarterly-pack**: cumulative category totals, mapped records, exceptions, reconciliation and accountant/software handoff.
- **repair-quarterly-records**: corrected rows, before/after totals and the next-update or fourth-update repair handoff.

Tell the assistant your business sources, standard or calendar periods, export coverage, accounting basis, and any updates already sent. For property, include ownership share and whether joint-property expenses are deferred. If a screenshot amount is unclear, the pack leaves it unresolved.

This plugin prepares records and does not submit through HMRC-compatible software. Pasted data and screenshot descriptions cannot establish that the underlying digital record chain is complete. Filing requires HMRC-compatible software and the user's software authorisation. The assistant can walk you through selecting suitable software, confirming its import template, mapping fields and comparing its cumulative preview with the pack. It does not connect to HMRC or submit updates. An export pack remains available without setup.

The pack uses cumulative periods, not isolated three-month totals. It separates each sole trade, the UK property business and the foreign property business. It distinguishes corrections from year-end tax adjustments and keeps unresolved rows visible.

Guidance checked 11 October 2026. The historical package plan targeted a 13 October submission; this is not the user’s schedule. Recheck applicable guidance for the user’s actual tax year and intended action when freshness affects the decision, and before a submission handoff. Dated official references are included with each skill. Tax-return preparation, VAT, corporation tax and tax-liability calculations are outside this scope.
