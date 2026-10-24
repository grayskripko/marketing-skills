# Official source register

All entries read 2026-10-11. Scope: NIH recipient SF425 expenditure drafting from supplied award records and PMS exports. For reference maintenance outside a drafting task, check newer official policies against the award terms. During drafting, use supplied newer policy excerpts to identify conflicts; do not fetch remote sources. These notes paraphrase deciding rules rather than reproduce manuals.

## GSA form identity and field definitions

- URL: https://www.gsa.gov/reference/forms/federal-financial-report
- Download: https://www.gsa.gov/system/files/SF425_3_0-V30b.pdf
- Status: landing page loaded; PDF fetched HTTP 200 and embedded XFA template/instructions read. Ordinary PDF text extraction returns only a viewer notice. GSA lists revision 06/2010 and page update November 14, 2022. The posted template displays OMB 4040-0014 and expiration February 28, 2025; use NIH's posted-form continuation instruction below when considering that printed date.
- Scope: generic single-award form, not NIH deadline authority. NIH-specific policies supersede its generic final 90-day instruction and interim quarter-end coverage rule.

Field decisions from the embedded instructions:

| Fields | Rule that changes mapping |
|---|---|
| 1–5 | Agency/award and recipient identity; 4a is UEI, 4b EIN. Recipient internal account is for recipient use. Never make up a missing identifier. |
| 6–9 | Report type, cash/accrual basis and project dates must match supplied records. Generic form quarter-end interim dates are modified by NIH's budget-period reporting coverage. |
| 10 | Use cumulative values through the applicable reporting cutoff. A period-only export requires prior compatible cumulative balances. |
| 10a–10c | Generic cash receipts/disbursements and their difference. For NIH, use PMS-prepopulated data under NOT-OD-22-099 instead of rebuilding cash fields. |
| 10d | Authorized Federal funds as of reporting end, not future award commitments. |
| 10e | Cash: paid direct charges, indirect charged, subrecipient advances/payments. Accrual: paid direct charges, incurred indirect and net change in amounts owed for received property or performed services. Remove credits/refunds and deduction-method program-income expenditures. |
| 10f | Cash: incurred unpaid obligations. Accrual: incurred obligations not yet recorded as expenditure. No overlap with 10e or unincurred future commitments. |
| 10g/10h | Federal total = expenditures + obligations; unobligated balance = authorization − Federal total. |
| 10i–10k | Required contribution excludes voluntary excess; eligible actual contribution may include allowable in-kind support. Remaining contribution is required minus actual, floored at zero. Final actual contribution should meet or exceed required contribution. |
| 10l–10o | Program income used as recipient share is excluded from 10l to avoid duplication. 10m is deduction spending; 10n addition spending. Remaining income = earned − spent. The template validates deduction and addition as mutually exclusive. |
| 11 | Rate type, percent, effective period, base, charged amount and Federal share. Charged = rate × base; totals by column. Do not substitute booked overhead for rate/base evidence. |
| 12–14 | Explain material issues in remarks; actual certification is the authorized official's action; 14 is agency use. |

The embedded 10e instructions contain an inconsistent parenthetical pointing deduction spending to 10o, while the field labels and 10m instructions place deduction spending in 10m and unspent income in 10o. Use the form's field labels and dedicated line instructions; do not repeat the stray parenthetical as a mapping rule.

## NIH form-directory page

- URL: https://www.grants.nih.gov/grants-process/write-application/forms-directory/federal-financial-report-ffr
- Status: loaded; last updated February 27, 2026. NIH says to continue using its posted form while approval renewal is reflected.
- Deciding rules: submit through PMS, reached directly or from eRA Commons; annual expenditure deadline is 90 days after the calendar quarter containing budget end; segment-final deadline is 120 days after segment end. Domestic SNAP is exempt from annual expenditure reports. It confirms cash prepopulation since April 1, 2022.
- Its linked supplemental DOC did not load through web retrieval. No rule here is claimed to have been verified from that DOC. Foreign SNAP wording is resolved using the more specific current GPS 16.7 below.

## Current NIH reporting policy

