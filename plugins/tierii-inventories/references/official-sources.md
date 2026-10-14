# Sources for Tier II inventory rules

Every source below was opened and read on 2026-10-13. The package makes no network requests at run time; these notes were written when it was built. Federal rules only: state programs can add chemicals, lower thresholds or require exact amounts, and the user supplies those. Facility applicability and exemptions are decided by the reporting owner.

## 1. 40 CFR part 370 — hazardous chemical reporting (current text)

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-J/part-370 — the browser page shows a bot check to scripted clients; the same text was read through the eCFR API, https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=370 (title 40 up to date as of 2026-10-08; part 370 last amended 2026-08-21 by 91 FR 37022). Compared with the 2025 annual edition, https://www.govinfo.gov/content/pkg/CFR-2025-title40-vol30/xml/CFR-2025-title40-vol30-part370.xml: thresholds, mixture rule and range codes unchanged; hazard-category definitions moved to 370.3 and aligned with the 2024 OSHA standard.
- 370.10(a)(1): EHS present at any one time at or above 500 lb or the TPQ, whichever is lower.
- 370.10(a)(2): other hazardous chemicals 10,000 lb; retail gas stations: gasoline 75,000 gal and diesel 100,000 gal, all grades combined, only for tanks entirely underground and in compliance with UST rules all year.
- 370.13: substances excluded under EPCRA 311(e) (FDA-regulated items, solids in articles without exposure, consumer-form products, research labs and hospitals under supervision, routine agriculture, fertilizer held for retail sale).
- 370.14(a): EHS — add quantities in all mixtures and all other forms across the facility, even when the mixture is also counted; non-EHS — either add the component across mixtures and other forms, or count the mixture as a whole.
- 370.14(b): the option for each mixture must be the same for SDS (311) and inventory (312) reporting unless impossible.
- 370.14(c): component = weight percent × mixture weight in pounds; not counted at ≤1%, or ≤0.1% for a carcinogen.
- 370.40(a), 370.45(a): inventory due by 1 March for chemicals present at any time during the previous calendar year at or above threshold.
- 370.42(s)(6)–(8): maximum amount on any single day; average daily amount; maximum number of days on site; for a mixture, the total mixture amount and each EHS amount.
- 370.43: range codes 01–13 (pounds) and the note to convert volume to pounds with a density factor; a SERC or LEPC may require exact amounts or ranges no broader than these.

## 2. 40 CFR part 355 — solid EHS TPQs and reduction factors

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-J/part-355/subpart-B — read through https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=355&section=355.15 and &section=355.16.
- 355.15: solids with two TPQs (e.g. 500/10,000): lower TPQ if powder <100 microns, in solution, molten, or NFPA reactivity 2–4; otherwise 10,000 lb.
- 355.16(b) and (c): 0.2 factor for solids in solution and 0.3 for molten solids; the notes say these reductions must not be used to determine the amount present at one time for 40 CFR 370.10.

## 3. EPA 2026 rule on hazard categories

EPCRA Hazardous Chemical Inventory Reporting Requirements: Conformity With the 2024 OSHA Hazard Communication Standard, 91 FR 37022, 22 June 2026. https://www.federalregister.gov/documents/2026/06/22/2026-12426/epcra-hazardous-chemical-inventory-reporting-requirements-conformity-with-the-2024-osha-hazard (bot check to scripted clients; metadata read through the Federal Register API) and full text https://www.govinfo.gov/content/pkg/FR-2026-06-22/html/2026-12426.htm.
- Effective 21 August 2026; compliance date for the new hazard categories 1 January 2028, expected in the 2027 reports due 1 March 2028.
- 2017–2026 EPCRA hazard categories listed; the new categories are the OSHA hazard classes and categories as on SDS Section 2.
- 2024 OSHA changes affecting EPCRA: Aerosols and Chemicals Under Pressure replace Flammable Aerosols; Desensitized Explosives added; pyrophoric and chemically unstable gases within Flammable Gases; pyrophoric gases removed from the hazardous-chemical definition. Twelve OSHA categories do not fit a 2017–2026 category.
- OSHA SDS update deadlines cited: 19 May 2026 for substances, 19 November 2027 for mixtures (29 CFR 1910.1200(j)).
- Earlier direct final rule (90 FR 51187, 17 Nov 2025) withdrawn on 9 Jan 2026 (91 FR 918) after adverse comment.

