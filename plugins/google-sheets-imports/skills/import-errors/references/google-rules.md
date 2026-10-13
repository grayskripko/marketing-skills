# Google Sheets rule register

Verified by opening the official pages on 2026-10-11. The Google Help pages displayed no publication or last-update date; read dates are access dates. The Developers guide below displays its own update date. The publisher should recheck these sources before submission; this release-check note does not authorize assistant browsing. Scope is Google Sheets IMPORTRANGE, not other import functions or Excel. Summaries below are paraphrases; do not treat nearby product limits as IMPORTRANGE limits.

## IMPORTRANGE — syntax, permissions and runtime

URL: https://support.google.com/docs/answer/3093340?hl=en
Read 2026-10-11; loaded successfully.

Supporting sections: Syntax; Permission & access; Performance; Usage Limits; Data Freshness; Volatility; Technical details & best practices.

- Arguments accept text or cell references. A1 imports without a tab use the first sheet. Named ranges and table references are supported.
- Destination connection grants differ from personal source access. Destination editors may import the whole source. The grant persists until its granting user loses source access; Google states it counts against a 600-user share limit.
- Export restrictions block new imports; existing formulas continue.
- Received data is limited to 10 MB per request, not a row count. Source calculations and chains delay imports; cycles prevent output. Aggregate before transfer.
- Throttling covers creator-wide import usage in open documents, including collaborator edits. No numerical request quota is supplied.
- Hourly checks occur while open. Re-entering formulas can reload; browser reload is not a forced refresh. Activation behavior is separately described around five minutes.
- Direct and indirect NOW/RAND/RANDBETWEEN dependencies are prohibited; TODAY is excepted. Static values lose automatic updates.

The document-activation and browser-reload passages are distinct; neither supports an immediate-refresh guarantee. The page's 600-user link currently leads to shared-drive membership documentation. Preserve the IMPORTRANGE page's own statement without extending that number to every Drive sharing configuration.

## Optimize your data references to improve Sheets performance

URL: https://support.google.com/docs/answer/12159115?hl=en
Read 2026-10-11; loaded successfully.

Supporting sections: Reference data on the same Sheet when possible; Use closed range instead of open range references; Avoid long reference chains when possible.

Cross-file references use an internet round trip even for the same owner, browser and Drive. Bounded A1 ranges reduce unnecessary work. Local copies are suitable for relatively static data and must not be sold as live synchronization. Dependent calculations wait for earlier values.

## Stop, limit, or change sharing

URL: https://support.google.com/drive/answer/2494893?hl=en
Read 2026-10-11; loaded successfully on retry with the English URL after a linked fetch timed out.

Supporting section: Prevent people from downloading, printing, or copying your file.

Current UI: Share → Settings → People who can download, copy, and print; owners select permitted roles. Administrators can restrict owners through Drive DLP. Do not recommend bypassing owner or administrator controls. The new-versus-existing IMPORTRANGE distinction is supported by the function page above, not inferred from this general sharing article.

## Use tables in Google Sheets

URL: https://support.google.com/docs/answer/14239833?hl=en
Read 2026-10-11; loaded successfully.

Supporting sections: Create table names; Use table references.

Table names cannot start with a number, exceed 255 characters, use TRUE/FALSE or cell-reference syntax, or contain special characters other than underscores. Spaces in table names become underscores in formulas. Table/column references adjust when table data is added or removed; verify the actual table and header names before repairing a reference.

## Name a range of cells

URL: https://support.google.com/docs/answer/63175?hl=en
Read 2026-10-11; loaded successfully.

Supporting section: Name a range.

Named ranges use letters, numbers and underscores; no spaces or punctuation. They cannot start with a number, TRUE or FALSE, use A1/R1C1 syntax, or exceed 250 characters. Check the existing name in the source before recommending a rename; a rename can affect other formulas.

## Google Sheets API overview — A1 notation

URL: https://developers.google.com/workspace/sheets/api/guides/concepts#cell
Read 2026-10-11; loaded successfully. Publisher footer: last updated 2026-09-03 UTC.

Supporting section: A1 notation, especially the single-quote requirement and object-name ambiguity tip. Quote sheet names containing spaces or special characters inside the IMPORTRANGE range string, for example `"'Quarter Sales'!A1:C20"`. This cites A1 syntax only; it does not authorize Sheets API access. The IMPORTRANGE first-sheet default comes from the function page, not the API's first-visible-sheet example.
