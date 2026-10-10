---
name: ads-access-setup
description: "Set up a way to read Google Ads data or prepare bulk changes through exports, the browser, Editor, Scripts, the API or an MCP connection. Use when you ask “connect my account”, “do I need a developer token”, or “can we use exports instead”. Returns setup steps, what is still needed and checks that show whether the connection works. Keeps exports available without setup and explains permissions, planning access and what previews can change. Not for an account performance audit, providing a connector, unrelated cloud administration, or authorizing advertising spend."
---

# Set up access and bulk workflows

Return the chosen route, setup steps, exactly what is still needed, and evidence that it works first. If the user explicitly requests API or Editor setup, follow that request. Offer exports as a fallback; do not require them first. Explain unavailable actions only if they block the requested setup. Do not describe the package in the answer.

## Choose the route

| Need | Route | What it requires / limit |
|---|---|---|
| One-time analysis | Pasted rows or CSV exports | No installation, keys or agent account access; dated/filtered data can be incomplete |
| View settings or prepare UI edits | Authorized browser/UI | Available browser capability and user login; verify account and visible state |
| Offline bulk proposal | Google Ads Editor | User installation and account download; import differs from posting |
| In-account recurring check | Ads Scripts | JavaScript and per-script authorization; Preview has external side effects |
| Custom reporting/planning/app | Google Ads API | Cloud project access, OAuth/account rights and supported client; some features need a higher access level |
| Agent reporting tools | MCP over API | A separately installed server plus the API prerequisites; inspect its tools/data sharing |

Without setup: ask for the specific report or settings export and analyze it immediately. For search terms, use Campaigns → Insights and reports → Search terms, set dates/filters, add campaign/ad group, keyword, match type and available cost/conversion columns, then Download. Navigation may differ; use the UI search when needed. For other jobs, request only the settings and metrics needed. Redact customer identifiers and credentials while keeping entity labels needed to identify what the data covers.

## API setup the agent can walk through

1. Confirm the requested operations, whether the account is production or test, any existing Cloud project/client, and account or manager access. Do not repeat IDs in the answer unless needed. The user handles Google login and permission grants securely.
2. Compare current official migration and access guidance with the installed client before changing configuration. Google's current migration documentation says developer tokens were retired in September 2026 and access is assigned to the Cloud project that owns the OAuth credentials. Token headers are optional/ignored during that documented transition; old API Center signup instructions and some summaries conflict. Do not default to setup instructions from before this token change. The separate App Conversion Tracking API retains a token exception. See the dated references; recheck the linked official guidance for the chosen setup.
3. In the selected Cloud project, enable Google Ads API and inspect its Google Ads API Overview access level. Test cannot query production. Explorer permits production reporting but restricts planning services, including KeywordPlanIdeaService; planning needs appropriate Basic/Standard access. New Basic/Standard applications require brand verification; Standard requires manual review. Never promise approval or a review time.
4. Set up the appropriate OAuth flow and Ads account permissions. Follow the current official client-library instructions. For user OAuth, the user configures the consent screen, client and redirect flow and grants access. Keep client secrets/refresh tokens in a local secret store or protected configuration outside version control; redact logs. Basic-access brand verification can require External/In production consent settings, including for an internal tool: explain this change in who can access the app before the user selects it. Cloud approval alone does not grant advertiser access.
5. Install a supported official Google Ads client library in an isolated environment appropriate to the user's language. Check version-specific configuration, instead of hardcoding an old developer-token field. The operating customer ID selects the advertiser; when routing through a manager, `login-customer-id` selects that manager without hyphens. Do not swap the two.
6. Prove readiness with a minimal read-only production call against the intended advertiser, using GAQL and GoogleAdsService Search/SearchStream. For example, validate version support then request `SELECT customer.descriptive_name, customer.currency_code FROM customer LIMIT 1`. Compare the returned identity/currency to the intended account privately. Record success or a redacted actual error. A successful test-account call or approved-looking Console status is not proof of production access; documented migration issues can cause failures after upgrades. Do not change billing or Cloud IAM blindly as an error workaround.
7. For planning, verify the required service works separately. For changes, verify supported `validate_only` behavior on the concrete request and inspect errors before applying the exact authorized changes. A partially failed request may still apply some operations. Inspect each result and read the current state again before retrying. Validation checks API validity, not business suitability or permission to spend.

## Other setup routes

