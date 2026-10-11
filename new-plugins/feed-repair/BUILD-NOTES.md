# Build notes

Built 2026-10-11 for planned submission around 2026-10-13. Slug stays `feed-repair`; display name is Feed Repair. No submission, publication or approval is claimed.

## Scope and decisions
The judged queue row and reasoning select field-specific Pinterest native RSS diagnosis: supported formats and claimed-domain links can explain publishing failures directly. Two skills cover item-level repair and native setup/status guidance. Core deciding knowledge is inline in both; each has a self-contained official source register. No connectors, scripts, account access or automatic publishing are included. Pasted XML, exports and user-described screenshots provide a no-setup route.

Both manifests follow the reference package's field structure; version 0.1.0, MIT, author Sergey Skripko. Personal author email omitted. A simple original RSS/check icon is included. The workspace has no root README or Git repository. No feed-repair row was found in the older PLUGINS.md or topic research; the current judged queue and user-specified slug/name control. Older names/policy research was read for packaging context but has no specific naming recommendation for this scope.

## Official sources verified
All four loaded through live web retrieval on 2026-10-11:
- https://help.pinterest.com/en/business/article/auto-publish-pins-from-your-rss-feed — format, field, error, board, timing and cap rules; no update date shown.
- https://help.pinterest.com/en/business/article/claim-your-website — ownership, single-account claim, verification methods and DNS wait; no update date shown.
- https://policy.pinterest.com/en/community-guidelines — native versus unauthorized automation, spam and redirect boundaries; page states May 2026 update.

Precise rule scope and unsupported behaviors are recorded in each skill's references/pinterest-native-rss.md. No historical source date was reused as a current verification date.

- https://create.pinterest.com/en-in/product-features/bulk-content-creation/?change_language=true — initial setup described as 24–48 hours; no update date shown. Added after the comparison exposed this useful timing distinction.

## Names and adjacent work
Local manifest/skill search found no other exact chosen names. Live web searches for Feed Repair and both skill slugs did not establish an exact Pinterest-native listing; this does not reserve a name. An adjacent Merchant Center repair product appeared, with different platform and input scope. The judged row's Pinterest Search and RSS Aggregator links were attempted but the web reader could not load them. Historical demand counts are therefore not reasserted as current. This build differentiates through item fixes tied to native RSS requirements, rather than search or aggregation.

## Plain-language pass
Changed “absence of image fields is a rejection” to “absence of an item image is a repair opportunity, not proof that webpage discovery will fail” because the official introduction permits webpage images. Changed “200 articles daily” to “up to 200 Pins per day” and retained the multiple-image implication. Setup is described as guidance through settings, without suggesting a tested connection.

## Verification and open questions
JSON parsing, front matter, 60–120-word skill descriptions, reference links, and private-string checks passed. Public repository and author URLs are intentional exceptions to the historical broad `gray` scan; no private strings are included.

Manual and live instruction evidence is recorded in REVIEW.md and tests/RESULT.md. These checks concern supplied-instruction behavior and text packaging, not installed-host automatic selection or live Pinterest publishing.

Reopen official requirements before the planned submission. Undocumented: old-item edits/re-ingestion, exact queue completion, retry/backfill behavior, subdomain/subpath matching beyond the verified claim scope. Ask for actual evidence rather than invent rules. Public documentation/privacy URLs follow the intended repository location; this local build has not published them, so publication and URL verification are required before submission. Directory availability and acceptance remain unresolved.


## bfix-feed-repair — 2026-10-11

Both independent reviews returned FIX, not REBUILD. Retained the plan's Pinterest-native scope and `feed-repair` slug. Reopened all four official sources on this date; formats, fields, errors, claim methods, timing and Pin cap remain supported. The Community Guidelines page announces a November 12, 2026 revision; the source register now separates that future revision from the May 2026 text currently in effect.

Applied shared answer-shape fix: “Start with a concise item table” became “Lead with the deciding whole-feed blocker, next action, or exact corrected XML fragment.” Tables are conditional on multiple findings; setup is conditional on the request or an evidenced blocker. Removed setup from the narrow worked example. Clarified that a value-preserving XML artifact retains the supplied destination and explains a needed replacement separately. For an already-connected duplicate feed, keep the existing connection rather than telling the user to add another.

Applied B-only disclosure fix: README, PRIVACY and both skills now cover robots.txt for each inspected host, including article/image and redirect hosts. This changes the documented inspection scope consistently without claiming a performed hosted-feed diagnostic.

Applied A-only evidence fix: four fresh complete natural requests, two fresh-context runs with equal browsing access and inherited model settings, full outputs, an answer-only blind comparison and final instruction hashes are retained under tests/fix-* and tests/answers/fix-*. Requests are builder-authored; exact runtime model identifier is not exposed. Settings metadata was removed before the final blind judge read answers. Historical A/B/C/D outputs remain historical evidence. The maintained native-RSS reference and diagnosis workflow is the value claim; broad superiority is not established.

Public-link repair payload: README.md, PRIVACY.md and this build log at the exact manifest destinations in the existing public repository. Authenticated write access was verified after initial anonymous GETs confirmed both 404s. No replacement destination or deletion of required privacy fields was used. The anonymous post-publication status and content comparisons are recorded in tests/fix-publication.json and the bfix report.

Validation: JSON, YAML front matter, matching skill names, 79/78-word descriptions, local links, icon XML, identical dated references and disclosure consistency pass. Both fresh XML outputs parse and retain both items, original title values and supplied destination URLs. Complete comparison judgments and publication verification are in the fix report; neither these checks nor the document publication establish Pinterest ingestion or installed-host routing.
