# Verified knowledge register

Verified 2026-10-11 for the planned 2026-10-21 submission. Reopen the two supplied Google Help pages and channel definitions before submission; record changed rules rather than assigning a future read date. Google Help exposes no absolute revision date in the retrieved articles.

## URL builders

https://support.google.com/analytics/answer/10917952?hl=en — read 2026-10-11. Exact URL returned HTTP 200 through direct retrieval after web-reader timeouts; current article title: URL builders: Collect campaign data with custom URLs.

Values are case-sensitive. Google recommends source, medium and campaign together, plus all relevant fields, especially ID and source platform. ID should match campaign-data upload IDs. Lowercase is a best-practice recommendation, not permission to rename established identities. Creative format and marketing tactic are described as not currently reported. UTM parameters are omitted from Landing page + query string and Page path + query string; Page location retains them. Parameter order is flexible. The article now includes a UTM best-practices table; campaign naming should match the exact campaign name.

## Manual and auto tagging

https://support.google.com/analytics/answer/11242870?hl=en — read 2026-10-11; loaded in web reader.

With both methods, auto-tagging supplies source, medium and other classification dimensions; manual content and term still supply their manual dimensions. If GCLID/DCLID cannot be used and any UTM exists, cross-channel values derive exclusively from UTMs. Incomplete fields can therefore produce (not set). This is conditional, not a finding that a supplied click ID failed. Linked platform and click-ID presence alone do not establish usable integration. Help explicitly says creative format and marketing tactic are not currently reported.

## Parameter-to-dimension map

https://developers.google.com/analytics/devguides/reporting/data/v1/api-schema — read 2026-10-11; loaded in web reader. Session mappings below are confirmed by API schema. Equivalent first-user and key-event manual fields are separate scopes, not interchangeable report columns.

| URL parameter | Session API dimension | Meaning |
|---|---|---|
| utm_id | sessionManualCampaignId | campaign ID |
| utm_campaign | sessionManualCampaignName | campaign name |
| utm_source | sessionManualSource | referrer/source |
| utm_medium | sessionManualMedium | medium |
| utm_term | sessionManualTerm | term |
| utm_content | sessionManualAdContent | ad content |
| utm_source_platform | sessionManualSourcePlatform | directing platform |

Documentation conflicts: Help's manual table places Session manual campaign ID on the utm_campaign row; the API schema explicitly assigns that ID to utm_id. Use the API mappings above. The schema also lists manual creative-format and marketing-tactic fields while both Help pages say those parameters are not currently reported. Existence of a schema field does not demonstrate populated values in a property. Preserve supplied values; request an actual export if reporting of either field decides the task.

## Default channel rules and error meanings

https://support.google.com/analytics/answer/9756891?hl=en — read 2026-10-11; loaded in web reader.

Definitions are case-insensitive; default channel groups cannot be edited. Manual Email matches email/e-mail/e_mail/e mail in source or medium. Referral uses referral, app or link as medium. Paid Social requires a source matching Google's social-site list and a medium matching ^(.*cp.*|ppc|retargeting|paid.*)$. Display media include display, banner, expandable, interstitial and cpm. These examples are not a complete ordered classifier. Unassigned means no channel rule matched; (other) is an aggregated row from cardinality limits. Neither proves a malformed URL. Missing source-list or platform evidence leaves a channel prediction conditional.

## URL parsing and serialization

https://url.spec.whatwg.org/#urlencoded-parsing — read 2026-10-11; loaded in web reader. Living Standard header: Last Updated 7 October 2026.

Query and fragment are distinct URL components. Form parsing splits on ampersands, then the first equals sign, replaces raw plus with space and percent-decodes UTF-8 once. Repeated keys remain separate tuples. Encoded plus (%2B) means a literal plus; %2520 becomes literal %20 after one pass, not space. Serializer encodes each field, not the entire URL. Invalid percent escapes can survive parsing; flag them without claiming every browser rejects them. This standard describes URL behavior, not GA4 duplicate-key precedence or custom fragment collection.

## Personal information in campaign URLs

https://support.google.com/analytics/answer/6366371?hl=en — read 2026-10-11; loaded in web reader and direct HTTP 200.

Google's policy excludes personally identifiable information from Analytics data. Both path and query parameters can expose it; campaign fields must not contain emails, personal phone numbers or similar identifiers. Redaction settings are not a substitute for a safe URL proposal. Use row references and masked samples rather than repeating personal information or credentials.

## Governance decisions (authored rules of thumb)

These are workflow conventions, not Google requirements: protect original rows and historical campaign identities; use unique assigned aliases within supplied scope; include owner/dates when supplied and request them only for a deciding action; treat unknown lifecycle as protected; do not infer a missing ID or collapse collisions; preserve unrelated URL bytes and click IDs; withhold a deployable proposal for signed URLs or unresolved templates; never choose duplicate-key precedence without evidence. A team's supplied approved naming rules decide vocabulary. Proposed future standards stay visibly unapproved until accepted.

## Fix verification — 2026-10-11

All six official destinations above reopened during bfix. API session ID/name mapping, conditional unusable-click-ID fallback, Help/API field conflict, exact Paid Social medium expression and report-field omissions were checked again. Ordinary unexplained parameters and command-like labels are preserved by an authored workflow convention; they are not Google approval requirements.