- URL: https://grants.nih.gov/grants/policy/nihgps/HTML5/section_8/8.4.1_reporting.htm
- Status: loaded; revision March 2026, superseding April 2024.
- Sections 8.4.1.2 and 8.4.1.5.1: NoA establishes SNAP and special frequency. Annual coverage is the budget period; deadline uses its calendar quarter + 90 days. SNAP cumulative segment report is due within 120 days, even if continuation is awarded. Reporting must include an authorized budget extension. NoA specifies more frequent requirements.
- Section 8.4.1.5.3: unobligated balance disposition follows award terms; absent automatic carryover, NIH may authorize spending or offset an award. A balance is not spending permission.
- Revision rules in 8.4.1.5.2 and final-revision language in 8.6.1 are not fully consistent; revision timeliness is outside these two skills. Do not generalize a revised-report deadline into an original-report deadline.

## Foreign SNAP and currency

- URL: https://grants.nih.gov/grants/policy/nihgps/HTML5/section_16/16.7_administrative_requirements.htm
- Status: loaded; March 2026 revision. Sections 16.7 and 16.7.5 explicitly require foreign SNAP expenditure data only at competitive-segment end; foreign non-SNAP reports annually.
- Foreign FFRs are in English and U.S. dollars. Use the exchange rate applicable when funds were drawn from PMS, with supplied drawdown evidence; do not use today's exchange rate. Missing conversion evidence is a missing input. Historical foreign issue-date exceptions are not in this current text.

## Cash-field change

- URL: https://grants.nih.gov/grants/guide/notice-files/NOT-OD-22-099.html
- Status: loaded; released March 25, 2022; effective April 1, 2022; still linked by the February 2026 NIH page.
- NIH/AHRQ recipients stopped completing 10a–10c and separate 30-day quarterly cash transaction reports. PMS uses real-time cash data and adjusts reported disbursements to drawdowns on non-closed type-P subaccounts. Expenditure reporting deadlines remain. Thus ledger accruals cannot supply editable replacement cash figures.

## Final reconciliation and removed workaround

- URL: https://grants.nih.gov/grants/guide/notice-files/NOT-OD-22-215.html
- Status: loaded; released September 21, 2022; effective October 1, 2022; still linked by the current NIH page.
- Final NIH FFR validation requires 10a = 10b = 10e and terminal 10f = 0. Final 10a/10b are non-editable. Incorrect drawdowns require PMS adjustments and its nightly refresh, not editing expenditures to fit. Routine final-to-interim conversion was rescinded.
- Continuing institutional training document segments with trainee obligations need the awarding grants official to arrange an interim conversion. Terminal training awards can request a performance extension; neither action is automatic.

## Final scope and closeout clock

- URL: https://grants.nih.gov/grants/policy/nihgps/HTML5/section_8/8.6.1_final_federal_financial_report.htm
- Status: loaded; March 2026 revision.
- Final FFR required on termination, transfer, or an award not extended by a new competitive segment. It covers the funded segment, states exact unobligated funds and has no unliquidated obligations. Federal expenditures must reconcile with PMS net cash disbursements.
- URL: https://grants.nih.gov/grants/guide/notice-files/NOT-OD-24-047.html
- Status: loaded; released December 21, 2023; reminder process updated January 2024.
- Original closeout reports are due within 120 calendar days after the period-of-performance end; overdue the next day. This supports calendar-day arithmetic rather than substituting the SF425 generic 90-day final text.

## PMS system data and failure meaning

- URL: https://pms.psc.gov/grant-recipients/ffr-updates.html
- Status: loaded in web reader and direct HTTP fetch; page does not state a revision date. Current access confirmed, not a fabricated effective date.
- Cash receipts reflect drawdowns, refunds and journal vouchers. Annual/final cash prepopulation can run through liquidation end, so its scope differs from the expenditure cutoff. Final cash fields are non-editable. By-budget-period annual documents can also be non-editable and require zero 10f; by-project-period annual treatment differs. Determine document structure before diagnosing an annual mismatch.
- Reconciliation submission failure means compare 10a/10b to 10e and check the correct document, drawdowns, refunds and refresh. It does not establish which source is wrong. PMS says updated corrections flow through nightly processing.
- Contacts: incorrect cash/authorization data → PMS help desk; NIH missing reports/lines 1–9 → eRA service desk; liquidation/reporting extensions → awarding grants official. Prepare a concise issue note from supplied evidence; do not send it or expose account credentials.

## eRA schedule and date conflict

