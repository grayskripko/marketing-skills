# Sources for HAZOP action rules

Use only data the user supplies for the task, including attached files they identify, without scanning folders, memory or chat history.

Each page below was opened on 2026-10-13 and the passage summarised here was read in it. The package makes no network requests at run time; these notes were written when it was built. The rules apply to US processes covered by OSHA Process Safety Management (29 CFR 1910.119) or EPA Risk Management Program 3 (40 CFR 68 subpart D). For other processes the skills use the site procedure the user supplies.

## 1. OSHA 29 CFR 1910.119(e), (i)

https://www.osha.gov/laws-regs/regulations/standardnumber/1910/1910.119 — read 2026-10-13. Same text in the eCFR, https://www.ecfr.gov/current/title-29/subtitle-B/chapter-XVII/part-1910/subpart-H/section-1910.119 — read 2026-10-13 through the eCFR versioner API for the 2026-10-01 point in time (the browser URL returned a bot-check redirect to scripted clients).
- (e)(5): a system to promptly address the team's findings and recommendations; assure recommendations are resolved in a timely manner and the resolution is documented; document what actions are to be taken; complete actions as soon as possible; develop a written schedule of when actions are to be completed; communicate the actions to operating, maintenance and other employees whose work assignments are in the process and who may be affected.
- (e)(6): at least every five years after completion of the initial PHA, the PHA is updated and revalidated by a team meeting (e)(4).
- (e)(7): PHAs, updates and revalidations, and the documented resolution of recommendations under (e)(5), are retained for the life of the process.
- (i)(2)(iii): before highly hazardous chemicals are introduced, for new facilities a PHA has been performed and recommendations resolved or implemented before startup; modified facilities meet management of change, paragraph (l).

## 2. EPA 40 CFR 68.67 (Program 3 process hazard analysis)

https://www.ecfr.gov/current/title-40/chapter-I/subchapter-C/part-68/subpart-D/section-68.67 — read 2026-10-13 through the eCFR versioner API for 2026-10-01; latest amendment listed 2024-05-10 (text cites 89 FR 17688, Mar. 11, 2024).
- 68.67(e): same recommendation system wording as 1910.119(e)(5).
- 68.67(f): update and revalidate at least every five years after completion of the initial PHA; revalidations done for 1910.119(e) are acceptable. This paragraph does not state the OSHA shutdown treatment in QE-03; do not apply that guidance as an EPA deadline extension.
- 68.67(g): retain PHAs, updates or revalidations and the documented resolution of recommendations for the life of the process.
- The 2024 amendments added PHA content items in (c)(8)–(10) and safer-technology implementation in (h). The skills do not judge PHA content, so these are not used.

## 3. OSHA directive CPL 02-01-065, Process Safety Management of Highly Hazardous Chemicals

https://www.osha.gov/enforcement/directives/cpl-02-01-065 and https://www.osha.gov/sites/default/files/enforcement/directives/CPL_02-01-065.pdf — read 2026-10-13. Signature date 14 December 2023, effective 26 January 2024. Enforcement guidance, not a regulation.
- QE-01: an initial PHA must be completed with recommendations resolved or implemented before startup; when a PHA is updated and revalidated before the five-year deadline, the next one is due within five years of that latest revalidation.
- QE-03: the five-year requirement cannot be delayed or restarted during a shutdown; the maximum period depends on the completion date of the prior PHA (example: completed 1 January 2020, next due no later than 1 January 2025). No PHA is required while the process is shut down and de-inventoried, but if the period expires before restart, the revalidation is done before highly hazardous chemicals are reintroduced.
- QE-04: PHAs and revalidations are kept for the life of the process.
- QE-19: OSHA expects a schedule for corrective actions, documentation of actions to be taken and of their completion as they occur; quoting the 1992 preamble (57 FR 6356), most actions can be completed within one to two years; "unusual circumstances" items are those needing a shutdown, expected in the first regularly scheduled shutdown or turnaround of the process.
- QE-20: a recommendation is resolved when the employer adopts it, modifies it or justifiably declines it; a rejection or modification should be communicated to the PHA team. OSHA recommends declining in writing, based on adequate evidence, that one or more is true: material factual errors in the analysis; not necessary to protect the health and safety of the employer's own or contractors' employees; an alternative measure would provide a sufficient level of protection; the recommendation is infeasible. The document should be retained with the recorded PHA findings.
- QE-21: facility siting study recommendations need not be on the same PHA worksheet or recommendations log, but must be documented and resolved under (e)(5) and kept under (e)(7).
- Appendix A, item 1: a PHA may be required more often than five years when a modification is significant enough to require a change in process safety information.

