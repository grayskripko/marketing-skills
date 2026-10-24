# Official evidence register

Read 2026-10-11. Scope: US remittance interpretation; Medicare-specific procedure is labeled below. Summaries are selective decision notes, not a reproduced code table. All six URLs loaded in the live web reader on this date.

## X12 CARC and group-code usage
https://x12.org/codes/claim-adjustment-reason-codes

The displayed list date is 2025-11-01; maintenance status was reviewed 2026-08-01. These are different dates. Per-code effective dates control historical interpretation. Deciding passages: “About Claim Adjustment Group Codes,” entries 16, 18, 23, 45 and 96. CARC16 separates billing data errors from attachment requests and needs a qualifying remark. 18 normally uses OA with a workers-compensation exception; 23 uses OA only. 45 restricts groups and amount scope. 96 also requires a qualifying remark. Preserve these constraints before proposing a correction. Full descriptions and uncommon codes should be checked at the source for the user's actual case.

## X12 publication chronology
https://ecommerce.x12.org/code-updates

Latest visible listing: July 1, 2026; file corrected August 3, 2026 for N922's effective date. March 1, 2026 listing was updated March 5. November 1, 2025 listing includes CARC changes; July 2026 includes RARC changes. These entries describe update bundles, not replacement dates for every individual code. The update downloads require a subscription; this package uses the public listing and live public code pages. Reopen this listing and both code pages before the planned 2026-10-22 submission; today cannot establish future currency.

## X12 supplemental and informational remarks
https://x12.org/codes/remittance-advice-remark-codes

Displayed list date: 2026-07-01. Deciding passages: introductory distinction between supplemental remarks and Alert messages; entries M51, N922, N923, N924. M51 identifies a missing, incomplete or invalid procedure code (start 1997-01-01; modified 2004-12-02). N922 concerns missing primary-care-dentist information; its public entry starts 2026-03-01. N923 reports an MAO payment-responsibility determination without denial; N924 reports that such determination is still pending. Both start 2026-07-01. Preserve encounter-record context; do not turn those remarks into ordinary claim denials. Alerts convey processing information rather than explain a specific adjustment.

## CMS claim, service and provider levels
https://www.cms.gov/medicare/coding-billing/electronic-billing/health-care-payment-remittance-advice

Page last modified 2024-09-10. Deciding sections: Overview; itemized claim/line information; group-code responsibility; provider-level balance adjustments. An ERA/SPR can contain several claims. CO assigns provider responsibility; PR assigns patient responsibility. CMS says Medicare beneficiaries may be billed for an adjustment only with PR. That condition does not establish every balance is collectible. PLB commonly covers provider interest, recovery of earlier overpayments or incentives, rather than a specific claim denial. Separate these from line-level adjustments. The page is the Medicare payment/remittance overview, not a universal commercial appeal policy.

## CMS Original Medicare first-level redetermination
https://www.cms.gov/medicare/appeals-grievances/fee-for-service/first-level-appeal-redetermination-medicare-contractor

Page last modified 2026-03-10. Scope: Original Medicare Part A/B initial determinations. Deciding sections: Filing a request for a redetermination; appeal timing; note on minor errors/omissions. A request is due within 120 days of receipt of the initial determination. Receipt is presumed five days after the notice date unless contrary evidence exists. CMS-20027 or a written request can be used. Required written-request elements include beneficiary name, Medicare number, disputed items/services and dates, requester's name and reason for disagreement; use placeholders in drafts rather than collecting identifiers in chat. Submit supporting evidence with the request. Minor claim errors/omissions go through correction/reopening, not appeals. Confirm the relevant MAC's process. Do not use this deadline for initial claim filing, commercial plans, Medicaid or Medicare Advantage.

## Evidence worklist method

This package's working method: request the document that would prove or disprove the stated adjustment, name its relevant field/date, and connect it to a proposed next step. A clearinghouse acceptance alone does not establish payer receipt. This is an evidence-handling method, not a quoted X12 field rule or a new payer policy. Keep accepted/rejected/pending stages distinct. For timely filing collect service date, applicable filing policy, original payer receipt and acceptance history. For authorization collect the actual authorization scope and submitted fields. For coverage disputes collect the applicable dated policy and existing supporting records; never create clinical evidence.

## CMS Original Medicare timely filing and appeal eligibility
https://www.cms.gov/regulations-and-guidance/guidance/manuals/downloads/clm104c01.pdf

Read 2026-10-11. Chapter 1 current cover revision 13725, issued 2026-04-10. Sections 70.4 and 70.6 carry revision 12909, issued 2024-10-24, effective 2024-11-26. Section 70.4 excludes provider/supplier untimely-filing denials from appealable initial determinations. Section 70.6 preserves usual beneficiary appeal rights when disputing untimeliness or responsibility; provider/supplier protests have no formal appeal channel, but the contractor may informally review on request. Identify whose finding is disputed before selecting a route. Original Medicare generally uses one calendar year from service, with institutional span-date rules; do not derive a case deadline without the service dates and applicable exception facts. Section 70.6 addresses late claims and challenges to a finding that filing was late; request actual MAC receipt/filing evidence and the MAC review process. The general 120-day redetermination period does not create a formal provider/supplier appeal entitlement for this filing protest; preserve the beneficiary branch above. Verify applicable exception criteria rather than treating every claimed delay as an exception.

## Additional encounter and processing decisions — checked 2026-10-11

https://x12.org/codes/remittance-advice-remark-codes

N925 and N926 start 2026-07-01. They distinguish no MAO payment responsibility from partial absence of responsibility at encounter submission. The latter does not mean every line was denied. N938 starts 2026-07-01 and is an Alert instructing against resubmission because automatic reprocessing will occur. Its processing instruction matters but does not supply CARC16’s required non-Alert explanation. Verify subsequent status before claiming these historical rows describe the present.