- URL: https://www.era.nih.gov/erahelp/commons/FFR/ffr_intro.htm
- Status: loaded; help banner revised August 25, 2026.
- NIH annual table: Jan–Mar budget ends → June 30; Apr–Jun → September 30; Jul–Sep → December 31; Oct–Dec → March 31. It also repeats the 90-day policy statement and exempts multi-year-funded awards from routine annual reporting. HHS completion occurs in PMS; Commons provides initiation/viewing.
- Conflict: June 30, 2026 + 90 days = September 28, 2026, while the table lists September 30. Do not present September 30 as literal addition. Drafting convention (this package's rule of thumb): use the recorded official due date, or the published eRA table as the standard schedule when none is supplied; show literal arithmetic differences as a short note. No source here establishes that an earlier self-calculated date overrides the published or recorded schedule.

## Federal institution exception

- URL: https://grants.nih.gov/grants/policy/nihgps/HTML5/section_17/17.7_administrative_requirements.htm
- Status: loaded; March 2026 revision; section 17.7.4.
- Federal institutions submit annual expenditure FFRs regardless of SNAP. This is a current exception, not merely a historical caveat. Apply the standard annual schedule to a supplied budget end unless specific terms establish a different frequency/date.

## Electronic form fields and limits

- URL: https://www.era.nih.gov/erahelp/commons/FFR/FFRLongForm.htm
- Status: loaded; help banner revised August 25, 2026.
- Award identity, report type, project dates and reporting end are prepopulated; draft them from supplied records rather than suggesting edits. Cash editability statements here are general HHS guidance; NIH's specific cash notice/PMS document rules control the NIH draft. Recipient expenditure is actual, not proved zero by absence of a required match. PMS supports ten indirect-expense entries; additional entries go in remarks.

## Institutional training exception

- URL: https://grants.nih.gov/grants/policy/nihgps/HTML5/section_11/11.3.13_reporting_requirements.htm
- Status: loaded; March 2026 revision; section 11.3.13.5.
- Institutional NRSA annual reporting is required. Stipends/tuition are obligated for the full appointment from its initiating budget period; qualifying portions extending beyond that period, childcare and applicable indirect costs can be unliquidated obligations. Terminal final has none and is due within 120 days. This specific NIH rule must be considered before applying PMS's generic by-budget-period zero-obligation statement.

## Current indirect-cost policy change

- URL: https://grants.nih.gov/grants/guide/notice-files/NOT-OD-26-072.html
- Status: loaded; released April 20, 2026, after March GPS.
- Updated 2 CFR 200 MTDC and de minimis flexibilities are rescinded for NIH; 45 CFR 75 indirect-cost provisions continue. Do not automatically apply the newer generic 15% de minimis rate or enlarged subaward threshold; use the supplied applicable agreement/award evidence.

## Policy freshness

- URL: https://grants.nih.gov/policy-and-compliance/notice-of-policy-changes
- Status: loaded; selected policy list includes notices through October 5, 2026. It states later notices supersede GPS. Targeted searches for 2026 SF425/FFR changes were also checked; no replacement of the embedded cash or original-report timing rules was established. This selected list is not every notice.
## Drafting conventions

Trace rows, mark missing amounts rather than zeros, separate overlapping scopes, deliver first and omit empty checks. These are this package's rules of thumb for usable drafts, not agency requirements. The package reads supplied data and references with no network requests and performs no account mutation.

## Restructured active foreign-subaward projects

- Source: https://grants.nih.gov/grants/guide/notice-files/NOT-OD-25-130.html
- Released July 18, 2025; read 2026-10-11. Applies to the described restructuring option for projects active on or before May 1, 2025 and applications submitted before May 1, 2025. It is not a blanket change to every foreign SNAP award.
- For the renegotiated Type 3 structure, the primary and each foreign supplement have separate document numbers and annual FFRs. SNAP and automatic carryover are removed for both; within-budget-period rebudgeting between them is prohibited. Confirm amended NoAs before using an old SNAP designation or merging ledgers.
- Verified again on 2026-10-11: eRA FFR overview (revised August 25, 2026) retains the four published annual table dates and budget-period coverage; NOT-OD-26-072 (April 20, 2026) retains the MTDC/de minimis rescission. URLs are in the corresponding sections above.
