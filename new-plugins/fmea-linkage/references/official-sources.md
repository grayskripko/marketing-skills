# Sources for FMEA linkage rules

Every page below was opened and read on 2026-10-13. The package makes no network requests at run time; these notes were written when it was built. IATF 16949:2016, the AIAG & VDA FMEA Handbook, the Ford FMEA Handbook and the AIAG Control Plan manual are sold or restricted; their text was not opened and is not reproduced. Only the openly published IATF sanctioned interpretations and FAQs, the Ford customer-specific requirements and two public summaries (section 6) below are used. The customer's own requirements, as the user supplies them, decide every case.

## 1. Where current customer-specific requirements are published

https://www.iatfglobaloversight.org/oem-requirements/customer-specific-requirements/ — read 2026-10-13. IATF list of OEM customer-specific requirements. For Ford it links "Customer Specific Requirements for IATF 16949:2016 – Effective 15 June 2026" and "Customer Specific Requirements for PPAP – Effective 15 June 2026" (the two PDFs below). Other OEMs are listed on the same page; this plugin does not embed their requirements.

## 2. Ford Customer-Specific Requirements for PPAP, effective 15 June 2026

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2026/06/Ford-Specifics-for-PPAP_June-2026-SCCAF-_-Final.pdf — read 2026-10-13. 32 pages, © 2026 Ford Motor Company. Summarised, not copied:
- Cover: intended for programs using the SCCAF process.
- 2.2.4 and 2.2.6: DFMEAs and PFMEAs meet the Ford FMEA Handbook; the AIAG & VDA FMEA Handbook format is accepted. Suppliers also keep foundation FMEAs for the processes used to make the part.
- 2.2.5 Process Flow Diagram: no Ford customer-specific requirement.
- 2.2.6: build-to-print suppliers obtain DFMEA information (YC, YS) from Ford to develop the PFMEA and special characteristics (CC, SC, HI, OS) and document them on the SCCAF, including sub-tier control points. The control plan identifies the special controls that prevent shipment of any nonconformance to a Ford CC, wherever in the supply chain. Characteristic traceability is required from the DFMEA through the PFMEA to the control plan and to the process instructions, documented on the APQP/PPAP Evidence Workbook.
- 2.2.7: control plans follow the AIAG Control Plan Manual, latest edition (the record of revisions names the 1st edition, required by 31 December 2024). For a CC at a sub-tier level, the sub-tier and tier 1 control plans identify the controls that prevent shipment of nonconforming product. The control plan includes ongoing monitoring of capability, stability and control.
- 2.2.9: the annual dimensional layout requirement is included in the control plan.
- 2.2.11.1: the special characteristics on the SCCAF must be traceable to the special-characteristic controls in the control plan.
- 3.1 Customer Notification (printed p.26): organizations contracted by Ford obtain approval through the Ford SREA process before implementing any organization-initiated or sub-tier-supplier-initiated change. Rechecked 2026-10-13.
- Record of revisions, June 2026: PFMEA and control plan approval requirements updated.

## 3. Ford Customer-Specific Requirements for IATF 16949:2016, effective 15 June 2026

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2026/06/Ford-IATF-CSR_Jun-2026-SCCAF_Final.pdf — read 2026-10-13. 44 pages, © 2026 Ford Motor Company. Summarised:
- Cover: intended for programs using the SCCAF process.
- 3.8, 3.9, 3.13: definitions of families of FMEAs, families of control plans and foundation FMEAs (generic FMEAs per process type).
- 8.2.3.1.2: CC symbol is the inverted delta ∇; SC, HI and OS have no Ford symbol; internal symbols allowed for internal use; fastener base part numbers beginning W9 are treated as inverted delta.
- 8.3.2.1: all PFMEAs and control plans need Ford Product Development Engineering approval regardless of PPAP level, plus STA approval for levels 3 and 5 or inverted-delta parts; revisions after initial approval also need approval; approval may be an email, electronic or physical signature; approval does not move responsibility for accuracy and completeness away from the organization. Family PFMEAs need STA approval before use. Foundation FMEAs are required; knowledge from problem solving (8D, Six Sigma, Shainin and similar) is documented in both the part and the foundation FMEAs; part and foundation FMEAs stay aligned in both directions; FMEAs are aligned to the control plans and work instructions or visual aids; FMEA software ensures alignment of foundation FMEA, part FMEA and control plan (bulk-material suppliers exempt). Reverse FMEA events for new launches. Special characteristics and control approach traceable from the DFMEA through the PFMEA and the SCCAF to the control plan, recorded in the APQP/PPAP Evidence Workbook. Revisions to inspection frequencies in control plans and PFMEAs need Ford approval through an SREA. Pre-launch or safe-launch control plan used from the launch milestone written as <TT> until <OKTB> before moving to the production control plan. Note (printed p.25, rechecked 2026-10-13): a Priority Supplier agrees safe-launch exit criteria upfront for extraordinary controls beyond <OKTB>; it should show at least 4 weeks of clean production at required jobs per hour without customer quality claims, with final inspection evidence available to the site STA engineer; any concern during safe launch extends it by 2 weeks after permanent corrective action.
- 8.5.1.1 Control plan: no Ford customer-specific requirement.
- 8.5.1.2: operators use the most current work instructions; work instructions contain reaction plans for nonconformances showing the specific required steps.
- 8.6.2: annual layout covers all dimensional requirements with at least 5 parts overall and at least one per cavity, tool or center where applicable; measurements are recorded in the APQP/PPAP Evidence Workbook. Rechecked 2026-10-13 for the control-plan completeness correction.
- 9.1.1.2: ongoing process capability Ppk > 1.33, included in the production control plan.
- Table A (printed p.36, referenced from 9.1.1.1 and 9.1.1.2; rechecked 2026-10-13): in control with Ppk ≥ 1.33, accept product; in control with Ppk < 1.33, 100% inspect; gone out of control (either Ppk band), identify the special cause and 100% inspect all product since the last in-control sample. The 100% inspection must prevent shipment of nonconforming product, typically by error proofing. SPC on product characteristics without continuous manufacturing process controls is not appropriate or sufficient for CCs.

