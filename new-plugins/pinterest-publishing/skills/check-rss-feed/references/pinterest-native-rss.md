# Official native RSS requirements

All pages opened and read 2026-10-11. These are recorded observations, not a promise that requirements remain current. Refresh the relevant official source when current requirements are needed, the supplied interface/error differs, or source age makes a deciding fact uncertain; distinguish refreshed facts from these observations. Evaluate effective dates against the current task date. If retrieval is unavailable, qualify any deciding fact that could not be refreshed. Paraphrases below; no page update date shown on the two help articles.

## RSS publishing
https://help.pinterest.com/en/business/article/auto-publish-pins-from-your-rss-feed

Scope: Pinterest business-account native RSS, not catalogs or API uploads. Sections “Before you get started”, “Connect your RSS feed”, “RSS feed specs”, “RSS feed error messages” support: claimed-site matching; unlimited matching feeds; per-feed boards; secret-board visibility; up to 24-hour processing; oldest first; up to 200 Pins/day; desktop connection and claim prerequisite; RSS 1.* RDF / 2.* XML support and Atom exclusion; item image/enclosure/media:content, title/description and claimed-domain link fields. The introduction explicitly includes multiple images in an item or webpage. The error table maps existing/fetch/parse/format/domain errors to distinct actions. It does not document re-ingestion, retries, exact scheduling, GUID deduplication or RSS-specific image/title size limits.

## Website claiming
https://help.pinterest.com/en/business/article/claim-your-website

Scope: claim ownership and verification. “Types of websites you can claim” requires ownership of domain/subdomain/subpath and control needed to verify; one Pinterest account can claim a website. Most marketplace stores cannot be claimed. Verification choices: HTML tag, root-level HTML file, DNS TXT; Google Merchant Center only for some accounts. HTML tag belongs in head; file in root, not a subfolder. TXT changes may take up to 72 hours. Claim initiation appears under Settings → Link to Pinterest → Claim next to Websites; existing claims are described under Settings → Claimed accounts. This page itself uses both menu names: ask for the user's described screen rather than inventing a universal menu. This claim guide does not require every claimant to have a business account; native RSS does.

## Publishing policies
https://policy.pinterest.com/en/community-guidelines

Page says last updated May 2026. The announced November 12, 2026 revision is future text on this read date; do not apply it early. “Spam” forbids unapproved automation, repetitive/deceptive/irrelevant money-making content, spam evasion and deceptive redirects; links should have original value. “Intellectual property and other rights” requires respecting others' rights. “Site security and access” disallows unsupported access methods and sharing account access. Valid XML cannot establish policy approval. Do not label an unexplained delay a policy violation.

## Diagnostic practices (authored, not Pinterest requirements)
Separate observed XML errors from suspected hosting or account issues. Require complete bytes for a whole-document parsing conclusion. Escape raw ampersands in XML text (or use CDATA where appropriate), bind namespace prefixes, and preserve supplied facts when proposing edits. An image URL opening for a user does not prove Pinterest can fetch it. Check only relevant public URLs when requested. No claim here establishes a tested Pinterest account connection.

## Initial setup timing
https://create.pinterest.com/en-in/product-features/bulk-content-creation/?change_language=true

Read 2026-10-11; no page update date shown. The RSS section says content generates Pins within 24–48 hours when setting up a feed, desktop only, business account and claimed site, up to 200 images daily. RSS Help separately says feed updates add content within 24 hours and uses a 200-Pin cap. Preserve both scopes; neither page establishes a guaranteed completion time for a backlog. This page also covers Instagram, partners and CSV; those sections are outside this package.

## Applying repairs to the requested answer

Put the requested XML or item repairs first; include only remaining blockers that affect them. A full document supports whole-feed checks; excerpts support only visible findings. Report local parsing as completed only when it was actually run. Pinterest’s listed RSS requirements specify no minimum item count. Keep supplied example destinations by default; distinguish illustrative URLs from literal hosting targets only when relevant. Apply explicitly supplied or approved replacements when the requested operational repair includes them; if a replacement is unknown, label a value-preserving artifact syntax-only or mark the proposed repair incomplete.

For RSS 1.0 structure, consult the [RSS-DEV specification](https://web.resource.org/rss/1.0/spec) (opened 2026-10-11), sections 5.3–5.5: items use `rdf:about`; channel `link`, `description` and `items`/`rdf:Seq` belong in the complete document, and an image reference points to its image definition. If those sections were omitted from a pasted excerpt, check them conditionally rather than declaring defects. These are RSS structure checks, not additional Pinterest GUID or image-size requirements.
