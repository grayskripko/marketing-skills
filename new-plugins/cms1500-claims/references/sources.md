# Official source register and field decisions

All sources read 2026-10-11. Scope: US Medicare professional paper claims, CMS-1500 02/12. Other payer instructions are supplied evidence with separate effective dates and service scope.

| Source | URL | Observed date/version and load |
|---|---|---|
| CMS professional paper claim page | https://www.cms.gov/medicare/coding-billing/electronic-billing/professional-paper-claim-form | HTTP 200; modified 2024-09-10. Explains electronic edit stages; title alone does not establish paper eligibility. |
| Medicare Claims Processing Manual Chapter 26 | https://www.cms.gov/Regulations-and-Guidance/Guidance/Manuals/downloads/clm104c26.pdf | HTTP 200; Rev. 12779 issued 2024-08-09; 78 pages. Current chapter linked by official index. |
| Supplied alternate Chapter 26 | https://www.cms.gov/regulations-and-guidance/guidance/manuals/downloads/clm104c26pdf.pdf | HTTP 200 after redirect to https://www.cms.gov/regulations-and-guidance/guidance/manuals/downloads/clm104c26.pdf. Byte-identical; not independent support. |
| CMS Pub. 100-04 index | https://www.cms.gov/Regulations-and-Guidance/Guidance/Manuals/Internet-Only-Manuals-IOMs-Items/CMS018912 | HTTP 200; live index links clm104c26.pdf on 2026-10-11. |
| CMS ASCA self-assessment | https://www.cms.gov/medicare/coding-billing/electronic-billing/administrative-simplification-compliance-act-self-assessment | HTTP 200; modified 2024-09-10. Paper exceptions and temporary/claim-specific scope. |
| CMS POS Code Set | https://www.cms.gov/medicare/coding-billing/place-of-service-codes/code-sets | HTTP 200; modified 2026-02-17. Current setting definitions. |

The chapter's posted age is a version observation. When the user requests a refresh, compare current revisions and effective dates with the service and receipt dates. Do not assign a future read date. Retrieval hashes/redirects are in [source checks](../tests/source-checks.json).

## Chapter 26 decisions

Every row below is paraphrased from the Chapter 26 URL above, read 2026-10-11. Section revisions differ from the overall PDF revision. Historical 08/05 and dual-use instructions are not current defaults.

| Section / items | Deciding rule | Evidence boundary |
|---|---|---|
| 10; form | Revised form is 02/12; photocopies of claim form unacceptable. | Text export cannot verify paper/print specifications. |
| 10; dates | DOB eight digits. Consistent six/eight digits across 11b/14/16/18/19/24A; 12/31 exceptions. | Convert only known dates. |
| 10.1 | Incomplete/invalid information may be returned as unprocessable; handling in Chapter 1. | Do not invent denial codes or an appeal remedy. |
| 10.2, Rev. 4232 issued 2019-02-08; 1–3 | Medicare box; required beneficiary ID/card name; DOB/sex. | Report item numbers instead of sensitive values. |
| 10.2; 5 | Patient mailing address and telephone entries. | Check presence without echoing values; redacted/omitted is not confirmed blank. |
| 10.2; 4/6/7/10/11 | Required 11: NONE ordinarily when no primary insurance; otherwise policy/group and insured dependencies. Accident/employment answers can signal primary coverage. Paper MSP needs primary EOB. | Do not invent payer order or NONE. |
| 10.2; 9 family | Participating provider plus Medigap assignment triggers entries. 9a MEDIGAP/MG/MGAP prefix; 9d COBA Medigap ID, even with 9a. 9b blank on 02/12; 9c blank when 9d completed. Insurer-specific separate Medigap authorization is needed in 13; direct Medicare payment exceptions do not supply it. | Not all supplemental policies belong here. |
| 10.3; 11a–13 | Conditional insured DOB/sex; 11c primary PAYERID or complete plan name; 11d blank. 12 permits documented signature on file. 13 has assignment-only/participating direct-payment exceptions. | Supplemental payment processing can depend on accurate authorization entry. Never invent on-file consent. |
| 10.4, Rev. 10341 issued 2020-09-04, effective/implementation 2020-10-06; 14–18 | 14 onset date; chiropractic initiation and conditional 19 date; no Medicare 14 qualifier; 15 blank; conditional work/hospital dates in 16/18; routine foot care 19 needs last-seen date/attending NPI; chiropractic 19 x-ray date only when x-ray established subluxation. | Need service circumstances. |
| 10.4; 17/17b | DN referring, DK ordering, DQ supervising. Named person's NPI in 17b; 17a blank. Separate forms when different providers must be reported in item 17 across services; different orderer/supervisor identities in 17 and 24J/31 for one incident-to service do not alone require a split. | Incident-to uses initial-service practitioner who ordered the non-physician service. PT/OT/SLP dates from 2012-10-01 use plan-of-care certifier as referring, including incident-to therapy. Role evidence precedes qualifier; do not invent a referring physician. |
| 10.4; 19/24D | Unlisted/NOC procedure narrative in 19 or attachment; NOC drug name/dosage. Missing narrative causes unprocessable handling. Modifier 99 requires line-specific applicable modifiers in 19. | Obtain real narrative/modifier evidence. |
| 10.4; 19/20/32 | Anti-markup: performing physician NPI in 19, applicable outside-performance indication/acquisition charge in 20, supplier details in 32; separate paper claim per test. | Reference lab is not automatically anti-markup. |
| 10.4; 21/24E | Twelve diagnoses A–L maximum, no periods/narrative; 0 ICD-10-CM, 9 ICD-9-CM; one code set/form, from-date for spans. One primary diagnosis letter per Medicare service line. | Do not choose primary diagnosis without documentation. |
| 10.4; 22/23 | Medicare 22 blank. 23 one condition: applicable QIO, IDE/PMA, HHA/hospice NPI G0181/G0182, CLIA covered lab, or loaded ambulance pickup ZIP. Additional conditions separate forms. | Non-Medicare corrected-claim instructions may differ. |
| 10.4; 24 | Six billable lines, shaded halves supplemental. Required dates/POS/HCPCS/diagnosis pointer; four modifier slots; valid to-date for spans beyond one day. | Export cannot verify print placement. |
| 10.4; 24F/G/28/29 | F line charge; G actual days/units, 1 for one service, elapsed anesthesia minutes. 28 sums F; 29 covered-service patient payment only. Defaults described: 1 unit, 0.1 ambulance mileage if omitted. | Do not multiply F by G again or promise automatic rejection for missing G. For selected-box/line exports, the supplied-line sum is a subtotal until the user establishes that all billable lines are included. Special ambulance rounding/oxygen units require applicable detail. |
| 10.4; 24J/31 | Rendering NPI generally; described incident-to with non-supervising orderer uses supervisor in J and supervisor signature; orderer signs if supervising. Documented signature alternatives allowed. | Role match does not establish incident-to eligibility. |
| 10.4; 25–27 | Tax ID/type as applicable, omission can delay payment; optional account number; assignment consistent with participation/service policy including lab and ambulance assignment-only services. | Do not echo tax ID or infer participation. |
| 10.4; 32/32a | One actual service location/form. Later 2011 instruction requires location for all POS, superseding earlier home exception. DME order-acceptance location; independent lab test location. Conditional facility NPI; reference-lab performing name/address/NPI for receipts from 2015-10-01 even across MAC jurisdictions. | Billing address is not automatically service location. |
| 10.4; 33/33a/b | Required billing name/address/ZIP/phone and billing provider/group NPI; 33b generally unreported except specific-policy direction. | Different individual/group/facility NPIs may be correct. |

