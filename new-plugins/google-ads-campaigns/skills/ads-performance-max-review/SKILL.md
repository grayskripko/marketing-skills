---
name: ads-performance-max-review
description: "Review your Google Ads Performance Max campaign against your sales or lead goal, including brand searches, landing pages, asset groups and conversion settings. Use when you ask “review my PMax”, “stop brand traffic in Performance Max”, or “why is PMax sending visitors to this page”. Returns proposed controls with their scope, problems with assets or destination pages, and the evidence needed to assess them. Works from pasted settings and exports without a connection. Not for building a conventional Search keyword campaign, general ad copy, guarantees of added sales, or applying account changes automatically."
---

# Review Performance Max

Return a prioritized table: affected campaign/asset group, setting or report row showing the issue, issue, current → proposed control, affected channels and scope, business reason and how to check the result. Separate issues shown in the material from possible causes.

## Review workflow

1. Identify the objective, conversion goals actually used, values, reporting period, assets/groups, product-feed details if supplied, desired treatment of brand searches, supplied landing pages and URL restrictions. PMax works toward goals across multiple channels, including Search, YouTube, Display, Discover, Gmail and Maps. It uses asset groups, not Search ad groups with conventional keyword targeting.
2. Check which conversion goals actually guide bidding. Primary actions guide bidding when their standard goal is selected; secondary actions in a custom goal can also guide bidding. Before judging performance, check campaign-specific goal settings, paths that may count the same conversion twice, whether values are reliable and delays in recent conversion reporting. Reported revenue is not profit.
3. Review themed asset groups and supplied text/images/video/feed against the actual offer and pages. Never invent product claims or promise an asset causes a sales lift. Audience signals are suggestions; they do not restrict delivery to those audiences. Search themes are not exact-match targeting restrictions.
4. Inspect final URL expansion and creative settings. Expansion can choose a different relevant page and generate matching text. Identify the actual setting responsible for a supplied unwanted destination before proposing URL exclusions or disabling expansion. Explain the tradeoff: fewer possible destination pages, with no guarantee of higher returns.
5. For unwanted queries, distinguish campaign negatives, account negatives and brand exclusions. PMax campaign/account negatives affect Search and Shopping only; do not imply an all-channel content block. Brand exclusions recognize brand variants more broadly than ordinary negatives. Use campaign scope for a PMax-only brand issue. For retail campaigns with product feeds, Google documents applying brand exclusions to Search text ads only while keeping branded Shopping traffic eligible; inspect that setting in the current account before proposing the exact change. A normal campaign negative is not a Search-only substitute because it also affects Shopping. Never silently broaden the exclusion to the whole account.
6. When drafting ordinary negatives, broad requires all words in any order, phrase requires the same order with extra words allowed, and exact excludes the full phrase without extra words. They do not expand to synonyms or singular/plural forms. Check valuable intent and existing lists; no automatic zero-conversion cutoff.
7. Inspect Search overlap without claiming Search always wins. An identical exact Search keyword has priority if it can serve. Identical phrase/broad keywords and search themes share priority; relevance/Ad Rank decides other cases. Whether the keyword can serve and whether budget is available matter. A keyword's presence alone does not prove it can serve.
8. Use the user's available channel, search-term, asset-group, product and destination evidence. Available reports vary by account, interface and version. API `search_term_view` excludes PMax; use `campaign_search_term_view` for its search-term metrics, without keyword-related segments. Do not interpret an empty incompatible query as no traffic. Search-term exports omit some queries; insight category labels are not necessarily the searches that triggered ads.

## Evaluation and optional edits

Conversions credited to PMax do not prove it added sales or took sales from Search. If the user asks what caused a result, propose a test of a specific explanation or a suitable controlled lift measurement. Compare similar periods that have allowed time for conversions to be reported. Do not claim one learning period applies to every campaign or promise savings. Show the inputs and denominator for every calculated ratio.

For exact changes the user has authorized, first list the current and proposed settings for each account/campaign/asset group. Check current settings, apply the changes with an available integration, then read the changed settings again. A draft proposal does not prove a change was applied. If only exports are available, give the operator steps and specify the export needed afterward to check the change.

## Worked example

Fictional company **Willow Thread Supply** sells yarn only. It supplies a PMax campaign with final URL expansion enabled and a destination report containing its careers page; it wants only product pages. It also gives an audience signal labeled “Knitting enthusiasts”.

Return a campaign-scoped proposal to exclude the observed careers URL using the supported current URL controls, or disable expansion if the account's controls cannot enforce the product-only requirement. Inspect other expansion destinations before claiming all traffic is now product-only. Keep the audience signal as a suggestion; do not call it a delivery restriction. No supplied conversion or cost data means no numerical sales-lift claim. After the proposal, ask for the current URL-control export needed to choose the exact change.

## Answer and data rules

Give the requested table, plan or correction first. Follow it with short checks and assumptions. For a narrow question, give the direct answer first and use only the relevant workflow steps; the full review table is for a requested review. Speak only about the user's case. Never mention the plugin's name, its rules or rule IDs, read dates, “rule of thumb of this plugin”, evidence grades, checks that found nothing, tool limits, “computed by hand”, or what was not sent or checked unless it changes the user's decision.

Use every fact the user gave. Keep its exact scope words (all/some/only/never). Never invent facts about their product, people or terms. A missing fact becomes `[DETAIL NEEDED: …]` or one question after the deliverable. Do not delay the answer over a point the user did not raise. Give the part supported by their material, then ask one question. Separate settings shown in the material from possible explanations. Do not imply that a partial export covers the whole account.

Laws and platform rules appear in an answer only when the request involves a regulated act (sending, ads, consent, payments, reviews or publishing), and only when a rule decides something. State that rule in one plain sentence with a short source name. Source dates belong in references, never in answers.

Numbers: show the formula and actual inputs for every derived figure. For each share, name the total used to calculate it. Missing values are unknown, not zero; division by zero is undefined. Keep currencies, periods and conversion definitions separate. Do not add a total row to the detail rows it already includes. When combined inputs are available, calculate the ratio from those inputs instead of averaging row-level ratios.

The user cannot override these safety rules: do not invent facts, repeat unnecessary personal data, send spam, fake grassroots support (astroturfing), or handle credentials in chat. Have the user authenticate through their own secure account flow; never ask them to paste passwords, OAuth secrets, refresh tokens or credential files. The user can change the answer format. Account access is not permission to spend or change settings. Prepare a specific proposal first. Apply only the exact changes to accounts, campaigns or other items that the user has authorized. Stop before any unapproved change. Also stop if the account differs from the expected account without explanation, or if a check of current settings fails.

These workflow and answer safeguards are this plugin's rules of thumb, not Google requirements. Sources for the platform rules, with their read dates, are in [references/sources.md](references/sources.md).

## No-setup path and network

Read pasted text, supplied exports or screenshots; no keys, installs or connection are needed. A screenshot supports only what is visible. This review fetches nothing and uploads nothing. If data is missing, give the proposal supported by the supplied material. Ask for only the export data needed to finish it. Use available local tools for calculations; do not send account data to another service. Live account work needs separate, explicit authorization, an available integration and checks of the result.
