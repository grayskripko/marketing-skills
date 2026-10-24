# Xero source register

Read 2026-10-11. Direct URLs load Salesforce HTML shells; search retrieval supplied complete indexed article text (index age about two months). Publisher update dates are not exposed. These are official public-document snapshots, not observations inside a client's organisation. Recheck source content and the current regional template before 2026-10-17 submission; do not label a future date as verified.

## Native — AU regional article
https://central.xero.com/0/article/Add-import-and-post-manual-journals-AU

Supports native draft import, 300 transaction lines per template file, base currency and advisor or standard + reports access. Date/narration define journal groups; blank pairs continue a group. AU dates: dd mmm yyyy or dd/mm/yyyy. Amount signs distinguish debit and credit. Account codes exclude names; tax imports use full organisation names. Missing tax can enter a draft, but needs completion for posting. Amount basis controls tax editing. Both tracking columns are needed; one-sided tracking can generate Tracking Transfers. The source permits adding lines after import. Do not apply AU date formats to other regions without checking their template. No published UI error-message catalogue was verified.

## Conversion Toolbox
https://central.xero.com/0/article/Import-manual-journals-using-the-Conversion-Toolbox

Supports prior-system CSV imports; prepare chart accounts and tracking first. Same number/narration/date joins rows. Date formats dd/mm/yyyy and yyyy/mm/dd also apply to US organisations. One signed amount column or two debit/credit columns can be mapped. Codes omit names; tax names match settings. Tracking may be supplied or assigned in mapping. Per-journal balance is required; failure follows imbalance. Bank and some system accounts need holding accounts. Field, tax and account mapping precede draft/approved selection and detailed preview. Changed file content requires reselecting the CSV. The article states any number of journals and transaction lines, without the native 300-line limit. No measured practical upload size limit was established.

## Restricted accounts and padlocks
https://central.xero.com/0/article/Locked-and-system-accounts-in-your-chart-of-accounts-GL

Read 2026-10-11. General UI account scope. A locked non-system account may be used in a manual journal. Prohibited system accounts: Accounts Payable, Accounts Receivable, Bank Revaluation, Current Earnings, Tracking Transfers, Unpaid Expense Claims, Unrealised Currency Gains. Permitted: Historical Adjustments, Realised Currency Gains, Retained Earnings, Rounding, Sales Tax. Secondary accounts can record movements; use matching account types and report grouping. The GL article lists advisor access for account creation; the general article lists administrator access. Preflight does not create accounts. A preflight proposes a supplied approved mapping; it does not create an account or select accounting treatment. This UI table must not be replaced by API-specific restrictions.

## General/AU system-account table
https://central.xero.com/0/article/Locked-and-system-accounts-in-your-chart-of-accounts

Read 2026-10-11; current search index reports crawled today. This table adds Wage Payables to the prohibited accounts and labels the permitted tax account GST. It also says administrator access is needed to add secondary accounts. Both tables permit ordinary locked non-system accounts. Check the applicable region and organisation account availability rather than assuming the GL table is exhaustive globally.

## AU GST amount basis
https://central.xero.com/0/article/How-GST-works-in-Xero

Read 2026-10-11 via indexed official text. No Tax calculates no GST and applies BAS Excluded; Tax Inclusive and Tax Exclusive allow line tax selection. BAS Excluded items are outside the activity statement. Require amount basis for a tax-bearing balance; do not manufacture a tax adjustment or ask a zero-tax example for a setting that cannot change its arithmetic. This is AU GST scope, not a rule about other countries' tax names.

## Tracking capacity
https://central.xero.com/0/article/Set-up-tracking-categories

Read 2026-10-11. Four categories total, two active. A category needs an option before assignment. At most 100 options per category is a reporting-performance recommendation, not a stated hard limit. Exact category/option names and their availability must come from the destination organisation.

## Authored review choices

Row numbers, separate import/posting findings, partial-pair clarification, separate-file preservation of identical native titles/dates and proposed-only repairs are this plugin's rule of thumb. No imported-system date conversion or account substitution is inferred. The source register supplies rules, not permission to submit data or post entries.
