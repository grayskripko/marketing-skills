# Official sources

All sources were read on 2026-10-12 while the package was built. The skills make no network requests; the rules below are embedded in the SKILL.md files.

The eCFR section pages refuse automated readers and send them to an access-request page. The same section text was read through eCFR's official versioner API for Title 40, which reported "up to date as of 2026-10-08". Each entry lists the page URL a person opens and the API URL that returned the text (HTTP 200).

Scope: these rules are for NSPS subpart VVa (40 CFR 60.480a–60.489a) and refinery units that apply VVa through subpart GGGa. They are not general LDAR rules. Permits, consent decrees, state rules, Part 63 programs and subpart VVb can set different thresholds, deadlines and records.

## 1. Applicability of subpart VVa — 40 CFR 60.480a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.480a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.480a
- Read 2026-10-12. Clause (a)–(b): applies to SOCMI process units (all equipment in a process unit is one affected facility) that commence construction, reconstruction or modification after November 7, 2006, and on or before April 25, 2023. Clause (d): exemptions (under 1,000 Mg/yr design capacity, heavy-liquid-only, beverage alcohol, no equipment in VOC service) need the records in 60.486a(i).
- Used in: every skill, applicability check.

## 2. Subpart VVb applicability and valve leak definition — 40 CFR 60.480b, 60.482-7b

- Pages: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVb/section-60.480b and https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVb/section-60.482-7b
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.480b and https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.482-7b
- Read 2026-10-12. 60.480b(b): units that commence construction, reconstruction or modification after April 25, 2023 fall under VVb. 60.482-7b(b): a valve leak under VVb is 100 ppm or greater, not 500 ppm.
- Used in: applicability check (a VVb unit is out of this profile; never apply 500 ppm to it).

## 3. Refinery units — 40 CFR 60.592a (subpart GGGa)

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-GGGa/section-60.592a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.592a
- Read 2026-10-12. (a): GGGa units comply with 60.482-1a to 60.482-10a. (b): for valves a unit may instead elect 60.483-1a, 60.483-2a, or the Phase III provisions of 40 CFR 63.168. (d)–(e): 60.485a, 60.486a and 60.487a apply, except as 60.593a provides.
- Used in: applicability check (a GGGa unit that elected 63.168 is outside this profile).

## 4. VVa valve standard — 40 CFR 60.482-7a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.482-7a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.482-7a
- Read 2026-10-12.
  - (a)(1): valves in gas/vapor or light liquid service are monitored monthly by 60.485a(b) methods, except as (f), (g), (h), 60.482-1a(c) and (f), 60.483-1a and 60.483-2a provide.
  - (a)(2): a valve that begins service after initial startup is first monitored within 30 days after the end of its startup period; under a 60.483-1a/-2a program it counts as leaking in the percent calculation, and if fewer than 2.0 percent are leaking it is first monitored at the next scheduled event or within 90 days, whichever comes first. A valve that replaces a leaking valve is excluded from (a)(2).
  - (b): an instrument reading of 500 ppm or greater is a leak.
  - (c)(1)(i): a valve with no leak for 2 successive months may be monitored in the first month of every quarter, beginning with the next quarter, until a leak is detected. (c)(1)(ii): the unit may be split into two or three subgroups monitored in different months, each every 3 months, with records of subgroup assignment. (c)(2): after a leak, monitor monthly until no leak for 2 successive months.
  - (d)(1): repair as soon as practicable, no later than 15 calendar days after detection, except as 60.482-9a provides. (d)(2): first attempt no later than 5 calendar days after detection.
  - (e): first attempts include, where practicable, tightening bonnet bolts, replacing bonnet bolts, tightening packing gland nuts, injecting lubricant into lubricated packing.
  - (f): no-detectable-emissions valves (no external actuating mechanism in contact with process fluid; under 500 ppm above background by 60.485a(c)); tested on designation, annually and on request.
  - (g): unsafe-to-monitor valves need a demonstration of immediate danger and a written plan to monitor as frequently as practicable during safe-to-monitor times.
  - (h): difficult-to-monitor valves need more than 2 meters elevation above a support surface, a qualifying unit (constructed on or before January 5, 1981, or under 3.0 percent of valves so designated) and a written plan for at least yearly monitoring.

