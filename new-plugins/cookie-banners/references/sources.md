# Official source register

Verified and read 2026-10-11. Each listed URL loaded with readable content. Adoption and publication dates below belong to the documents, not the read date. Snapshot verified 2026-10-11. For package release verification or a separately requested source refresh, re-open official sources to identify later changes. Ordinary supplied-material reviews use this embedded snapshot without fetching URLs.

| Source | Date and status | Scope and exact locator |
|---|---|---|
| [EDPB taskforce report PDF](https://www.edpb.europa.eu/system/files/2023-01/edpb_20230118_report_cookie_banner_taskforce_en.pdf) | Adopted 2023-01-17; read 2026-10-11. Current PDF linked by the official landing page; no replacement found in the targeted official search. | §§1–5 national ePrivacy rules for storage/access, GDPR for subsequent processing; §§6–8 refusal/positive action and authority differences; §§9–10 preselection; §§11–14 deceptive links; §§15–19 case-specific color/contrast; §§20–24 legitimate interest; §§26–30 necessity documentation; §§31–35 withdrawal. |
| [EDPB report landing page](https://www.edpb.europa.eu/documents/task-force-report/report-of-the-work-undertaken-by-the-cookie-banner-taskforce_en) | Published 2023-01-18; read 2026-10-11. | Confirms report identity and download; publication date differs from adoption. |
| [CNIL: Que dit la loi](https://cnil.fr/fr/cookies-et-autres-traceurs/que-dit-la-loi) | Dated 2020-09-29; live explanatory page read 2026-10-11. | France, Article 82. Sections on scope, exempt purposes, positive prior consent, new purposes, controller information, equal ease of refusal/withdrawal and proof. This page still links the original 2020 recommendation; use the consolidated version below for amendments. |
| [CNIL consolidated recommendation](https://cnil.fr/sites/default/files/2026-01/recommandation_cookies_consolidee.pdf) | Consolidated publication 2026-01-16: recommendation 2020-092 of 2020-09-17, amended by 2025-131 of 2025-12-18; read 2026-10-11. | France. §2.1 purposes; §2.2 controller identities; §2.3 granular choices, rejection/close, display recommendations, six-month good practice; §3 effective withdrawal; §4 proof; §5 measurement lifetime/retention recommendations; §7.1–7.6 authenticated cross-device choice scope, conflict handling, logged-out separation, identifier minimization and rollout. |
| [CNIL audience-measurement guidance](https://www.cnil.fr/fr/cookies-solutions-pour-les-outils-de-mesure-daudience) | Published 2025-07-04; read 2026-10-11. | France. “Dans quels cas…”: publisher-only measurement, anonymous statistics and prohibited data joining/cross-site identifiers. “Les recommandations…”: thirteen-month example without rolling renewal, twenty-five-month data recommendation. “Je suis fournisseur…”: self-assessment is not CNIL certification. |
| [CNIL 2020 guidelines](https://cnil.fr/sites/cnil/files/atoms/files/lignes_directrices_de_la_cnil_sur_les_cookies_et_autres_traceurs.pdf) | Adopted 2020-09-17, deliberation 2020-091; read 2026-10-11. | France; Article 5 measurement exemption. Read with current measurement guidance and consolidated recommendation. |
| [CNIL original recommendation](https://cnil.fr/sites/cnil/files/atoms/files/recommandation-cookies-et-autres-traceurs.pdf) | Adopted 2020-09-17, deliberation 2020-092; read 2026-10-11. | Historical original reachable through “Que dit la loi”; the 2026 consolidated document incorporates the cross-device amendment. Do not use the original alone for that workflow. |

## Finding-to-choice-to-evidence map

| Finding | Choice affected | Required deciding material |
|---|---|---|
| Optional tracking before positive choice / preselection | No action, X, custom save | Defaults, saved state, timed reads/writes; report §§6–10. |
| Refusal missing or obscured | Reject | Layer capture and action path; report §§8, 11–19; France recommendation §2.3. |
| Legitimate-interest bypass | Reject / object | Separate storage/access and subsequent-processing purposes; report §§20–24. |
| Unsupported essential category | No action / reject | Requested service, precise purpose and configured data use; report §§26–30; CNIL measurement guidance. |
| Ineffective or difficult withdrawal | Withdraw | Accessible route, action count and future reads/writes; report §§31–35; France recommendation §3. |
| Acceptance-only account propagation | Reject / withdraw / login / logout | Account and anonymous state captures, propagation trace, conflict notice; France recommendation §7. |

This map and the evidence worksheet are authored review methods. Authority obligations and recommendations retain their source and country scope. No generic EU pixel size, contrast ratio, lifetime, certified provider list or mandatory floating icon is inferred.

## Repair verification — 2026-10-11

Reopened the EDPB report and landing page, CNIL measurement guidance, consolidated recommendation and the following official pages during bfix. The 2026 material retains the distinctions used in the skills.

- [CNIL consumer cross-device explainer](https://www.cnil.fr/fr/cookies-et-autres-traceurs-quelles-conditions-consentir-en-une-fois-pour-plusieurs-appareils), read 2026-10-11: “Vous devez savoir à quoi vous consentez” explicitly places scope information in the CMP before account login. Consolidated §7.1 states information before exercising the choice; §7.2 separately recommends the immediate new-device reminder.
- [CNIL cookie FAQ](https://www.cnil.fr/fr/cookies-et-autres-traceurs/regles/cookies/FAQ), dated 2026-04-29; read 2026-10-11: current FAQ checked alongside the consolidated recommendation.
- Measurement guidance, “Les recommandations” and comparative-service paragraphs, read 2026-10-11: tracker expiry and data retention are distinct recommendations; multi-publisher comparisons require independent data and trackers.

