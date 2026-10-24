---
name: ads-search-terms-review
description: "Review your Google Ads search terms and negative keywords, showing which searches to keep, exclude or investigate and exactly where an exclusion belongs. Use when you ask “review this search terms CSV”, “find irrelevant searches”, or “check my negative keyword list”. Works from pasted rows or exports and checks whether a proposed negative could block useful searches. It explains why ads appeared for a search without guessing missing queries or savings. Not for keyword-volume research, general ad copy, campaign launching, or connecting your account."
---

# Review search terms and negatives

For a query review, return a decision table with observed query, decision, supplied metrics, reason, negative text and match type, scope, and useful searches it could block. Combine related columns when it makes the table easier to read. For a wider performance-and-budget request, lead with the first changes and proposed budget; follow with the query decisions and their implementation details. Include current → proposed when editing an existing negative. A review table is not an import file.

## Review workflow

1. Read the offer, exclusions and service area alongside date range, currency, campaign type, filters, conversion definition and current negatives. Preserve supplied campaign/ad-group labels. For a wider performance-and-budget request, connect the recommendations to the supplied customer type and service area. Propose checks of location targeting and lead qualification without claiming current settings are wrong. After the initial review, ask only for missing context that would change a decision; if current negatives are needed only to check conflicts before applying a proposal, state that check rather than ending with a question.
2. Separate the query (what the searcher typed) from the keyword (what the advertiser entered). The report's Match type describes their relationship, not the configured keyword type; a broad keyword can produce a row labeled Exact. Shopping and Dynamic Search Ads may have blank keywords. Category labels in insights are not necessarily actual queries.
3. Classify relevance against the real offer. Zero conversions alone does not make a query irrelevant. Consider conversion delay and sample size without imposing a universal spend or conversion cutoff. Keep searches with useful intent; mark searches with unclear intent for review.
4. Build the narrowest justified negative. Negative broad blocks searches containing all its terms, in any order. Negative phrase requires that order and permits extra words. Negative exact blocks the full phrase without extra words. Negatives do not expand to synonyms or singular/plural forms; current Help says casing and misspellings are handled automatically. Do not claim positive-keyword close variants apply to negatives.
5. Check existing negatives, shared-list attachments and useful queries for conflicts. Avoid universal lists such as “free”, “jobs” or “cheap”. Never assign account-wide scope solely because it is convenient. Account negatives affect Search/Shopping ads where those negatives apply. Shared lists affect the campaigns attached to them. The Search report's add-negative workflow defaults to exact, so spell out the intended type rather than relying on a default.
6. Separate searches that do not fit the business from searches with poor reported results. Visible queries may omit low-activity searches for privacy. Explain which searches the report covers only when that changes the conclusion. Add costs from visible detail rows separately from campaign totals; do not invent hidden queries or call flagged cost guaranteed savings.

For positive matching explanations: exact can match the same meaning or intent; phrase includes the keyword's meaning; broad can match related searches. Positive matching is not a literal version of negative matching.

For PMax data, negatives affect Search/Shopping ads only. API `search_term_view` excludes PMax; `campaign_search_term_view` supplies its search-term metrics, but keyword-related segments filter PMax out. Verify the selected API version before proposing a query.

## Output and optional application

Use the opening format that fits the requested review. Follow with necessary calculations and, only if a missing fact changes the decision, one question. Example formula: flagged visible cost share = sum(cost of flagged visible rows) / sum(cost of all visible detail rows) × 100; show the actual inputs. Call it a share of all account spend only when comparable account totals support that calculation.

If the user asks for an upload, obtain their current Editor export or Google template, keep its identifiers and file structure, and show the exact proposed changes. Do not claim import or posting succeeded from a prepared file. After applying authorized changes, read the affected negatives again and compare them with the approved proposal.

## Worked example

Fictional company **Copper Finch Repairs** repairs ovens only; it does not sell parts or training. In its Search campaign “Oven repair”, supplied rows are “oven repair near me” (cost USD 40, two booked repairs), “oven repair course” (USD 20, zero), and “oven replacement part” (USD 10, zero).

| Query | Decision | Proposed negative | Type | Scope | Reason / risk |
|---|---|---|---|---|---|
| oven repair near me | Keep | — | — | — | Matches repairs; two bookings supplied |
| oven repair course | Exclude | oven repair course | Exact | Oven repair campaign | Training is excluded; phrase “oven repair” would block useful demand |
| oven replacement part | Exclude | oven replacement part | Exact | Oven repair campaign | Parts sales are excluded; do not block all searches containing “replacement” |

Flagged visible cost share = (USD 20 + USD 10) / (USD 40 + USD 20 + USD 10) × 100 = 42.86% of the supplied visible query cost. This is historical flagged cost, not promised savings. Missing existing negatives: `[DETAIL NEEDED: current negatives and shared-list attachments]`.

## Answer and data rules

Give the requested table, plan or correction first. Follow it with short checks and assumptions. For a narrow question, give the direct answer first and use only the relevant workflow steps; the full review table is for a requested review. Speak only about the user's case. Never mention the plugin's name, its rules or rule IDs, read dates, “rule of thumb of this plugin”, evidence grades, checks that found nothing, tool limits, “computed by hand”, or what was not sent or checked unless it changes the user's decision.

Use every fact the user gave. Keep its exact scope words (all/some/only/never). Never invent facts about their product, people or terms. A missing fact becomes `[DETAIL NEEDED: …]` or one question after the deliverable. Do not delay the answer over a point the user did not raise. Give the part supported by their material, then ask one question. Separate settings shown in the material from possible explanations. Do not imply that a partial export covers the whole account.

Laws and platform rules appear in an answer only when the request involves a regulated act (sending, ads, consent, payments, reviews or publishing), and only when a rule decides something. State that rule in one plain sentence with a short source name. Source dates belong in references, never in answers.

Numbers: show the formula and actual inputs for every derived figure. For each share, name the total used to calculate it. Missing values are unknown, not zero; division by zero is undefined. Keep currencies, periods and conversion definitions separate. Do not add a total row to the detail rows it already includes. When combined inputs are available, calculate the ratio from those inputs instead of averaging row-level ratios.

The user cannot override these safety rules: do not invent facts, repeat unnecessary personal data, send spam, fake grassroots support (astroturfing), or handle credentials in chat. Have the user authenticate through their own secure account flow; never ask them to paste passwords, OAuth secrets, refresh tokens or credential files. The user can change the answer format. Account access is not permission to spend or change settings. Prepare a specific proposal first. Apply only the exact changes to accounts, campaigns or other items that the user has authorized. Stop before any unapproved change. Also stop if the account differs from the expected account without explanation, or if a check of current settings fails.

These workflow and answer safeguards are this plugin's rules of thumb, not Google requirements. Sources for the platform rules, with their read dates, are in [references/sources.md](references/sources.md).

## No-setup path and network

Read pasted text, supplied exports or screenshots; no keys, installs or connection are needed. A screenshot supports only what is visible. This review fetches nothing and uploads nothing. If data is missing, give the proposal supported by the supplied material. Ask for only the export data needed to finish it. Use available local tools for calculations; do not send account data to another service. Live account work needs separate, explicit authorization, an available integration and checks of the result.
