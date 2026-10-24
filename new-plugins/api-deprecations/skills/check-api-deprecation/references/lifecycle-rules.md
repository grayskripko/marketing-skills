# Lifecycle source register

Read 2026-10-11. Verify changing provider policy again near the planned 2026-10-22 submission. These are paraphrased decision rules, not copied RFC examples. Runtime uses this bundled text and supplied exports; it fetches nothing.

## RFC 9745 — March 2025, Standards Track

https://www.rfc-editor.org/rfc/rfc9745.html

Sections 2.1–2.2: Deprecation is an Item whose value is a Structured Field Date; default scope is the responding resource, with documented wider scope possible. Sections 3–3.1: deprecation links expose policy or migration information and can precede an announcement. Section 4: sunset must not be earlier than deprecation. Sections 5 and 7: deprecation itself changes no behavior, but clients must not assume behavior remains unchanged after the date. A header is a hint, not a service guarantee.

Current-status page: https://www.rfc-editor.org/info/rfc9745/
Errata search: https://errata.rfc-editor.org/search/?rfc_number=9745 — opened; returned no matching errata.

## RFC 8594 — May 2019, Informational

https://www.rfc-editor.org/rfc/rfc8594.html

Sections 1.4 and 3: Sunset describes expected unavailability, not the first stage of deprecation. Value is one HTTP-date, normally future; a past timestamp suggests possible unavailability now. It is a hint, without an availability guarantee or prescribed post-retirement status. Section 4: it does not control HTTP caching. Sections 5–6: default scope is the responding resource; wider scope requires documentation; sunset links can describe policy, retirement and mitigation. No universal minimum notice period is specified.

Current-status page: https://www.rfc-editor.org/info/rfc8594/
Errata search: https://errata.rfc-editor.org/search/?rfc_number=8594 — opened; returned no matching errata. The section 3 sample has a weekday inconsistent with its date; generate your own validated date.

## RFC 9651 — September 2024, Standards Track

https://www.rfc-editor.org/rfc/rfc9651.html

Sections 3.1, 3.3.1, 3.3.7 and 4.2: Item parameters are permitted; Date serialization is @ plus integer seconds from the Unix epoch, with possible negative values and no leap-second counting. Date syntax is @, an optional minus sign (no plus), and 1–15 ASCII digits; the inclusive integer range is −999999999999999 to 999999999999999. Parsing is specified in §§4.2.4 and 4.2.9 (not §4.2.8, which parses Booleans). A quoted string, Boolean or multiple comma-separated Items does not become a Date. Syntactically representable dates may exceed the local date library's range; conversion failure is not automatically a protocol error. This RFC replaces RFC 8941.

## RFC 9110 — June 2022, Standards Track

https://www.rfc-editor.org/rfc/rfc9110.html#section-5.6.7

Section 5.6.7: recipients accept IMF-fixdate and the two obsolete HTTP-date forms, while senders generate IMF-fixdate. GMT is the literal zone in IMF-fixdate; UTC prose and HTTP-date wire syntax differ. Recompute the weekday instead of copying an illustrative header, including RFC 9745's UTC example.

## RFC 8288 — October 2017, Standards Track

https://www.rfc-editor.org/rfc/rfc8288.html

Sections 3.1–3.3: relative link targets resolve against the message context, not a body base URI. The anchor parameter overrides link context. An application unable to honor anchor ignores that entire link, not just the anchor. Relation values identify the relationship; rel may occur only once in a link-value. This RFC replaces RFC 5988.

## GitHub REST API versions — living provider documentation

https://docs.github.com/en/rest/about-the-rest-api/api-versions

Read 2026-10-11; the page has no publication date displayed. Applies to GitHub REST, not arbitrary APIs or GitHub GraphQL. The standard previous-version support window is at least 24 months after the next version's release. The supported table lists 2026-03-10 with no scheduled end and 2022-11-28 ending March 10, 2028. The documented omitted-header default is 2022-11-28; after its retirement unversioned requests use the next oldest supported version. Explicitly selecting a retired version returns 410 Gone. GitHub documents Deprecation as HTTP-date, differing from RFC 9745's Date syntax; report the standards mismatch without changing the provider's attributed behavior. Security/reliability and low-usage exceptions can fall outside standard versioning. Recheck a newer supplied provider export before using this snapshot.

## Editorial decisions

Choose a conflict table only for a requested comparison, a checklist only for requested migration steps, and missing-detail markers only where an editable draft needs them. Otherwise answer the question directly. These are output options, not HTTP requirements. Calendar arithmetic comes from the supplied policy; neither RFC invents a user's notice window, approval date, deadline or successor compatibility.
