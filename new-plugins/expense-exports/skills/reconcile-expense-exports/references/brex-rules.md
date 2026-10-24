# Brex export rules — source register

Observed/read 2026-10-11. All seven URLs loaded as substantive Brex Help Center articles. No publication or last-update date was visible in the retrieved article text; the date records verification, not publication. Re-open relevant pages before the planned 2026-10-17 submission and when a supplied error or UI differs. These are current retrieved rules for their named workflows, not inferred account settings.

| Official source and section | Decision supported |
|---|---|
| [Exporting to your integration](https://www.brex.com/support/integration-exporting), Export settings, CSV exports, Troubleshooting | Debit/Credit GL required; configurable requirements; non-retroactive reimbursement cutover; vendor prerequisites; ZIP versus SFTP; missing assignments, conflicting rules and entity/location errors. |
| [QuickBooks Online integration](https://www.brex.com/support/quickbooks-online-integration), Exporting, Troubleshoot | CSV marks exported without delivery; separate bank feed; card-payable account type; stale mappings; repeated large-batch errors and 2,000-row retry guidance; payment-date mismatches. |
| [How the Accounting page works](https://www.brex.com/support/brex-dashboard-accounting-page), Prepare, Review, Exported, Downloading, Export history | Selection blocked by one incomplete row; receipt compliance differs from coding; ordinary downloads; batch evidence; exported changes do not sync; send-back preserves ERP entries. |
| [General Ledger accounts](https://www.brex.com/support/general-ledger-accounts), Manage GL visibility, Refresh | Disabled values disappear from selection; ERP account changes require refresh for immediate availability. |
| [Fields library](https://www.brex.com/support/accounting-fields), Connecting user fields to accounting fields | User and accounting Department differ; historical expenses created without a user department need manual coding. |
| [NetSuite integration setup](https://www.brex.com/support/netsuite-integration), Connecting NetSuite, Setting NetSuite defaults, Troubleshooting | Receipt URL and Created From shown on preferred journal lines; other export objects need corresponding forms configured; mandatory-field errors require per-entity defaults, including the generated AP line, even with coded expense rows. |
| [Syncing reimbursements to your integration](https://www.brex.com/support/reimbursements-integration-sync), Export formats, Switch export formats, Closing exported vendor bills in ERP manually | ERP-specific objects override general defaults. QBO journals/bills; Xero bills only; Workday/Oracle journals. Email-first vendor matching, name fallback for duplicate emails; statement-cycle consistency; payment export closes Brex-paid bills, manually closing a Brex-paid bill causes a later payment-export error; external payments require manual bill closure when paid. |

## Interpretation boundaries

Brex’s Accounting article describes a failed batch as not reaching the ERP. A user-supplied ledger or manual import may nevertheless contain the same expenses: reconcile that evidence before retrying. The successful direct-ERP status definition does not override QuickBooks’ explicit CSV exception.

Reconciliation methods—stable-ID matching, candidate labels for fuzzy matches, separate currency totals, and inspecting existing entries before retry—are this plugin’s rules of thumb. They are analysis choices, not claimed Brex field constraints. The sources specify no universal safe retry count or automatic deletion of ERP entries.
