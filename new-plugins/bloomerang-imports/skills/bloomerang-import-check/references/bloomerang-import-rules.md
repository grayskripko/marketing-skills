# Bloomerang CRM donation import rules

Read 2026-10-11. Scope: Bloomerang CRM Data Tools importer, not Fundraising offline gifts, peer-to-peer participants or Volunteer imports. Each linked official page loaded during this build. Dates below are the publisher's displayed dates, not invented publication times. Refresh these pages near the planned 2026-10-20 submission and record any changes.

## Source register

| Source | Publisher date | URL | Deciding knowledge |
|---|---|---|---|
| Set Up Import Files | 2026-05-14 | https://help.bloomerang.com/en/articles/12632800-imports-set-up-import-files | CSV format; separate individual/organization files; supported/excluded records; 10,000 rows and 2MB; matching; recent gifts and Journey Automation |
| Required Fields | 2025-12-11 | https://help.bloomerang.com/en/articles/12632768-what-are-the-required-fields-for-an-import | New-record names differ from existing-record identity; timeline entries can create constituents; tokenized joint-account first names |
| Update Constituents via Import | 2026-07-30 | https://help.bloomerang.com/en/articles/12632440-imports-update-constituents-via-import | Account IDs preferred; name plus secondary identity; donations/notes/interactions create only; household-head and primary-contact effects |
| Import Fields | 2026-06-09 | https://help.bloomerang.com/en/articles/12632811-imports-import-fields | Existing custom fields/options; one donation per row; mm/dd/yyyy; Cash default; supported payment methods; one contact entry per type; phone format |
| Import Errors | 2026-01-23 | https://help.bloomerang.com/en/articles/12632752-imports-import-errors | Missing fields; unknown account IDs; negative amount; numeric pick-multiple exclusion; 255-character header limit; automatically managed groups |
| Import Data into Bloomerang CRM | 2026-01-29 | https://help.bloomerang.com/en/articles/12632760-imports-import-data-into-bloomerang-crm | Saved template settings; preview/mapping; contact entries add rather than overwrite; skipped-record retry |
| Work with the Imports List | 2026-01-23 | https://help.bloomerang.com/en/articles/12632468-imports-work-with-the-imports-list | Recent-import detail, original-file download and skipped-record download |
| 2026 Bloomerang CRM Release Notes | 2026-10-08 (HTML timestamp); latest dated section 2026-10-08 | https://help.bloomerang.com/en/articles/16058779-2026-bloomerang-crm-release-notes | Current release review; October soft-credit change concerns credit amounts, not an added CSV field or permission to import pledge payments |

## Creation and matching

Source support: Required Fields, sections for new and existing constituents; Setup, required-fields and matching sections; Update, matching section.

Creation requires both personal names for an individual or Organization Name for an organization. An existing constituent can instead be identified by its Bloomerang Account Number. Every donation additionally needs Date, Amount and Fund. A donation import can create a constituent when the creation fields are present; do not demand an account number for an intentionally new constituent.

Without an account number, the newer Setup and Update pages require the constituent's name plus email, standardized street address, or matching last-seven phone digits. A name alone or email alone is insufficient. Tokenized first-name matching may identify a joint account; it is not permission to create two constituents. No official source here establishes a local algorithm for address standardization or arbitrary fuzzy import matching.

**Source disagreement:** Required Fields lists the organization's email combination using personal first/last names; Setup and the later Update page describe organization identity with the constituent name plus email. Use the newer organization-name rule, record any affected uncertainty and prefer a verified account number for a disputed organization. Do not treat the primary contact as the organization's donor identity.

**Interpretation for supplied exports:** valid columns establish an eligible matching route; they do not prove that the unique intended account exists. Export absence is conclusive only within its stated coverage. Unknown IDs should be corrected, not silently removed. An account/type/name conflict is held pending resolution. These evidence-handling choices are preparation conventions, not a claim about undocumented importer precedence.

## Format, limits and values

Source support: Setup, file-size and setup sections; Fields, donation/contact sections; Errors, field-value/header rows.

The stated limits are 10,000 rows and 2MB. Header inclusion and MB's byte definition are not specified. A file with embedded newlines needs CSV-record counting, not physical line counting. Preparation convention: at most 9,999 donation records plus header and at most 2,000,000 serialized bytes; show exact counts at the boundary and verify in the importer. This convention intentionally stays inside either common interpretation and is not an additional product rule. Bytes include headers, quotes, encoding and line endings; do not estimate original file bytes from a pasted excerpt.

