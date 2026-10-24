# CMS1500 Claims

Check CMS-1500 claim boxes before submission and get corrections and missing evidence under US Medicare Chapter 26 and supplied payer instructions.
For billing staff reviewing US professional claims before submission.
Needs pasted item values or readable exports, payer identity, service dates, and any payer instructions you want applied. No accounts, keys, installations or paid APIs are required.

## Skills

- **cms1500-field-preflight** — check the whole supplied claim or selected fields; get item and line corrections, arithmetic fixes and missing evidence.
- **cms1500-provider-roles** — reconcile referring, ordering, supervising, rendering, service-facility and billing roles; get conflicts and a supported field mapping.

Paste a numbered item map, CSV, JSON or readable text export. State whether omitted fields are blank or merely outside the export. Use claim aliases and provider-role aliases; omit beneficiary identifiers and contact details when they do not decide the check. Add payer instructions with their effective date and service-specific evidence such as orders, signatures or authorization records.

Medicare Chapter 26 rules are embedded. Other payer requirements come from the instructions you supply. A partial export yields findings for the supplied fields and a targeted evidence list. The workflow produces a correction worksheet; submission, denial appeals, institutional claims and coding selection are separate jobs.

## Data and network

The skills read only the pasted text and files you select. They fetch no URLs by default. If you request a rule refresh, the agent opens the official CMS URLs listed in [references/sources.md](references/sources.md), including their CMS redirects, or an official payer URL you provide. No claim contents or personal identifiers go into web queries. There are no connectors, account reads, telemetry or plugin-managed storage.

[Privacy](PRIVACY.md) · [Source register and field rules](references/sources.md) · [Build notes](BUILD-NOTES.md)
