# Selfpay Estimates

Prepare a US uninsured/self-pay good faith estimate from approved services, codes, fees and dates; check CMS request/scheduling deadlines, model fields and recurring-service treatment.
For clinic administrators and billing staff. Paste an approved service list, fee schedule, dates and patient payment status, or supply a text/CSV export. No clinic account, API key, additional software or paid API is needed.

| Skill | Input | Output |
|---|---|---|
| selfpay-estimate-prepare | Approved services, codes, cash-pay fees, dates and payment status | Itemized estimate draft, provider totals, recurring scope and delivery deadline |
| selfpay-estimate-check | Existing estimate plus approved corrections and scheduling/request history | Corrected fields and charges, deadline result and missing details |

Use “Make a cash-pay estimate from this approved fee list” or “Check this GFE for weekly visits.” Clinical code selection, insured copays and dispute filing are separate jobs.

Use a patient alias in pasted inputs. Name, birth date and provider identifiers can be completed in the practice's own system. Missing fields stay marked; a draft with missing required fields is not marked complete. Patient-rights statements belong in the patient document.

## Sources and network

The embedded source register was checked on 2026-10-11. It covers CMS guidance through Part 5 (December 13, 2024), the model form, co-provider enforcement policy and federal holidays. The CMS-hosted example still displays an OMB expiration of 11/2025; the package uses its fields without claiming a renewed form approval.

The skills work with pasted text and supplied files. For a current-rule question or source refresh, the assistant may fetch public CMS pages/PDFs, the official eCFR or GovInfo rule text, OPM holiday tables and RegInfo form-status pages, including public redirects. Searches are restricted to cms.gov, ecfr.gov, govinfo.gov, opm.gov and reginfo.gov and use policy terms only. No patient or practice data goes into URLs or searches. No account connectors, telemetry, patient messages or uploads.

[Privacy](PRIVACY.md) · [Build notes](BUILD-NOTES.md) · [MIT license](LICENSE)
