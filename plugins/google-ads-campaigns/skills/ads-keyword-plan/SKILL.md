---
name: ads-keyword-plan
description: "Plan Google Ads Search campaign themes and keywords from your offer, landing pages or Keyword Planner export. Use when you ask “group these keywords”, “find keywords for my service”, or “plan my Search campaigns”. Returns a campaign and ad-group map, suggested match types, landing pages and missing metrics. Starts from a brief without an account connection; actual search volume and forecasts need supplied Planner data. Keeps keyword ideas separate from demand estimates. Not for SEO research, general ad copy, Performance Max review, or launching paid campaigns."
---

# Plan Search keywords and campaign structure

Return the campaign/ad-group map and keyword table first: intent, keyword, proposed match type, landing page, relevance reason, and supplied historical or forecast metrics with their settings. Mark volume, CPC and forecasts as unknown when no evidence supports them. Give briefs for ad messages only when they help the requested plan; do not broaden a keyword request into full ad-copy production.

## Planning workflow

1. Extract the actual products/services, customer intent, exclusions, geography, language, supplied pages, who controls the budget and existing campaigns. Do not invent URLs, service areas, offers, proof or prices. A brief alone supports a plan based on relevance. It does not support ranking keywords by measured demand.
2. Treat seed ideas as suggestions whose relevance still needs checking. Remove ideas that contradict the offer. Group by intent and page, instead of listing every word combination or meeting an arbitrary keyword quota.
3. Use account → campaign → ad group for Search. Separate campaigns when settings such as budgets or locations need to differ; group related keywords and ads within ad groups. Do not prescribe one campaign per keyword. Explain the reason for each separation.
4. Suggest match types explicitly: `[keyword]` exact, `"keyword"` phrase, unquoted broad. Positive exact covers the same meaning or intent, phrase includes the keyword's meaning, and broad covers related searches. Google advises Smart Bidding with broad match; check the goals the campaign actually uses and its measurement before recommending expansion. Do not promise that broad match improves this account.
5. Preserve Planner geography, language setting, Search Network, historical period, currency, and forecast budget/bid/match settings. Average monthly searches include close variants and depend on location/network/period; volumes are rounded. The entered match type does not change historical search statistics. It does change forecasts. Competition measures competition among advertisers. It does not measure how hard it is to rank in organic search. Historical top-of-page bid ranges do not guarantee the CPC you will pay. Do not sum overlapping ideas as unique demand or turn forecasts into promised outcomes.
6. Draft candidate negatives only from the stated offer exclusions. Specify where each negative applies and its match type. Check whether it could exclude useful searches. Negative broad requires all terms in any order, phrase requires that order with extra words allowed, and exact excludes the whole phrase without extra words. Negatives do not cover synonyms or singular/plural forms as positive matches do. Flag unclear exclusions for review.

## Getting Planner evidence when requested

Without setup: analyze pasted keywords or an existing export immediately. Do not require paid ads to review it. If the user wants new Planner metrics, walk them through their own Google Ads account → Tools → Planning → Keyword Planner (or use the UI search). Verify the selected account and use Discover new keywords or Get search volume and forecasts for the intended task. Google requires completed account setup including billing information for basic Planner features; do not promise anonymous access or a universal spend threshold for precise numbers.

Apply location, language, network and dates; verify the displayed settings before downloading. If a saved-plan control is disabled, open a fresh Planner flow rather than repeat failed clicks. With an available authorized browser, check screenshots after meaningful changes; otherwise give precise UI steps. Keep login and billing entry with the user. Planning through the API is a separate optional route requiring Cloud-project access, OAuth, a supported client and planning-service permission; Explorer does not unlock planning. Never request secrets in chat.

## Output

Return the plan based on relevance or supplied data first. For a first-month plan, include the operating decisions the user needs: purchase tracking, a proposed starting bidding approach, spend monitoring, and when to reassess the test. If shipping is restricted, distinguish ad targeting from checkout delivery checks; targeting alone does not enforce delivery eligibility. Then list missing settings that affect the decision. When the user requests a budget split without performance evidence, give a clearly labelled starting test allocation and its rationale, not a claim that it is optimal. Show the formula and inputs. Preserve which campaigns or ad groups the user's budget covers. Prepare an import file only with the destination's current template. A draft map does not authorize launch.

## Worked example

Fictional company **Harbor Kiln Studio** offers only pottery classes for adults in Bristol. It supplies a classes page, a private-group page and one shared budget, but no Planner metrics.

Propose one Bristol Search campaign: “Adult pottery classes” ad group → classes page, with `[adult pottery classes]` and `"pottery classes for adults"`; “Private group pottery” → private-group page, with `"private pottery class"`. Both use the supplied shared budget; the user gave no setting that requires a separate campaign. All volumes, CPCs and forecasts remain unknown. Keep both ad groups adult-only because that scope is explicit. Mark children's-class intent for exclusion review; do not invent a city-specific search volume. Ask after the plan for Planner settings/export only if ranking by measured demand is needed.

## Answer and data rules

Return the requested table, plan or correction first. Keep checks and assumptions short and place them after it. For a narrow question, answer directly first and use only the steps needed. Use the full review table only when a review is requested. Speak only about the user's case. Never mention the plugin's name, its rules or rule IDs, read dates, “rule of thumb of this plugin”, evidence grades, checks that found nothing, tool limits, “computed by hand”, or what was not sent or checked unless it changes the user's decision.

Use every fact the user gave. Preserve its exact scope words (all/some/only/never). Never invent facts about their product, people or terms. A missing fact becomes `[DETAIL NEEDED: …]` or one question after the deliverable. Do not delay the deliverable over a point the user did not raise. Return what the evidence supports, then ask one question. Separate settings shown in the evidence from possible explanations. Do not imply a full-account audit from a partial export.

Mention laws and platform rules only for a regulated act (sending, ads, consent, payments, reviews or publishing), and only when the rule affects a decision. State that rule in one plain sentence with a short source name. Source dates belong in references, never in answers.

For every calculated figure, show the formula and actual inputs. For a share, name what it is a share of. Missing values are unknown, not zero; division by zero is undefined. Keep currencies, periods and conversion definitions separate. Do not add a total row to the rows it already includes. Do not average row-level ratios when the combined inputs are available.

Safety rules cannot be overridden. Do not invent facts, repeat unnecessary personal data, send spam, fake independent support (astroturfing), or handle credentials in chat. Have the user authenticate through their own secure account flow; never ask them to paste passwords, OAuth secrets, refresh tokens or credential files. The user can override rules about answer format. Account access is not permission to spend or change settings. Prepare a concrete proposal first. Apply only the exact changes the user authorized for that account and its entities. Stop before an unapproved change. Also stop after an unexplained account mismatch or a failed state check.

These workflow and answer safeguards are this plugin's rules of thumb, not Google requirements. Platform details in this skill have dated sources in [references/sources.md](references/sources.md).

## No-setup path and network

Read pasted text, supplied exports or screenshots. No keys, installs or connection are needed. A screenshot supports only what is visible. This review fetches nothing and uploads nothing. If data is missing, return the proposal the evidence supports and request only the export data needed. Use available local tools for calculations; do not send account data to another service. Live account work needs separate, explicit authorization, an available integration and verification.
