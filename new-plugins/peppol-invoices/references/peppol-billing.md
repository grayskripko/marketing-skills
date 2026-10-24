# Peppol Billing rejection reference

Scope: Peppol BIS Billing 3.0 UBL invoice and credit note, May 2026 release 3.0.21. Read 2026-10-11. This is a targeted rule register, not the complete validator. All linked pages below were retrieved successfully on that date. Do not apply these field paths to PINT, self-billing or CII without their own mapping. Recheck the release and mandatory date before diagnosing a later submission.

## Release and source register

- [Billing specification](https://docs.peppol.eu/poacc/billing/3.0/), read 2026-10-11: live page identifies May 2026.
- [Official mandatory-release table](https://peppol.org/documentation/technical-documentation/post-award-documentation/), read 2026-10-11: Billing publication 2026-05-20; mandatory 2026-08-17. The table lists PINT and self-billing separately.
- [Release notes](https://docs.peppol.eu/poacc/billing/3.0/release-notes/), read 2026-10-11: release 3.0.21; EN16931 artefacts 1.3.16 published 2026-04-10. Profile 02 adds billing with response and requires separate SMP registration. R004 rejects version syntax; Dutch R054–R057 are warnings; Danish R052/R053 and DK-R-017 are fatal. BR-CO-25 was removed: do not present an older due-date error as a current rule without checking the provider's artefact version.
- [Invoice syntax](https://docs.peppol.eu/poacc/billing/3.0/syntax/ubl-invoice/) and [credit-note syntax](https://docs.peppol.eu/poacc/billing/3.0/syntax/ubl-creditnote/), read 2026-10-11: cardinalities, ordering and UBL mapping. `cbc` and `cac` are namespace prefixes, not literal string requirements. Invoice namespace `urn:oasis:names:specification:ubl:schema:xsd:Invoice-2`; credit note `urn:oasis:names:specification:ubl:schema:xsd:CreditNote-2`.

## Required fields and exact error mapping

All rule links in this and later tables: read 2026-10-11, May 2026 release. A mandatory field must be populated meaningfully, not with a made-up placeholder. Full syntax may impose additional cardinalities and conditional fields.

| Rule | Meaning / UBL field / correction |
|---|---|
| [BR-01](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-01/) | Supply the specification identifier at root CustomizationID; Peppol imposes its format too. |
| [BR-02](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-02/) | Supply root ID (invoice number). |
| [BR-03](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-03/) | Supply root IssueDate. |
| [BR-04](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-04/) | Supply InvoiceTypeCode; credit notes use CreditNoteTypeCode. |
| [BR-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-05/) | Supply DocumentCurrencyCode. |
| [BR-06](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-06/) | Seller name: AccountingSupplierParty/Party/PartyLegalEntity/RegistrationName. |
| [BR-07](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-07/) | Buyer name: AccountingCustomerParty/Party/PartyLegalEntity/RegistrationName. |
| [BR-08](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-08/) | Seller postal address must exist. |
| [BR-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-09/) | Seller postal address needs Country/IdentificationCode. |
| [BR-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-10/) | Buyer postal address must exist. |
| [BR-11](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-11/) | Buyer postal address needs Country/IdentificationCode. |
| [BR-12](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-12/) | LegalMonetaryTotal/LineExtensionAmount is required. |
| [BR-13](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-13/) | LegalMonetaryTotal/TaxExclusiveAmount is required. |
| [BR-14](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-14/) | LegalMonetaryTotal/TaxInclusiveAmount is required. |
| [BR-15](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-15/) | LegalMonetaryTotal/PayableAmount is required. |
| [BR-16](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-16/) | At least one invoice line; credit notes use CreditNoteLine. |
| [BR-21](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-21/) | Each line needs ID. |
| [BR-22](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-22/) | Each line needs InvoicedQuantity (CreditedQuantity for credit note). |
| [BR-23](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-23/) | Quantity needs unitCode. |
| [BR-25](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-25/) | Each line needs Item/Name. |
| [BR-26](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-26/) | Each line needs Price/PriceAmount. |
| [BR-27](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-27/) | Net item price cannot be negative; do not fix credit notes by making prices negative. |
| [BR-62](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-62/) | Seller electronic address requires its scheme identifier. |
| [BR-63](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-63/) | Buyer electronic address requires its scheme identifier. |
| [BR-CL-25](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CL-25/) | EndpointID/@schemeID must satisfy the CEF EAS requirement. Its published XPath still includes all 14 May-removed Peppol schemes, including 0217; this expression alone does not prove their rejection. Match the supplied failed assertion and provider artefact/version. |
| [PEPPOL-EN16931-CL008](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-CL008/) | Peppol electronic-address scheme membership check on EndpointID/@schemeID, using the `$eaid` list. Read with the current published EAS list; request the provider's actual artefact/version when results differ from current membership. |
| [PEPPOL-EN16931-R003](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R003/) | BuyerReference OR OrderReference/ID must exist. Use the actual buyer routing reference or actual PO. |
| [PEPPOL-EN16931-R004](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R004/) | CustomizationID starts with urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0 and contains no ::. Remove release suffixes; preserve legitimate extensions only after checking the profile. |
| [PEPPOL-EN16931-R007](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R007/) | ProfileID must resolve to an approved process. Ordinary billing: urn:fdc:peppol.eu:2017:poacc:billing:01:1.0. Country/profile exceptions require exact lookup. |
| [PEPPOL-EN16931-R008](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R008/) | Empty leaf elements, including whitespace-only ones, fail. Required: populate; optional and unused: omit. |
| [PEPPOL-EN16931-R010](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R010/) | AccountingCustomerParty/Party/EndpointID must exist. |
| [PEPPOL-EN16931-R020](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R020/) | AccountingSupplierParty/Party/EndpointID must exist. |
| [PEPPOL-EN16931-R051](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R051/) | Money currencyID must match DocumentCurrencyCode, except invoice VAT total in accounting currency. |

## Arithmetic and precision

Use decimals, not binary floating-point. Recalculate commercial quantities, prices and confirmed tax rates without changing them. Group VAT by category and rate. Price base quantity defaults to 1 if omitted; do not divide by zero or change a supplied base. Line allowances and charges are already reflected in line net; document adjustments affect document totals separately.

| Rule | Required calculation / deciding constraint |
|---|---|
| [PEPPOL-EN16931-R120](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R120/) | LineExtensionAmount = quantity × (PriceAmount / BaseQuantity) + line charges − line allowances. The XPath uses slack 0.02; it is not a document-total tolerance. |
| [PEPPOL-EN16931-R121](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R121/) | Supplied Price/BaseQuantity must be greater than zero. |
| [PEPPOL-EN16931-R040](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R040/) | Allowance/charge Amount = BaseAmount × MultiplierFactorNumeric / 100; slack 0.02 when both operands exist. |
| [PEPPOL-EN16931-R041](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R041/) | Percentage supplied requires base amount. |
| [PEPPOL-EN16931-R042](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R042/) | Base amount supplied requires percentage. |
| [PEPPOL-EN16931-R046](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-R046/) | If gross price exists in Price/AllowanceCharge/BaseAmount, net PriceAmount = gross price − price discount Amount. Avoid double subtraction. |
| [BR-CO-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-10/) | Document LineExtensionAmount = sum of rounded line net amounts. |
| [BR-CO-11](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-11/) | AllowanceTotalAmount = sum of document-level allowances. |
| [BR-CO-12](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-12/) | ChargeTotalAmount = sum of document-level charges. |
| [BR-CO-13](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-13/) | TaxExclusiveAmount = line total − document allowances + document charges. |
| [BR-CO-14](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-14/) | Invoice-currency TaxAmount = sum of VAT breakdown TaxAmount values. |
| [BR-CO-15](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-15/) | TaxInclusiveAmount = TaxExclusiveAmount + invoice-currency VAT total. |
| [BR-CO-16](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-CO-16/) | PayableAmount = TaxInclusiveAmount − PrepaidAmount + PayableRoundingAmount; absent prepaid/rounding contributes zero. |
| [BR-S-08](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-S-08/) | For each standard-rated rate, TaxSubtotal/TaxableAmount reconciles matching line nets, document allowances and document charges. Exact XPath has its own tolerance; do not borrow 0.02. |
| [BR-S-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-S-09/) | Standard-rated breakdown VAT = taxable amount × Percent / 100, rounded to 2 decimals. The test compares absolute supplied VAT against rounded tax calculated from the absolute taxable base; their difference must be strictly below 1. This test alone does not establish the correct sign. Base −100, rate 20%, VAT +20 passes this magnitude comparison although signed arithmetic gives −20; inspect other rules and the actual document. |
| [BR-DEC-12](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-12/) | TaxExclusiveAmount: maximum 2 decimal places. |
| [BR-DEC-20](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-20/) | TaxSubtotal/TaxAmount: maximum 2 decimal places. |
| [BR-DEC-23](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-23/) | Line net amount: maximum 2 decimal places. |
| [BR-DEC-14](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-14/) | Tax-inclusive total: maximum 2 decimal places. |
| [BR-DEC-17](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-17/) | Payable rounding amount: maximum 2 decimal places. |
| [BR-DEC-18](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-DEC-18/) | Amount due: maximum 2 decimal places. |

Other amount limits: follow the syntax cardinalities and the current BR-DEC rules; a two-decimal amount limit does not impose the same precision on quantities or unit prices. XPath `round` and ordinary commercial rounding can differ for negative half ties: inspect the actual rule and provider output for such cases.

## VAT category decisions

The user or accountant supplies the tax treatment; an exporter error is not permission to select a different treatment. Line VAT category is Item/ClassifiedTaxCategory/ID; breakdown category is TaxTotal/TaxSubtotal/TaxCategory/ID, with TaxScheme/ID VAT. Rates are Percent; explanation fields are TaxExemptionReason and TaxExemptionReasonCode on the breakdown category.

| Category | Constraints and sources (read 2026-10-11) |
|---|---|
| S | Standard-rated: line rate > 0; calculate breakdown VAT from category/rate base. [BR-S-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-S-05/), [BR-S-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-S-09/) |
| Z | Zero-rated: line rate 0, breakdown VAT 0; no exemption reason. [BR-Z-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-Z-05/), [BR-Z-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-Z-09/), [BR-Z-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-Z-10/) |
| E | Exempt: line rate 0, breakdown VAT 0; exemption reason text or code required. [BR-E-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-E-05/), [BR-E-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-E-09/), [BR-E-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-E-10/) |
| AE | Reverse charge: line rate 0, breakdown VAT 0; reason must identify reverse charge. Additional seller/buyer identifier conditions require full validation. [BR-AE-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-AE-05/), [BR-AE-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-AE-09/), [BR-AE-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-AE-10/) |
| O | Outside VAT scope: line rate absent, breakdown VAT 0, outside-scope reason required; lines trigger restrictions on seller, tax representative and buyer VAT IDs. Do not remove true IDs before confirming treatment. [BR-O-02](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-O-02/), [BR-O-05](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-O-05/), [BR-O-09](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-O-09/), [BR-O-10](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-tc434/BR-O-10/) |

## Permitted codes and current-list pitfalls

All these code-list pages were read 2026-10-11. They are the published May 2026 lists, not arbitrary ISO/UNECE supersets. Membership alone does not prove the value is appropriate for the transaction.

- [eas](https://docs.peppol.eu/poacc/billing/3.0/codelist/eas/): Endpoint scheme list: 0088 GLN, 0184 Danish CVR, 0208 Belgian enterprise number, 0106 Dutch chamber number. Retain code leading zeros and validate actual registered identifier. May release removed 0037, 0147, 0154, 0170, 0177, 0193, 0194, 0202, 0203, 0205, 0212, 0213, 0215, 0217. Some removed codes remain in other identifier lists; do not use ICD as EAS. Normative Peppol membership differs from the published BR-CL-25 enumeration. CL008 is the Peppol membership check; preserve the actual failed assertion and ask the provider to reconcile its artefact/version with the current list before attributing a failure.
- [ICD](https://docs.peppol.eu/poacc/billing/3.0/codelist/ICD/): Legal/party identifier schemes use this different list. An ICD-listed scheme need not be valid for EndpointID.
- [ISO4217](https://docs.peppol.eu/poacc/billing/3.0/codelist/ISO4217/): Document currency codes: EUR, USD and GBP are examples; May release removed ANG and BGN and added XCG. Updating an actual currency may require conversion, not an attribute substitution.
- [UNCL5305](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL5305/): Published categories: AE, B, E, G, K, L, M, O, S, Z. B is Italy-only; G export, K intra-community, L Canary Islands IGIC, M Ceuta/Melilla IPSI require specific rules. Never infer these from a zero tax amount.
- [UNCL1001-inv](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL1001-inv/): Invoice-type code list; apply profile restrictions in P0100 too. 380 is a commercial invoice.
- [UNCL1001-cn](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL1001-cn/): Credit-note code list; apply profile restrictions in P0101 too. 381 is a credit note.
- [UNECERec20](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNECERec20/): Quantity unit codes: C62 = one/unit, HUR = hour, KGM = kilogram. Recommendation 21 package codes use X prefix. Do not export local labels such as pcs as if they were valid codes.
- [UNCL4461](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL4461/): Payment means: 30 credit transfer, 58 SEPA credit transfer, 59 SEPA direct debit; related account/mandate fields and country rules still apply.
- [vatex](https://docs.peppol.eu/poacc/billing/3.0/codelist/vatex/): Exemption reason codes when a code is supplied. Text-or-code requirements do not mean every zero VAT category needs an exemption reason.

[PEPPOL-EN16931-P0100](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-P0100/) (read 2026-10-11): for profiles 01 and 02 permitted invoice codes are 71, 80, 82, 84, 102, 218, 219, 326, 331, 380, 382, 383, 384, 386, 388, 393, 395, 553, 575, 623, 780, 817, 870, 875, 876, 877.

[PEPPOL-EN16931-P0101](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-EN16931-P0101/) (read 2026-10-11): for profiles 01 and 02 permitted credit-note codes are 381, 396, 81, 83, 532. Do not change commercial document type merely to fit a code.

## Country/context and severity

Check each exact XPath context, not just the message label. In this release Dutch identifier warnings do not by themselves establish the cause of a network rejection. For example, an invalid EAS scheme can still be fatal while a length check on the same identifier is a warning.

- [PEPPOL-COMMON-R054](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-COMMON-R054/) (read 2026-10-11): Warning: scheme 0106 identifier should contain 8 digits. Preserve a missing leading zero only when the data owner confirms it; never guess one.
- [PEPPOL-COMMON-R052](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-COMMON-R052/) (read 2026-10-11): Fatal: Danish P-number must be exactly 10 digits.
- [PEPPOL-COMMON-R053](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/PEPPOL-COMMON-R053/) (read 2026-10-11): Fatal: Danish SE identifier must be DK followed by 8 digits.
- [DK-R-017](https://docs.peppol.eu/poacc/billing/3.0/rules/ubl-peppol/DK-R-017/) (read 2026-10-11): Fatal in its Danish supplier/buyer context: a supplied buyer PartyLegalEntity/CompanyID needs schemeID 0184. Does not say every buyer worldwide needs a Danish ID.

## Provider retest handoff

Workflow recommendation, not an additional Peppol requirement: regenerate from corrected source fields; validate the complete document with the intended UBL schema and current EN16931, Peppol and applicable national rules; retain full failed-assert report and release identifier. Ask the provider to check registered recipient/process/document support and envelope addressing for recipient-not-found or delivery errors. Do not claim registration was checked from a screenshot. A successful content validator is distinct from network delivery and recipient acceptance.
