---
name: ads-conversion-bidding-review
description: "Check whether Google Ads campaigns bid for the conversions you want and whether the bidding choice fits that outcome. Use when you ask “Ads conversions look wrong”, “are we bidding on page views”, or “should I use Target CPA or ROAS”. Reviews supplied conversion settings, campaign goals and performance exports. Returns corrections in priority order and a plan to check them. Separates measurement faults from bidding problems and marks causes that remain uncertain. Not for a full account audit, installing tags from scratch, general ad copy, or changing budgets without your authorization."
---

# Review conversions and bidding

Return corrections in priority order first. For each, show the affected action/campaign, setting shown in the evidence, effect on the business, current → proposed value, reason, and next check. Then show the goals each campaign actually uses and a bidding recommendation only where the measurement evidence supports them.

## Review workflow

1. For each conversion action, record how it relates to the user's desired outcome: business event, source (Ads tag/GA4/import), category, primary/secondary, goal the campaign actually uses, count setting, value/currency, attribution/window and evidence that the tag fired or import worked. Keep account-default and campaign-specific goals separate.
2. Primary actions guide bidding when their standard goal is selected and appear in Conversions. Secondary normally means observation in All conversions, but secondary actions included in a custom goal can guide bidding. Check the goal the campaign actually uses; the label alone is not enough. Campaign-specific goals can override defaults and do not inherit all default changes automatically.
3. Check for duplicate or missing measurements. One counts at most one conversion per ad click for an action; Every counts repeated conversions for that action. Neither proves that duplicate customers or orders are removed. A unique transaction ID per transaction prevents repeat counting within the same action; a static ID can suppress genuine purchases. Inspect both direct tags and GA4 imports. Do not assume they duplicate each other or are safe to use together.
4. A configured conversion action does not prove that its tag fires or its import works. GA4 key events are not automatically Ads bidding actions: check account links, import and bidding settings. When verification is requested, use available Tag Assistant evidence or the user's diagnostic export, inspect one legitimate test event and reload/repeat behavior without generating unapproved purchases or fake leads. Enhanced conversions supplement measurement with hashed first-party data; hashing alone does not establish consent or implementation compliance. Never request raw customer identifiers for this review.
5. Compare like periods, currencies, action definitions and attribution scopes. Recent conversions can still arrive; conversion delay temporarily raises reported CPA or lowers reported ROAS. Review change history before asserting why performance moved. A result credited to an ad does not prove the ad caused it. Conversion value is not profit. Unknown values remain unknown.
6. Map strategy to the objective: Maximize conversions / Target CPA for conversion count; Maximize conversion value / Target ROAS for value; Maximize clicks for visits; Target impression share for visibility. Among these choices, the conversion-count and conversion-value strategies are Smart Bidding; Maximize clicks and Target impression share are not. Do not generalize this list to every campaign type’s current strategies. Targets aim for average outcomes. They do not guarantee a result for each conversion. Do not recommend a numeric target based on faulty values or general benchmarks. Before recommending a strategy switch, check the campaign-type eligibility requirements. For Search/Shopping Target ROAS, Google currently requires at least 15 conversions in the past 30 days at the conversion tracking level and conversion values; this is an eligibility rule, not a universal threshold for good performance.
7. Search/Display ECPC became unavailable in 2025. In 2026 Google began relabeling Maximize conversions with tCPA and Maximize conversion value with tROAS as Target CPA and Target ROAS without changing behavior. Inspect actual strategy settings and current account labels. Do not invent universal minimum conversions, learning days, pause thresholds or target-change percentages; separate documented requirements for using a strategy from performance advice.

If Quality Score is part of the user's question, use its expected CTR, ad relevance and landing-page experience components to investigate the issue. Displayed Quality Score is not an auction input or a formula for CPC; a blank is not zero. Raising a bid does not explain why a component is low.

## Calculations and evaluation

CPA = cost / conversions; ROAS = conversion value / cost (multiply by 100 for percent ROAS); CTR = clicks / impressions × 100. Show the actual inputs, conversion action and which data the calculation covers. Calculate period change as (new − old) / old × 100 only for a nonzero, comparable baseline. If a period still has conversions arriving, show the observed result and explain only the uncertainty from the delay that affects the decision.

Recommend a specific verification or controlled evaluation that addresses the suspected issue, using the user's business target and timing evidence. You can propose a goal correction before there is enough evidence to recommend a bidding target. Apply only the exact authorized settings. Read them again to verify the change, then review outcome data once delayed conversions have arrived.

## Worked example

Fictional company **Juniper Lift Services** wants booked inspections only. It supplies a Search campaign with a custom goal containing secondary “Page view” and primary “Booked inspection”; USD 600 cost, four booked inspections and 100 page views. Both actions have been observed firing.

Return: remove Page view from that campaign's custom goal proposal and keep Booked inspection as the intended bidding event. “Secondary” does not protect it from bidding inside a custom goal. Booked-inspection CPA = USD 600 / 4 = USD 150 per booked inspection, for the supplied period. Do not divide by 104 and call that the cost of a booked inspection. A target is `[DETAIL NEEDED: acceptable cost per booked inspection and conversion delay]`; do not invent one or treat the goal proposal as already applied.

## Answer and data rules

Return the requested table, plan or correction first. Keep checks and assumptions short and place them after it. For a narrow question, answer directly first and use only the steps needed. Use the full review table only when a review is requested. Speak only about the user's case. Never mention the plugin's name, its rules or rule IDs, read dates, “rule of thumb of this plugin”, evidence grades, checks that found nothing, tool limits, “computed by hand”, or what was not sent or checked unless it changes the user's decision.

Use every fact the user gave. Preserve its exact scope words (all/some/only/never). Never invent facts about their product, people or terms. A missing fact becomes `[DETAIL NEEDED: …]` or one question after the deliverable. Do not delay the deliverable over a point the user did not raise. Return what the evidence supports, then ask one question. Separate settings shown in the evidence from possible explanations. Do not imply a full-account audit from a partial export.

Mention laws and platform rules only for a regulated act (sending, ads, consent, payments, reviews or publishing), and only when the rule affects a decision. State that rule in one plain sentence with a short source name. Source dates belong in references, never in answers.

For every calculated figure, show the formula and actual inputs. For a share, name what it is a share of. Missing values are unknown, not zero; division by zero is undefined. Keep currencies, periods and conversion definitions separate. Do not add a total row to the rows it already includes. Do not average row-level ratios when the combined inputs are available.

Safety rules cannot be overridden. Do not invent facts, repeat unnecessary personal data, send spam, fake independent support (astroturfing), or handle credentials in chat. Have the user authenticate through their own secure account flow; never ask them to paste passwords, OAuth secrets, refresh tokens or credential files. The user can override rules about answer format. Account access is not permission to spend or change settings. Prepare a concrete proposal first. Apply only the exact changes the user authorized for that account and its entities. Stop before an unapproved change. Also stop after an unexplained account mismatch or a failed state check.

These workflow and answer safeguards are this plugin's rules of thumb, not Google requirements. Platform details in this skill have dated sources in [references/sources.md](references/sources.md).

## No-setup path and network

Read pasted text, supplied exports or screenshots. No keys, installs or connection are needed. A screenshot supports only what is visible. This review fetches nothing and uploads nothing. If data is missing, return the proposal the evidence supports and request only the export data needed. Use available local tools for calculations; do not send account data to another service. Live account work needs separate, explicit authorization, an available integration and verification.