Dates are mm/dd/yyyy. Each donation occupies one CSV record. A blank Transaction Method becomes Cash. Permitted methods: Cash, Check, Credit Card, EFT, In Kind, Apple Pay, Google Pay, PayPal, Venmo. An unknown method must not become an invented payment history. The negative-amount error covers a parenthesized negative number; a refund must not be repaired by reversing its sign.

Funds, campaigns, appeals and custom field definitions/options need to exist beforehand. Import cannot create/delete custom definitions or pick-list options. New user-managed groups are an explicit exception to the general existing-values wording. Automatically managed donor or membership groups are excluded. Pipes separate generic pick-multiple options; numeric pick-multiple values cannot be imported. Column labels have a 255-character ceiling.

Contact types use separate columns. Only one entry of each address/email/phone type per import; the last mapped contact column in CSV column order within each address/email/phone category becomes primary. With Home Email before Work Email in the CSV, Work Email becomes primary even when Home Email is mapped last. Place the intended primary column last among mapped columns in its category and review preview. Source: Import Data, Map the Data; Setup, file setup (both rechecked 2026-10-11). Phone values require at least ten digits, extensions use x, international numbers begin with +. Treat these strings as text. Phone matching's seven-digit suffix does not relax the ten-digit phone-field requirement.

## Operation and retry boundaries

Source support: Setup, supported data; Update, introduction and household section; Import Data, preview/import sections; Imports List, recent imports.

Constituent profiles can be created or updated. Donation, interaction and note imports create entries; they do not update previous entries. Pledges, pledge payments, recurring donations, tasks and refunds are excluded. A household may have its name fields updated through its account number; other profile fields affect the head of household. Household creation is excluded. This is not a household donation-routing guarantee.

Import template name, data type and individual/organization choice become fixed after save. Preview shows proposed creations/updates, not completed work. Added address/email/phone values create entries instead of overwriting existing entries. Review update choices and primary effects.

Setup says gifts dated in the last 30 days can qualify donors for donation acknowledgement Journey Automation when used. That is conditional on configured automation; no default-on claim or suppression behavior is documented here.

Use Download Skipped Records after a partial run. Reimport only the corrected skipped subset; successful test or production rows must not be included again. Same donor/date/amount can also mean two real gifts: deduplication needs supplied history or approval. The how-to suggests one or two test records early and five later; this package uses the smaller test set and removes successful test gifts from a subsequent batch. No account import is performed by the skills.

## Error-to-repair lookup

These are recognizable fragments; quote the actual user's message in an answer.

| Message fragment | Meaning | Repair |
|---|---|---|
| field “is required” | Missing required value or mapping | Restore/map the field for every affected record |
| “Account number is required when Household is mapped” | Household names mapped without household identity | Add verified household numbers for affected rows |
| “not a valid value” | Wrong field type/option, or a multi-value separator problem | Check mapping and accepted options; use pipes where applicable |
| Negative parenthesized Amount | Negative donation value | Resolve sign/source intent; do not convert a refund into a donation |
| “No matching Bloomerang account number” | Specified constituent ID does not exist | Correct using verified export; removing an ID requires an identity decision |
| “numeric pick multiple” | Unsupported numeric multi-select import | Keep source values for manual entry; remove only the upload mapping |
| Header over 255 characters | Label too long | Shorten uniquely, preserve source mapping |
| “Every line in your file has an error” | No records can import | Recheck all field mappings before repairing individual values |
| “automatically-managed groups” | Managed donor/membership group target | Use an appropriate user-managed group or remove mapping with approval |

The older Errors page says household data cannot be imported in the unknown-ID tip; newer Setup and Update expressly allow household-name updates with household numbers. Use that narrower, newer distinction rather than a blanket household prohibition.

## Preparation conventions, not vendor requirements

Proceed/Repair/Hold labels, record-number tracing, conservative byte/header choices, conflict holds, unconfirmed-export treatment, amount/count reconciliation, no guessing, and keeping unresolved rows separate are authored workflow choices. They prevent silent data loss or donor reassignment. No invented minimum amount, column-count ceiling, currency conversion, gift deduplication key, identity precedence or automatic automation suppression is specified.