## 5. Delay of repair — 40 CFR 60.482-9a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.482-9a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.482-9a
- Read 2026-10-12.
  - (a): allowed if repair within 15 days is technically infeasible without a process unit shutdown; repair before the end of the next process unit shutdown; monitoring to verify repair within 15 days after startup.
  - (b): allowed for equipment isolated from the process that does not remain in VOC service.
  - (c): for valves, allowed if purged-material emissions from immediate repair exceed the fugitive emissions likely from delay, and purged material is collected and destroyed or recovered in a 60.482-10a control device when repair is done.
  - (e): beyond a shutdown only if valve assembly replacement is needed, supplies are depleted and had been sufficiently stocked; not beyond the next shutdown unless it occurs sooner than 6 months after the first.
  - (f): a delayed valve that remains in service may be treated as repaired after two consecutive monthly readings below the leak definition.

## 6. Definitions — 40 CFR 60.481a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.481a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.481a
- Read 2026-10-12.
  - Repaired: adjusted or altered to eliminate a leak and re-monitored by 60.485a(b) to verify emissions are below the leak definition.
  - First attempt at repair: action to stop or reduce leaks of organic material using best practices.
  - Process unit shutdown: excludes an unscheduled stop under 24 hours; an unscheduled stop shorter than clearing and restarting would take and producing more emissions than delay; use of spare equipment or bypassing without stopping production.
  - Initial calibration value: concentration measured at the start-of-day calibration, or at the most recent recalibration after a drift assessment.
  - In VOC service: at least 10 percent VOC by weight. In light liquid service: conditions in 60.485a(e). In gas/vapor service: gaseous at operating conditions.
  - Quarter: a 3-month period; the first ends on the last day of the last full month within 180 days after initial startup.

## 7. Test methods — 40 CFR 60.485a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.485a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.485a
- Read 2026-10-12. Amended 89 FR 43070, May 16, 2024.
  - (b)(1): Method 21; calibrate before use each day; zero air under 10 ppm hydrocarbon; methane or n-hexane in air at no more than 2,000 ppm above the leak definition. Multi-scale instruments: lower scale with gas no higher than 2,000 ppm above the leak definition, highest scale with about 10,000 ppm; unused scales need no calibration that day.
  - (b)(2): drift assessment at least at the end of each monitoring day with the same calibration gas, without adjusting the readout. Drift % = (post-test response − initial calibration response) / calibration gas value × 100. (i) Negative drift over 10 percent: re-monitor all equipment read since the last calibration with readings between the leak definition and leak definition × (100 − drift%)/100. (ii) Positive drift over 10 percent: equipment read above the leak definition and below leak definition × (100 + drift%)/100 may be re-monitored at the operator's discretion.
  - (c): no-detectable-emissions tests use the difference between maximum reading and background against 500 ppm.
  - (e): light liquid service = a component with vapor pressure above 0.3 kPa at 20 °C, those components at 20 percent by weight or more, and liquid at operating conditions.
  - (h): %VL = VL / VT × 100. VT counts difficult- and unsafe-to-monitor valves only in the period they are monitored. VL includes valves with delayed repair. A new valve not monitored within 30 days of being placed in service counts in VL and VT for that period. Subgroups are summed. VT excludes readings taken to verify repair.

## 8. Recordkeeping — 40 CFR 60.486a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.486a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.486a
- Read 2026-10-12. Amended 89 FR 43071, May 16, 2024.
  - (a)(3): each monitoring event records instrument ID, operator ID, equipment ID, date and instrument reading.
  - (b): a weatherproof, readily visible identification with the equipment ID goes on leaking equipment; on a valve it may come off after 2 successive months with no leak.
  - (c): leak log kept 2 years: instrument, operator and equipment IDs; detection date and each repair attempt date; repair methods per attempt; maximum Method 21 reading at successful repair or when found nonrepairable; "Repair delayed" and reason if not repaired within 15 calendar days; signature of the owner or operator (or designate) who decided repair needs a shutdown; expected repair date if not repaired within 15 days; shutdown dates while unrepaired; date of successful repair.
  - (e)(8): calibration records: date and operator initials; cylinder ID, certification date and certified concentration; scales used; corrective action if the readout could not be adjusted; each drift assessment result (end-of-day reading and percent difference); procedure for self-made calibration gas.
  - (f): unsafe- and difficult-to-monitor lists with explanation and monitoring plan or schedule. (g): skip-period programs record the schedule and percent leaking per period.

