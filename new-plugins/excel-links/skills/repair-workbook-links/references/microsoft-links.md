# Microsoft workbook-link reference notes

All pages below loaded with substantive content; read 2026-10-11. These are access dates, not publication dates. Undated Support pages had no displayed revision date. Publisher maintenance only, not a runtime instruction: recheck before the planned 2026-10-13 submission if policy or behavior changes. Use these bundled notes locally; do not fetch the linked pages during this workflow. Platform tabs matter; Windows/web instructions are not a promise of identical Mac menus.

## Management

https://support.microsoft.com/en-us/excel/manage-workbook-links

Sections: Find workbook links; Break a workbook link (Windows and Web); FAQ; Link refresh settings. Covers names, objects and charts beyond formulas, query-parameter dependencies, link removal, startup preferences and web cross-domain failures. Its web FAQ identifies “Not logged in” for cross-domain, cross-geography and cross-tenant refresh; desktop is the documented alternative. The current page distinguishes desktop's irreversible Break links from web Undo. It does not establish full coverage from a pasted search export.

## Storage

https://support.microsoft.com/en-us/excel/description-of-workbook-link-management-and-storage-in-excel

Sections: Relative vs. absolute links; three storage configurations; mapped drives vs. UNC; failure scenarios. The formula bar is not a reliable view of the serialized path. Same-folder/child, sibling-folder and different-drive cases store different path forms; opening-route changes can break links and saving can retain the bad path.

## File Block policy

https://support.microsoft.com/en-us/excel/external-workbook-links-to-blocked-file-types-will-be-disabled-by-default

Effective date stated: October 2025. Sections: What to expect; Review File Block Settings. Existing blocked links retain last successfully refreshed values; new links show #BLOCKED with restricted-type error detail. Microsoft's page also describes a security-reducing registry override and labels re-enabling not recommended. Recommend reviewing the actual File Block settings and using an approved converted replacement; do not recommend the registry override. It does not assert a universal blocked-extension list; inspect the actual settings.

## Syntax

https://support.microsoft.com/en-us/excel/create-workbook-links

Sections: source/destination; create links between cells; defined names. A closed source adds a path to the displayed formula; generated links use absolute cell references. Preserve reference semantics during manual edits. Source means workbook supplying data; destination means workbook holding the reference.

## Reference errors

https://support.microsoft.com/en-us/excel/how-to-correct-a-ref-error

Sections: invalid cell references; closed workbook with INDIRECT. Invalid/deleted references cause #REF!; closed-source INDIRECT and dynamic-array references have separate failure behavior. This does not mean every #REF! is a broken workbook path.

## Named 3-D edge case

https://learn.microsoft.com/en-us/troubleshoot/microsoft-365-apps/excel/update-external-links

Publisher update: 2026-03-31. Scope: .xlsx source defined name referring across sheets, external named reference in another .xlsx destination, then save/close both files, reopen the destination and update links. Confirm every condition before assigning this diagnosis. Workarounds listed: both files .xlsb, or avoid that external named 3-D reference. Content loaded despite an authorization banner; no account was used. Generic update errors alone do not establish this scenario.

## Safety recommendations

Generate applicable user-operated steps from these recommendations; the user or source owner performs every Excel/file operation and reports observations.

Separate backup; prefer one confirmed target; verify source meaning; compare before saving; reopen through intended route; do not certify an excerpt as a complete workbook audit. These are this package's safety recommendations, not vendor promises.

## Applying the notes to the requested answer

Use the relevant section inline with the requested diagnosis or action; these notes do not require a separate source report or checklist. Trace local chart inputs, name chains and query helpers when inventorying dependencies. For dual mapped/UNC access, use a confirmed UNC source and verify both destination routes. For an archive, retain confirmation records and local query results before removing their dependencies, then verify without source access. For live web or blocked-format repairs, retain an authoritative, maintained source: desktop cloud refresh must be saved back, and an approved-format replacement must be genuinely converted and kept current. For a direct total-cell workaround, recalculate and save the source before checking closed-source updates. These are case-specific application recommendations; retain the exact platform and failure scope above.
