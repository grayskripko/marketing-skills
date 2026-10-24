# Sources for PPAP package rules

Every page below was opened and read on 2026-10-13. The package makes no network requests at run time; these notes were written when it was built. The AIAG PPAP manual (4th edition), the AIAG Service PPAP manual and IATF 16949 are sold under licence; their text was not opened and is not reproduced. Element names are used only as the labels people use for them. The customer's own requirements, as the user supplies them, decide every case.

## 1. Where the current customer-specific requirements are published

https://www.iatfglobaloversight.org/oem-requirements/customer-specific-requirements/ — read 2026-10-13. IATF list of OEM customer-specific requirements. For Ford it lists "Customer Specific Requirements for IATF 16949:2016 – Effective 15 June 2026" and "Customer Specific Requirements for PPAP – Effective 15 June 2026", linking to the two PDFs below. Other OEMs listed on the same page include General Motors (effective 30 October 2025), Stellantis (June 2025), Renault Group (April 2026) and IVECO Group (24 November 2025); this plugin does not embed their requirements.

## 2. Ford Customer-Specific Requirements for PPAP, effective 15 June 2026

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2026/06/Ford-Specifics-for-PPAP_June-2026-SCCAF-_-Final.pdf — read 2026-10-13. For use with AIAG PPAP 4th edition and Service PPAP 1st edition; for programs using the SCCAF process; 32 pages, © 2026 Ford Motor Company. Summarised, not copied:
- Applicability: PPAP is required for, among others, new tooled parts, design changes including running changes, changes in operating pattern, process changes after approval, added or modified tooling, and capacity above verified capacity.
- 2.2.1 Design record: released in Ford's design system; records aligned across release system, CAD, drawing and purchase order, with concurrence when the PO differs; software level and strategy number for parts with software; drawing notes need evidence of conformance; part-marking compliance screenshot and part photo, or approved exemption.
- 2.2.1.1 Material reporting: approved entry in the GMM dashboard with "PPAP Approve" = YES.
- 2.2.2 Change documents: a WERS Alert or a build deviation in Jira.
- 2.2.3 PV testing on Phase 0 parts; additional production streams need PV testing for Phase 2.
- 2.2.6 Traceability of characteristics from DFMEA through PFMEA to control plan and process instructions, in the APQP/PPAP Evidence Workbook; every PFMEA needs Ford Product Development approval, plus STA approval at submission levels 3 and 5 or for safety and regulatory (inverted-delta) components (printed p. 10); build-to-print suppliers document special characteristics on the SCCAF, including sub-tier control points; control plan identifies controls preventing shipment of nonconforming CC wherever in the supply chain.
- 2.2.7 Control plans: same approval rule as PFMEAs, Product Development always, STA also at levels 3 and 5 or inverted-delta components (printed p. 11); sub-tier and tier 1 control plans identify CC controls made at sub-tier level.
- 2.2.8 MSA before capability studies; gauge R&R by ANOVA; report % study variation and % tolerance and ±2 GRR standard deviations; < 10% of tolerance acceptable, 10–30% decided with the STA site engineer, > 30% unacceptable; minimum 10 parts × 3 operators × 3 trials (variable), 50 × 3 × 3 (attribute); kappa > 0.75, though with guard-banded gauge limits lower kappa may be acceptable when it comes from rejecting good parts, all out-of-specification parts still rejected (printed p. 13); attribute study parts should be 25% near or at each limit, 30% expected variation, 10% beyond each boundary group, "near" = ±5% of total tolerance centred on each limit (printed p. 14); one-sided formulas (6σ_GRR / (USL − 0) for one-sided geometric tolerance; 3σ_GRR / |limit − mean| otherwise).
- 2.2.9 Dimensional results: at least 5 parts, individual results for all Ford-specified dimensions, parts from every cavity, tool or stream.
- 2.2.11.1 Ppk on a stable data set of ≥ 25 subgroups of ≥ 5 (≥ 125 measurements) from consecutive parts spread over ≥ 300 parts, covering all tools, cavities, streams and shifts; until then 100% inspection or mistake-proofing; acceptance Ppk ≥ 1.67 (a note in the same section writes > 1.67); capability not required for OS characteristics; SPC without continuous process control is not sufficient for CC; supplier selects capability characteristics when Ford designated none. Note 1 (printed p. 17): remove special causes; data still not normal should be matched to the expected distribution (e.g. Weibull) before Ppk, with STA site engineer guidance.
- 2.2.11.3 Heat-treated parts: 30 parts in total for hardness or required properties, ≥ 9 for destructive tests; all readings inside a band at 90% of the tolerance, none at the limits; Rockwell to one decimal.
- 2.2.11.6 When criteria are not met: mistake-proofing or 100% inspection built into the process; visual or statistical methods not permitted; guard-band formulas for 100% gauges (worked example 600 ± 40 µm, 20% GRR → 568 to 632 µm).
- 2.2.12 Laboratory complies with ISO/IEC 17025 or national equivalent; accreditation not required.
- 2.2.13 Electronic AAR with every PSW for parts with appearance criteria.
- 2.2.18 Electronic PSW default; paper PSW exceptions SREA, directed tier 2, capacity uplift, bulk material; eCAR evidence for APPC and MPPC; approved sub-tier part approvals with each PSW phase; final Schedule A with the PSW for each new tooled end item; evidence that sub-tier CC controls are effective; family of parts on one PSW needs prior STA concurrence with every prefix, base and suffix noted; service part number in parentheses above the production part number.
- 5.2.2 Interim approval needs an approved engineering or build deviation (WERS Alert or Jira Deviation).
- Appendix H (printed p. 29, added June 2026): tier-1 suppliers of electronic commodities containing flashed software meet the Ford Software Industrialization Checklist, available through the Supplier Quality Hub (not opened: login).

