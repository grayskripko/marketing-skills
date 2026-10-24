# DPA Agreements

Check what is missing from an EU supplier DPA, fill its processing annex, and turn conflicting security answers or subprocessor lists into questions for the vendor.

For EU procurement, privacy and compliance teams reviewing supplier processing terms. Provide pasted DPA text or selected text, PDF, CSV or spreadsheet exports containing party roles, processing details, security answers and subprocessor lists. No vendor accounts, API keys or additional software are required. Enable the plugin in a host that supports its skills.

| Skill | Result |
|---|---|
| dpa-commitments | Missing commitments and proposed agreement changes |
| dpa-processing | Activity-specific roles and processing schedule with unknowns visible |
| dpa-vendor-questions | Vendor-ready questions tied to clauses, export rows and report scope |

Examples: “Check this supplier DPA for missing duties.” “Fill the processing annex from these notes.” “Give us five questions based on the security export and subprocessor list.”

The reference pack distinguishes Article 28 controller–processor clauses (2021/915) from transfer clauses (2021/914). It includes EDPB role guidance and Opinion 22/2024 on downstream processors. Sources were verified on 2026-10-11; source versions and provision locators are in [official sources](references/official-sources.md).

## Data and network

Runtime fetches: none. The skills read pasted text and files you select for the task. They draft in the conversation and do not contact vendors or change agreements. They ship no connectors, scripts, telemetry or storage service. Use data categories instead of individual records and remove unnecessary identifiers. For updated official guidance, paste its text with its date and URL.

[Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