## 4. EPA guidance pages and instructions

https://www.epa.gov/epcra/hazardous-chemical-inventory-reporting — thresholds as in 370.10; annual inventory by 1 March; check state requirements.

https://www.epa.gov/epcra/tier-ii-forms-and-instructions — page last updated 22 June 2026. States may add chemicals, set lower thresholds and use their own form. 2017–2026 Tier II form for calendar year 2026, report due 1 March 2027; 2027 Tier II form for calendar year 2027 onward, report due 1 March 2028.

https://www.epa.gov/sites/default/files/2017-06/documents/tier_ii_inventory_form_instructions_2017.pdf — Tier II instructions v.17. Average daily amount = total of all daily weights ÷ number of days present on site; report weights in pounds, converting volume with a density factor; "identical to last year" boxes for page 1 and each chemical, with every data element still completed; a state may require exact amounts.

https://www.epa.gov/system/files/documents/2026-05/tier-ii-form-instructions_2027_may-2026.pdf — 2027 Tier II Regulatory Overview and Instructions, May 2026. Pounds = density (lb/gal) × gallons; density = specific gravity × 8.34 lb/gal; mixture and EHS aggregation as in 370.14; hazard section uses the OSHA classes and categories from SDS Section 2.

https://www.epa.gov/epcra/tier2-submit-software — current version Tier2 Submit 2025 "rev 1" for reporting year 2025; used only to confirm that software follows the reporting year. Not used in the skills.

## 5. EPA List of Lists (EHS and TPQs)

https://www.epa.gov/epcra/consolidated-list-lists — April 2025 version; Excel file https://www.epa.gov/system/files/documents/2025-04/microsoft-excel-version-of-the-comprehensive-list-of-lists-updated-april-2025.xlsx and PDF https://www.epa.gov/system/files/documents/2025-04/consolidated-list-of-lists-updated-april-2025.pdf. Column "EPCRA 302 EHS TPQ" read from the Excel file:
sulfuric acid 7664-93-9: 1,000; nitric acid 7697-37-2: 1,000; hydrogen peroxide (Conc.> 52%) 7722-84-1: 1,000; ammonia and ammonia (anhydrous) 7664-41-7: 500; formaldehyde and formaldehyde (solution) 50-00-0: 500; sulfur dioxide 7446-09-5: 500; hydrogen chloride (anhydrous; gas only) 7647-01-0: 500; chlorine 7782-50-5: 100; hydrofluoric acid / hydrogen fluoride 7664-39-3: 100; phenol 108-95-2: 500/10,000. No EHS TPQ: methanol 67-56-1, sodium hydroxide 1310-73-2, sodium hypochlorite 7681-52-9, hydrochloric acid 7647-01-0 (solution entries), propane 74-98-6.
The PDF introduction restates the solid-TPQ rule and says the 0.2 and 0.3 factors are not used for the twelve reactive solids marked "a" in part 355.

## 6. Lead-acid batteries

https://www.epa.gov/sites/default/files/2013-08/documents/revised-lead-acid-memorandum.pdf — EPA Office of Emergency Management memorandum "Lead Acid Battery Reporting Under EPCRA Sections 311 and 312 – Revised" (undated in the scan; hosted 2013; cites the pre-2008 section numbers 370.20 and 370.28, now 370.10 and 370.14). Sulfuric acid in all lead-acid batteries is added with other sulfuric acid toward the 500 lb EHS threshold; non-EHS chemicals such as lead need not be added; the batteries may be reported as a mixture naming sulfuric acid or sulfuric acid may be listed separately.

## 7. Units and identifiers

https://www.nist.gov/pml/special-publication-811/nist-guide-si-appendix-b-conversion-factors/nist-guide-si-appendix-b8 — NIST SP 811 Appendix B.8: pound (avoirdupois) → kilogram 0.4535924 (footnote: exact 0.45359237); gallon (US) → litre 3.785412.