## Additional official decisions

ASCA self-assessment URL above, read 2026-10-11: physician/supplier small-provider exception is fewer than 10 FTEs. Do not substitute the separate fewer-than-25 provider threshold. Stated exceptions also cover specified roster/demonstration claims, certain MSP with multiple primary payers and OTAF adjustments, beneficiary/managed-care submissions, dental claims, foreign services by non-US providers, electricity/communication disruption outside provider control expected to exceed two business days, and providers averaging fewer than 10 claims/month in a calendar year. Qualifying self-assessors should not send a waiver request. Exceptions may be temporary or claim-specific; obtain the actual basis.

POS Code Set URL above, read 2026-10-11: 02 telehealth outside patient's home; 10 telehealth in patient's home, Medicare applicability/availability April 1, 2022. 19 off-campus outpatient hospital, 22 on-campus outpatient hospital (2016 descriptions). 27 outreach site/street effective October 1, 2023. POS setting definitions do not establish service coverage or modifiers.

Professional paper page URL above, read 2026-10-11: initial basic-standard electronic edits can reject a batch; implementation-guide edits reject individual claims; Medicare payment/coverage edits may reject or deny individual claims. Do not call every rejection a denial or infer codes from field errors. Paper preflight does not validate 837P syntax.

## Authored workflow choices

Correction worksheets, aliases, absent-from-export distinction and one deciding question are workflow choices, not CMS requirements. No numerical readiness score is used. Field completion does not establish clinical, enrollment or service-policy evidence.

## Conditional decision layer reverified 2026-10-11

Source: [CMS Chapter 26](https://www.cms.gov/Regulations-and-Guidance/Guidance/Manuals/downloads/clm104c26.pdf), Rev. 12779 issued 2024-08-09; read 2026-10-11. These branches control the shorter ordinary-rule summaries above.

| Section / item | Deciding rule | Supplied evidence needed |
|---|---|---|
| 10.2 / 10d | Medicaid-only entry; prefix the Medicaid number with MCD. | Medicaid entitlement; worksheet uses an identifier placeholder. |
| 10.2 / 11 | Non-face-to-face lab may reuse retained MSP information. Reference lab with none enters None. Face-to-face lab collects MSP and bills accordingly. | Encounter type and retained-MSP status; ordinary office claims do not inherit this exception. |
| 10.2–10.3 / 11, 11b | Reported termination of previously primary insurance: NONE then 11b. Retirement entry is RETIRED plus six/eight-digit retirement date, right of vertical dotted line on 02/12. | Actual terminating event and known date; preserve the consistent date-format rule. |
| 10.4 / 19 | Independent laboratory obtaining a specimen from a homebound or institutionalized patient enters Homebound. | Documented specimen collection and patient circumstance, not merely a home POS. |
| 10.4 / 32 | Certified mammography screening center enters six-digit FDA-approved certification number. | Center certification; distinct from 32a NPI and 23 CLIA. |