## 4. Site procedures, tool records and case records (not US rules)

These show how real procedures and records behave. They are not legal duties; the skills use them only to read a supplied record correctly.

- INPEX, Hazard and Operability (HAZOP) Studies procedure, 0000-AH-PRC-70001 Rev 0, 27 Jan 2022, §9, pp. 29–30. https://www.inpex.com.au/media/asdn0dfc/0000-ah-prc-70001-hazard-and-operability-studies-rev-0.pdf — read 2026-10-13. Operational phase: a HAZOP recommendation counts as fully closed when the linked MOC, which records the recommendation, response and tracking details, has been endorsed and submitted for approval; if the approver rejects the MOC, the action closes only with sufficient approver justification, otherwise it is revisited. Project and brownfield-project phases use different criteria. Changes an answer: a transfer-to-MOC closure can be valid under the supplied procedure while the field change is still outstanding.
- ABB, HAZOP, LOPA, SIF Designer, ORD and SIF Performance User Manual, version 3.3, 3BNP102815-330 A, document release April 2026, Section 7 Recommendations & Observations, pp. 139–142. https://library.e.abb.com/public/379136d908034536901fa80b814948a7/3BNP102815-330_A_en%20HAZOP%20LOPA%20SIF%20Designer%2C%20ORD%20and%20SIF%20Performance%203.3%20User%20Manual.pdf — read 2026-10-13 (downloaded PDF, text extracted). Recommendations and Observations are separate tabs; Due Date and Status apply to Recommendations only; Ref Id is user-editable; one recommendation can be referenced by several hazardous events, causes or LOPAs, and an existing one can be linked to another open study; export and close-out sheet generation use the items selected by checkbox. Changes an answer: shared-object links, not matching text, settle identity; an Observation's blank due date is not a recommendation defect; a selected export does not prove the whole study is present.
- U.S. Chemical Safety Board, Bio-Lab Lake Charles recommendation 2020-05-I-LA-R2, issued 24 Apr 2023, status changed to Closed – Acceptable Action 6 Sep 2025. https://www.csb.gov/assets/recommendation/Status_Change_Summary_Bio-Lab_(Bio-Lab_R2)_C-AA.pdf — read 2026-10-13. The recommended PHA action system assigns each item to a person with a deadline for initial evaluation, keeps the rationale when an item is modified or rejected, and tracks every item until resolved; CSB closed it after reviewing the documentation Bio-Lab submitted. Changes an answer: an initial-evaluation deadline is a different milestone from an implementation date.
- IChemE Safety Centre, Effective revalidation of risk assessments: Delta HAZOP, Revision 2, November 2024, §7.1.2, p. 10. https://www.icheme.org/media/27204/effective-revalidation-of-risk-assessments-delta-hazop.pdf — read 2026-10-13. System boundaries and nodes should align with the previous HAZOP reports; guidewords do not need to be selected because a Delta HAZOP does not follow the guideword method. Changes an answer: carry-over matching uses the previous study's identifiers, and no new guidewords is not a gap.
- SPE-146192, "Learning the lessons – retrospective HAZOPs", SPE Offshore Europe, Aberdeen, 2011 (practitioner paper, published in the ABB library). https://library.e.abb.com/public/82ddae46619bd6b1852579580048cbe7/SPE%20SPE%20146192%20Learning%20the%20lessons%20-%20retrospective%20HAZOPs.pdf — read 2026-10-13. Recording software that extracts recommendations only loses the causes, consequences, section and guidewords needed to respond to and close the recommendation later. Changes an answer: when a recommendation's intent is unclear, the originating scenario is the record to ask for.

## Rules of this plugin (no external source)

- Identifier matching normalises only case, spaces, leading zeros and separators; a different node or number is never linked automatically.
- A closure record older than the recommendation is raised as a question, not as a finding.