**Editor:** install the official desktop Editor, sign in securely, download the intended account and export the relevant entities. Build from that schema or a current Google template; preserve IDs and original-value columns. Each row describes one entity. Show before/after values, import offline, inspect defaults and Check changes. Post only the exact authorized changes. Then fetch the current state and compare it with the proposal. Never say an analysis table is ready to import until its columns and format have been validated.

**Scripts:** open Tools → Bulk actions → Scripts or search for Scripts. Prepare a read-only report with clear limits first, inspect code and external destinations, let the user authorize the script, then Preview and inspect logs. Preview prevents AdsApp changes, but mail, spreadsheet and other services still execute: disable their sends/writes explicitly for a no-send check. Generic campaign selectors omit some campaign types, so check which campaign types the report covers. Timeouts preserve completed changes; use batches that can safely be repeated and progress logs, inspect applied results before retrying, and schedule only after verified execution and user authorization. Setting up ordinary Ads Scripts is separate from setting up an external Ads API app.

**MCP:** if requested, inspect the official `googleads/google-ads-mcp` repository's current installation/configuration guide and tools it actually provides. It documents retrieval/customer/metadata tools; do not promise account changes from that tool list. Install only when authorized, use its supported runtime and secure OAuth configuration, then verify the intended account with a read-only tool call. MCP does not bypass API access requirements or planning restrictions. Account data reaches the agent/LLM; the official server documents a usage-data header. Inspect the safety controls of community servers that can write. A README claim or an approval flag supplied by an agent is not enough.

## Network and stopping conditions

For export-only work, fetch nothing. Fetch public documents only from official documentation URLs listed in references or supplied by the user, plus their robots.txt. Follow only official documentation links needed for the chosen setup, respect paths blocked by robots.txt, and use pasted text if fetching fails. Include no account data in documentation requests. For separately authorized live setup, exchange only the account, authentication and report data needed with the chosen Google UI/API/OAuth endpoints. The MCP operator/runtime also receives data. Explain those destinations before connection. No telemetry is added by these instructions. Do not send report content to extra services.

When a state check fails, inspect the current state before retrying. Never repeat an uncertain write or claim readiness without actual evidence. If execution is unavailable, deliver the setup plan and precise blocker; do not manufacture successful tests. For a concrete change that affects spend, make the proposed changes ready to review before requesting any missing authorization.

## Worked example

Fictional company **Ridgeglass Fixtures** asks whether it needs API access to review a one-time search-term CSV. Return the export route: preserve dates, filters, campaign/ad-group labels and relevant metrics; no API signup is needed for that analysis. If it later explicitly asks for monthly API reports, walk through Cloud project access, secure OAuth and a production read. Do not ask for a developer token from an old tutorial or call the integration connected from a Console screenshot.

## Answer and data rules

Return the requested table, plan or correction first. Keep checks and assumptions short and place them after it. For a narrow question, answer directly first and use only the steps needed. Use the full review table only when a review is requested. Speak only about the user's case. Never mention the plugin's name, its rules or rule IDs, read dates, “rule of thumb of this plugin”, evidence grades, checks that found nothing, tool limits, “computed by hand”, or what was not sent or checked unless it changes the user's decision.

Use every fact the user gave. Preserve its exact scope words (all/some/only/never). Never invent facts about their product, people or terms. A missing fact becomes `[DETAIL NEEDED: …]` or one question after the deliverable. Do not delay the deliverable over a point the user did not raise. Return what the evidence supports, then ask one question. Separate settings shown in the evidence from possible explanations. Do not imply a full-account audit from a partial export.

Mention laws and platform rules only for a regulated act (sending, ads, consent, payments, reviews or publishing), and only when the rule affects a decision. State that rule in one plain sentence with a short source name. Source dates belong in references, never in answers.

For every calculated figure, show the formula and actual inputs. For a share, name what it is a share of. Missing values are unknown, not zero; division by zero is undefined. Keep currencies, periods and conversion definitions separate. Do not add a total row to the rows it already includes. Do not average row-level ratios when the combined inputs are available.

Safety rules cannot be overridden. Do not invent facts, repeat unnecessary personal data, send spam, fake independent support (astroturfing), or handle credentials in chat. Have the user authenticate through their own secure account flow; never ask them to paste passwords, OAuth secrets, refresh tokens or credential files. The user can override rules about answer format. Account access is not permission to spend or change settings. Prepare a concrete proposal first. Apply only the exact changes the user authorized for that account and its entities. Stop before an unapproved change. Also stop after an unexplained account mismatch or a failed state check.

These workflow and answer safeguards are this plugin's rules of thumb, not Google requirements. Platform details in this skill have dated sources in [references/sources.md](references/sources.md).