## 4. IATF 16949:2016 Sanctioned Interpretations, November 2025 edition

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2025/11/IATF-16949-SIs-Nov-2025.pdf — read 2026-10-13 (linked from https://www.iatfglobaloversight.org/iatf-169492016/iatf-169492016-sis/). A sanctioned interpretation changes the interpretation of a requirement and can be the basis for a nonconformity.
- SI 6 (8.3.3.3, issued October 2017): special characteristics are documented in drawings (as required), risk analysis such as the PFMEA, control plans and standard work or operator instructions, identified with specific markings and cascaded through each of these documents.
- SI 11 (8.5.6.1.1): not every primary process control needs a back-up or alternate method; where they exist, they are on the organization's list of process controls.
- SI 20 (10.2.3, issued December 2020): problem solving includes reviewing and, where necessary, updating documented information such as the PFMEA and control plan.
- SI 24 (Annex A.1 Note 3, issued May 2022): for highly automated processes where the control method is held by a system such as an MES, summary control information with direct reference or linkage to that system is acceptable.
- SI 25 (Annex A.2, issued May 2022): minimum control plan content includes control plan number, issue and revision date, part numbers or a common control plan designation, engineering change level, phase covered, part or process step number and process name or operation description.

## 5. IATF 16949:2016 Frequently Asked Questions, June 2026 edition

https://www.iatfglobaloversight.org/wp/wp-content/uploads/2026/06/IATF-16949-FAQs_June-2026.pdf — read 2026-10-13 (linked from https://www.iatfglobaloversight.org/iatf-169492016/iatf-169492016-faqs/). An FAQ explains an existing requirement.
- FAQ 17 (8.5.6.1.1): an alternate process control is not required for every primary control; where back-up or alternate controls are needed, both primary and alternate controls should be defined in the process flow, PFMEA, control plan and standardised work; uses of alternate controls are reviewed periodically as input to updating the process flow, FMEA and control plan.
- FAQ 21 (8.6.2): ongoing layout inspection and functional testing requirements are defined in the control plan, including any customer-specific ones.

## 6. Public explanations of the AIAG Control Plan manual and IATF 10.2.4 (secondary sources)

The licensed manual itself was not opened; these are the publishers' own summaries, not manual text.
- https://blog.aiag.org/core-tools-and-iatf-169492016-overview — AIAG, "Core Tools and IATF 16949:2016 Overview", 15 August 2018, read 2026-10-13. Under 10.2.4 Error-proofing: the control plan includes the test frequency of error-proofing devices, and records of those tests are kept.
- https://intertek-cdn.s3.amazonaws.com/www-intertek-com/media/other/webinars/2024/2024-04-09-WBN-NA-BA-Importance-of-APQP-CP-in-the-Automotive-Industry_EN.pdf — Intertek webinar slides, 9 April 2024, read 2026-10-13. Slide 23, manual 1.4: the method and frequency to confirm error-proofing effectiveness are defined on control plans. Slide 24, manual 1.8: reaction plans define specific actions, the individual responsible for taking action and the responsible owner of the action.

## Rules of thumb of this plugin (no external source)

- Rows are matched by operation number and characteristic number, applying any approved mapping the user supplies; names confirm a match but never create one. A one-character difference in a revision or part number is a mismatch, never a match.
- A flow step (including receiving, storage, transport, inspection, rework and repair, when the flow shows them) with no PFMEA rows is reported; a control plan row with no PFMEA row is a question, not a defect.
- A PFMEA detection or prevention control that the control plan does not run at the same operation is a conflict, because the PFMEA then relies on a control that is not in place.
- Control plans for different phases are compared separately.
- A change is carried to every row with the same characteristic or operation number, not only to the operation named in the change.
