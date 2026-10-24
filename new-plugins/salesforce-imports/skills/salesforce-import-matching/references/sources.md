# Matching source register

Read 2026-10-11. All pages opened successfully and contained article text. These are current public documentation observations, not guarantees about a particular org or the future submission date. Publication dates are included where displayed; other pages have the access date above. Supporting details below are paraphrased; the deciding rules are inline in SKILL.md.

| Official source and URL | Verified scope / supporting detail |
|---|---|
| [Custom objects](https://help.salesforce.com/s/articleView?id=sf.importing_matching.htm&language=en_US&type=5) | Wizard: Name, Salesforce ID, External ID; Name is case-sensitive; only unique External IDs are offered; auto-number cannot match; input duplicates are not uploaded. |
| [Wizard workflow](https://help.salesforce.com/s/articleView?id=xcloud.import_with_data_import_wizard.htm&language=en_US&type=5) | Separate add/update/combined modes, explicit mapping, unmapped fields omitted, workflow/process options. |
| [Lead matching](https://help.salesforce.com/s/articleView?id=xcloud.for_leads.htm&language=en_US&type=5) | Name matching is case-sensitive; Email matching uses exact values; None creates input leads; selected matching criteria determine identity. |
| [Business accounts and contacts](https://help.salesforce.com/s/articleView?id=sf.for_accounts_and_contacts.htm&language=en_US&type=5) | Account Name and Site; paired Salesforce-ID selection; account overwrite checkbox preserves populated values by default and cannot clear with blanks; access affects matching. |
| [Import Data, Trailhead](https://trailhead.salesforce.com/content/learn/modules/lex_implementation_data_management/lex_implementation_data_import) | Wizard up to 50,000, Data Loader up to 150 million; object, edition, access and storage constrain imports. Recommends a small test file. |
| [Data Loader operations](https://help.salesforce.com/s/articleView?id=inserting_updating_or_deleting_data.htm&language=en_US&type=5) | Upsert selects an ID or External ID; related-object key selection is separate; success/error CSVs record outcomes. |
| [SOAP upsert](https://developer.salesforce.com/docs/platform/api/guide/sforce-api-calls-upsert.html) | No match creates, one match updates, multiple matches fail. Non-unique External ID requires View All Data in this SOAP call; case-insensitive matching depends on Unique and its case option. Do not transfer Wizard behavior. |
| [Common Data Loader errors](https://help.salesforce.com/s/articleView?id=000384437&language=en_US&type=1) — published 2026-05-25; read 2026-10-11 | External-key Update null mapping error: setting expects an External ID in CSV mapping; documented resolution is unchecking it. Standard-ID fallback requires verified Id mapping. Does not establish every supported version or API mode. |
| [Configure Data Loader](https://help.salesforce.com/s/articleView?id=sf.configuring_the_data_loader.htm&language=en_US&type=5) — read 2026-10-11 | Current table distinguishes SOAP/default, Bulk and Bulk 2.0; it does not list the external-key Update setting. No complete cross-mode alternative workflow is inferred. |
| [Related records by External ID](https://help.salesforce.com/s/articleView?id=000383207&language=en_US&type=1) — read 2026-10-11 | Related-object External ID selection and relationship mapping; distinguish the target upsert key from the parent lookup. For an Opportunity Account lookup, use `Account:ERP_Account_Key__c`. |
| [Blank or null values with Data Loader](https://help.salesforce.com/s/articleView?id=000385542&language=en_US&type=1) — read 2026-10-11 | Explicit null updates use Insert Null Values with Bulk API disabled; Wizard blank cells do not clear populated account fields. |

| [Null values and Bulk API](https://help.salesforce.com/s/articleView?id=Data-Loader-Behavior-with-Bulk-API-Enabled-using-Insert-null-values&language=en_US&type=1) — read 2026-10-11 | Insert Null Values applies with Bulk API disabled; Bulk ignores empty cells. |

## Scope and editorial choices

Official Wizard and Trailhead pages list somewhat different standard-object examples. Do not treat either example list as exhaustive: confirm the actual object's availability and edition rather than categorically excluding Opportunities. A file above 50,000 rows exceeds the Wizard limit regardless. Agent decision policy: hold ambiguous or unverified identities and keep update-only intent; release established identities when applicable prerequisites are met. Investigate duplicate rules when creation, supplied errors, changed fields or known org rules make them material. Hold the whole batch only for a shared unresolved issue affecting every row. These are editorial decision policies, not Salesforce limits. Privacy, output format, no account writes, and no key normalization without an identity convention are editorial safeguards.

The accounts/contacts article’s general access warning does not establish a replacement-creation outcome for a supplied Update existing configuration. Hold inaccessible rows without inventing that outcome; show the existing values and distinguish account from contact mappings.

Platform matching and access behavior can change. On a requested refresh, retrieve only these official public URLs; never include row values or org URLs. No release-specific date formats or API settings are claimed without tool-specific evidence.
