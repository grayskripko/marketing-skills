# Grant Applications

Compare a grant application, budget and attachments with the funder’s actual instructions and amendments.
For nonprofit staff preparing work for their authorized grant owner and finance reviewer. Supply the notice, amendments, draft, budget and approved organization facts. No account, API key or paid service is required.

## What this package runs and connects to

The grant-review workflows use Markdown instructions and reference text, JSON metadata, and a static SVG icon. The manifests configure no installers, hooks, MCP or LSP servers, account connectors, or background processes. Installing the plugin does not launch a process or connect an account.

The skills work only from task text, attachments, and local files that you explicitly supply. They prohibit web search, URL retrieval, account access, dependency downloads and paid APIs; a supplied URL is treated as text, and the assistant asks you to paste the relevant content. Grants.gov source links and GitHub publisher/support links are references, not retrieval instructions or connection endpoints. The skills permit the assistant's existing local file and calculation tools: budget checking requests local calculation when available, and draft checking requests a local word/character counting tool, with explicit arithmetic or internal counting as fallbacks. Those host tools may execute code; this is not a no-execution workflow. The skills do not instruct software installation, application submission, message delivery, publication or account-setting changes. They prohibit overwriting originals and retaining copies by default; replacement passages are returned in the answer rather than written into source files.

This release contains only skill instructions, reference notes, JSON metadata, a static SVG icon, privacy documentation and the MIT license.

The publisher operates no task-data collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain conversations, attachments and host-tool artifacts under its own terms.

| Skill | Give it | You get |
|---|---|---|
| read-grant-requirements | Notice/RFP, amendments, questions, supplied AI-use restrictions; approved facts and readable attachments if checking what you have | Requirements with conditions, exceptions and exact source locations; attachment gaps and actions |
| check-grant-draft | Instructions, application draft, approved facts and readable attachments or inventory | Most important fixes, replacement passages where allowed, and missing content |
| check-grant-budget | Budget rows with quantities, units, currency, project dates and supplied cost rules | Recalculated figures, formulas and differences from the application or funding totals |

## Preparation coverage

The skills check supplied requirements, budgets and drafts, and return supported replacement passages where the funder permits AI writing. They do not prepare a complete application from a brief.

## Using it

Paste the relevant sections or provide readable files selected for this task. Include funder/program, jurisdiction, version and dates where known; missing values stay unknown. Remove donor and beneficiary identifiers, bank details and signature images. Keep signer role, approval date and signed/unsigned status where required for the check. Pasting text needs no setup. File reading and spreadsheet calculations depend on your assistant’s local tools; unreadable scans need a readable excerpt.

Examples: “Turn these amended instructions into our checklist.” “Check this answer against question 3 and our approved program notes.” “Reconcile these session costs with our grant request.”

The funder’s own instructions decide the requirements. An attachment list does not prove its contents. AI-use restrictions may allow checks but forbid writing replacement answers. The skills follow those restrictions. Budget corrections show the original figures and calculations. They do not approve new spending commitments.

## Limits

Use the results to prepare for authorized grant and finance review. The plugin does not find grants, submit applications or predict awards. It does not certify eligibility or compliance, validate portals or judge PDF layout from extracted text. No live funder updates are retrieved. The result covers the supplied versions and readable material.

## Data and network

Nothing is fetched: no searches, URL requests, account connections, dependency downloads or paid APIs. Only pasted material and supplied files selected for this task are read. Local tools may calculate figures or count words; originals are not overwritten. The plugin has no service, telemetry or storage. Your assistant processes the conversation and files under its own terms. See [PRIVACY.md](PRIVACY.md).

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). [MIT license](LICENSE).