## 9. Skip-period alternative for valves — 40 CFR 60.483-2a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.483-2a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.483-2a
- Read 2026-10-12. Start under 60.482-7a. After 2 consecutive quarterly periods at or below 2.0 percent leaking, skip 1 of the quarterly periods; after 5 consecutive, skip 3. Above 2.0 percent, return to 60.482-7a. Notify before implementing (60.487a(d): 90 days before). Record percent leaking per period. New valves must first go through 60.482-7a(a)(2).

## 10. General standards — 40 CFR 60.482-1a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.482-1a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.482-1a
- Read 2026-10-12. (a) compliance within 180 days of initial startup. (d) vacuum service and (e) under-300 hr/yr VOC service exclusions need the 60.486a(e) lists. (f) dedicated batch units operating under 365 days a year may use the operating-time frequency table, with minimum spacing of 30, 60, 90 and 120 days for quarterly, semiannual, three-quarter and annual monitoring.

## 11. Reporting — 40 CFR 60.487a

- Page: https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-60/subpart-VVa/section-60.487a
- API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&section=60.487a
- Read 2026-10-12. (c): semiannual reports give, per month, valves found leaking and valves not repaired as required by 60.482-7a(d)(1), the facts explaining each delay of repair and why a shutdown was technically infeasible, and shutdown dates in the period. (d): 90-day notice before electing 60.483-1a or 60.483-2a.

## 12. EPA Method 21 — 40 CFR part 60, appendix A-7

- EPA copy (dated 8/3/2017, states it is not the official version): https://www.epa.gov/sites/default/files/2017-08/documents/method_21.pdf
- Official text API: https://www.ecfr.gov/api/versioner/v1/full/2026-10-08/title-40.xml?part=60&appendix=Appendix%20A-7%20to%20Part%2060
- Read 2026-10-12; the clauses below match in both.
  - 3.7: response time = time from a step change to 90 percent of the final reading.
  - 6.3: meter readable to ±2.5 percent of the leak definition.
  - 7.2: cylinder gases certified within 2 percent with a shelf life; reanalyze or replace at its end. 7.3: self-made gases within 2 percent, replaced each day of use unless stability is shown.
  - 8.1.1: response factor for each compound before the analyzer goes into service; must be under 10 unless the rule says otherwise; published factors may be referenced.
  - 8.1.2: calibration precision before service and at 3-month intervals or the next use, whichever is later; three alternating zero/calibration readings; average algebraic difference / known value × 100 must be 10 percent or less.
  - 8.1.3: response time before service and after any change to the sample pump or flow configuration; average of three; 30 seconds or less.
  - 8.3.1: probe at the leak interface; find the maximum reading and hold about two times the response time. 8.3.1.1 valves: stem/packing gland interface around the stem, packing gland take-up flange seat, and all housing interfaces of multipart valves.
  - 10.1: daily calibration adjusts the readout to the calibration gas; if it cannot be adjusted, the analyzer is malfunctioning and needs corrective action before use.

## 13. EPA, Leak Detection and Repair: A Best Practices Guide (October 2007)

- URL: https://www.epa.gov/sites/default/files/2014-02/documents/ldarguide.pdf
- Read 2026-10-12. Guidance, not a rule. Section 6 lists compliance problems found by inspectors: components missing from inventory; reported monitoring rates that are not credible (a data-logger showing about one valve per second; 8,000 components by one person in a day); probe moved too fast or not held at the maximum for twice the response time; probe held away from the interface (a Bay Area district study found only 43 percent of valves leaking above 500 ppm when measured 1 cm away); instrument not meeting Method 21 section 6, dirty or leaking probes, wrong gases, no daily calibration; components wrongly designated unsafe or difficult to monitor; components put on delay of repair without considering in-service methods such as drill-and-tap. It gives about 500–700 valves per day for a two-person team and typical analyzer response times of 2–4 seconds.
- Used in: calibration check (monitoring-rate screen, labelled as an EPA guide observation, not a limit) and delay-of-repair review.

## This package's own conventions (not from a source)

- Deadline arithmetic: deadline = detection date + 5 (or 15) calendar days, inclusive of the deadline date. The rule says "no later than 5/15 calendar days after"; it does not spell out the counting. If the site's written program counts differently, the site's convention is used and stated.
- A field missing from an export is "not supplied", never "not done".