https://www.cas.org/training/documentation/chemical-substances/checkdig — CAS describes the check-digit calculation (worked example 107-07-3 shown as an image). The method used in the skills (digits except the last, weighted 1, 2, 3 … from the right, sum mod 10) was confirmed on all 1,876 CAS numbers in the List of Lists Excel file: every one passes.

## Rules of thumb of this plugin (no external source)

- For non-EHS mixtures, upper-bound screening is the default when only a concentration range is supplied; replace it with an exact supplier weight percentage when available. Show both endpoints when they change a threshold or code.
- With counts and receipts but no usage dates, the highest possible amount between two counts is the earlier count plus all receipts before the next count, reported as an upper bound.
- Names that differ by one character, grade or concentration are never linked automatically.
- A failing CAS check digit is treated as a typing error to query, not as a different chemical.
- Densities, concentrations and EHS status are never filled from memory except the TPQ table embedded in the skills.

## 8. EPA concentration-range guidance

https://www.epa.gov/epcra/reporting-ehs-mixture-based-concentration-range — opened 2026-10-13; updated 14 April 2026. For an EHS mixture with component concentration ranges, use the upper-bound concentration to determine each component weight for EPCRA sections 302, 304 and 311/312 reporting.

## 9. Presence duration and inventory-system peaks

https://www.epa.gov/epcra/there-time-period-constitutes-present-facility — EPA FAQ, updated 14 April 2026; checked 2026-10-13. No minimum time period: a substance present at any one time during the year above the threshold is reportable.

https://helpcenter.agvance.net/home/maximum-average-daily-inventory-report — Agvance Maximum and Average Daily Inventory report, modified 12 November 2024; checked 2026-10-13. Max Lbs comes from end-of-day weights, so a product received and removed the same day can show zero; late entry of receipts, delivery, blend tickets and invoices makes the report inaccurate; a wrong Product Unit Weight (gallon-to-pound setup) makes Max Lbs wrong. Vendor-specific; not generalized to every inventory system.

## 10. EPA transition guidance for the 2024 OSHA hazard classes

https://www.epa.gov/epcra/epcra-hazardous-chemical-inventory-reporting-revisions-hazard-categories-and-reporting — updated 12 August 2026; checked 2026-10-13.
- Reporting years 2024–2026: Aerosols 1–3, Chemicals Under Pressure 1–3, chemically unstable Flammable Gases 1A/A and 1A/B and Desensitized Explosives 1–4 are reported as Hazard Not Otherwise Classified; Flammable Gases – Pyrophoric Gas – 1A as Pyrophoric Gas.
- A revised SDS received during 2026: the facility may use the SDS it already had for the 2026 annual report (due 1 March 2027); the 2027 report (due 1 March 2028) should use the revised SDS where available.
- SDS Section 2(c) downstream hazards: EPA has no policy on reporting them; check with the state. Interim recommendation: report them if reasonably anticipated to occur at the facility (a warehouse storing epoxy components would not, an epoxy-table maker would).

## 11. OSHA trade-secret concentration ranges

https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.1200 — 29 CFR 1910.1200(i)(1)(iv)–(vi), as amended 20 May 2024; current text checked 2026-10-13. A concentration withheld as a trade secret is given as a prescribed range (0.1–1, 0.5–1.5, 1–5, 3–7, 5–10, 7–13, 10–30, 15–40, 30–60, 45–70, 60–80, 65–85, 80–100%); the narrowest possible range must be used; two consecutive ranges may be combined when the exact range lies within 0.1–30% and fits no single range among the first seven; a narrower range is allowed.

## 12. Range code 13 lower boundary

https://www.epa.gov/sites/default/files/2017-06/documents/tier_ii_inventory_form_instructions_2017.pdf — Tier II instructions v.17 (2017), Table 2; checked 2026-10-13: code 12 is 1,000,000–9,999,999 lb; code 13 starts at 10,000,000 lb.