## 3. Ford Customer-Specific Requirements for IATF 16949:2016, effective 15 June 2026

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2026/06/Ford-IATF-CSR_Jun-2026-SCCAF_Final.pdf — read 2026-10-13. 44 pages, © 2026 Ford Motor Company. Summarised:
- 7.5.3.2.1 Inspection and measurement records keep actual values; pass/fail alone is not acceptable for variable measurements; minimum 2 years. Final Schedule A kept for the life of the part plus one year.
- 8.2.3.1.2 Symbols: CC = inverted delta ∇; SC, HI and OS have no Ford symbol; internal symbols allowed for internal use; base part numbers beginning W9 (fasteners) treated as inverted delta.
- 8.3.2.1 Special characteristics traceable from DFMEA through PFMEA and SCCAF to control plan; build-to-print suppliers obtain YC/YS information from Ford; also applies to Ford-directed sub-tier suppliers without a multi-party agreement.
- 8.3.4.4 Sub-tier approvals may be evidenced by a summary (approved PSWs, a listing of approvals or equivalent); STA will not grant full PPAP approval while the part or process is under a WERS Alert or Jira Deviation.
- 8.6.2 Annual layout on at least 5 parts; with several cavities, tools or centres, at least one part from each, minimum 5 overall; 5 per cavity not required.
- 9.1.1.2 Ongoing process capability Ppk > 1.33.

## 4. Oshkosh Defense EITAN addendum to the Global Supplier Quality Manual, revision 1.3, July 2024

https://osn.oshkoshcorp.com/-/media/OSN/supplier-resources/standards-guide/2022/Defense/EITAN-Addendum71224.pdf — read 2026-10-13. Used only as a published reporting practice, not as a Ford rule. Summarised:
- §21 Dimensional results, best practice 2 (printed pp. 13–14): for true position, list basic x and y, feature size and position tolerance zone, and show MMC bonus tolerance as a separate line; the bonus can be added to the position zone when MMC applies.

## Rules of thumb of this plugin (no external source)

- A file listed in an index with no pasted content is "Indexed only", never complete.
- One-character differences in part numbers, suffixes or revision letters are mismatches, never matches.
- A value exactly on a limit is within the limit unless the user's specification says otherwise.
- Evidence dated before the current change level's date is questioned as possibly describing the previous design.
- Where Ford's text is ambiguous (Ppk exactly 1.67; where the 90% heat-treat band sits), the skills show the value and ask rather than decide.
