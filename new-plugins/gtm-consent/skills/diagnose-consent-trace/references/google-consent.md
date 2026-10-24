# Google consent decision reference

Read 2026-10-11. All six official URLs below loaded successfully in the live source check. Dates below are page metadata where observed, not predicted submission-day currency. Scope: Google Tag Manager web containers and Google website consent mode.

| Source | URL | Observed update date | Deciding detail |
|---|---|---|---|
| Troubleshoot consent mode | https://developers.google.com/tag-platform/security/guides/consent-debugging | 2026-07-30 | Earliest Consent event establishes defaults; latest establishes updates. Empty tab, absent defaults, late defaults and absent updates are distinct cases. A blocked container can prevent connection. |
| Set up consent mode | https://developers.google.com/tag-platform/security/guides/consent | 2026-07-30 | GTM consent APIs avoid queued gtag updates. Choices need persistence and restoration; update on the interaction page before navigation. |
| Create a consent template | https://developers.google.com/tag-platform/tag-manager/templates/consent-apis | 2026-07-30 | Async work before update: at least 500 ms wait in the default. Regional specificity is per type. Sandbox APIs and per-type write permissions are required. |
| Custom template APIs | https://developers.google.com/tag-platform/tag-manager/templates/api | 2026-07-30 | setDefaultConsentState/updateConsentState process after current-event tags, before queued data-layer items. States accept granted/denied; other values resolve denied and undefined preserves prior state. isConsentGranted treats unset as granted. addConsentListener does not fire for unset-to-granted. |
| Tag Manager consent support | https://support.google.com/tagmanager/answer/10718549?hl=en | No update date displayed | Built-in checks adapt behavior; additional checks require every listed type, including custom types, granted at the trigger. Not set adds no check. Consent Overview tracks additional-check configuration. |
| Consent mode overview | https://developers.google.com/tag-platform/security/concepts/consent-mode | 2026-07-30 | Basic blocks tags before consent. Advanced can send measurements without cookies under denied storage. ad_user_data and ad_personalization are independent of ad_storage. |

## How to use the evidence

Read the troubleshooting source for the reported error; setup/template sources for command placement and regional or async behavior; API reference for exact field and listener semantics; support/overview sources for firing versus blocking. The SKILL files carry the deciding rules so pasted-text analysis works without retrieval.

The table format, smallest-next-capture method and routing boundaries are this plugin's rules of thumb. A late default establishes an ordering defect, not proof of the exact data sent. To assess that, use the supplied tag and request evidence. Never decode undocumented compact network consent parameters by guesswork; request Consent-tab fields and API calls instead.

Refresh these URLs before the planned 2026-10-22 submission and when a supplied trace contradicts an embedded rule. Keep actual read dates and page update dates separate.

## Fix-pass verification — 2026-10-11

Reopened all six sources. Confirmed custom consent types and the all-required-types condition in “Tag consent settings”; verified `isConsentGranted`, `addConsentListener`, `setDefaultConsentState` and `updateConsentState` against their individual API entries. Capture branches are authored diagnostic choices, not mandatory Google collection checklists. Reuse supplied evidence and collect only the missing discriminator.
