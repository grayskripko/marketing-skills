# Zendesk export interpretation

Use only when supplied fields match the documented objects below. A vendor name or arbitrary CSV column label is insufficient: request the export mapping if needed. These are bundled facts for offline analysis; do not fetch sources at runtime. User scoring and snapshot policies govern analytical choices.

## Legacy satisfaction ratings — source S1

| Field/state | Meaning and analytical use |
|---|---|
| `score=good` / `bad` | Scored positive / negative responses for binary CSAT. |
| `score=offered` / `unoffered` | Survey offered / not offered; neither is a scored response. |
| `id`, `ticket_id` | Rating identity and ticket join key, respectively. |
| `created_at`, `updated_at` | Rating creation and update times; neither is ticket resolution time. |
| `assignee_id`, `group_id` | Assignment at rating time, not current ticket assignment. |

The API is explicitly legacy. Only one CSAT option can be active; migration requires disabling legacy and custom CSAT automations/triggers. List filter `good` includes ratings with and without comments; comment-only extracts are selected populations. The count endpoint is approximate; above 100,000 it caches for 24 hours and may temporarily report 100,000 with null refresh time.

Analytical decisions: exclude offered/unoffered from scored CSAT. A current-state snapshot cannot reconstruct historical invitations. Repeated IDs across snapshots may be updates, not extra respondents: preserve versions until the export's as-of/event policy is known. Never automatically select latest `updated_at` for a historical period.

## Current survey responses — source S2

Select `subjects` entries with `type=ticket` and join their `id`; `subject_zrns` can also encode `zen:ticket:ID`. Conversation/request subjects do not establish a ticket relationship, even when their ID text appears in the ticket export. Label that relationship unconfirmed pending a mapping, rather than definitively unmatched. Count response `id`, not answers or subjects, as the response unit.

Select an answer with `type=rating_scale` and `question.sub_type=customer_satisfaction`; other rating questions are not CSAT. Preserve `rating` and `rating_category` (`bad`, `neutral`, `good`). Ask how neutral enters the user's metric rather than silently dropping it or guessing a numeric cutoff.

A `skipped` comment is missing text, not a missing rating; a skipped CSAT question supplies no score. Answers have `created_at` and `updated_at`; `expires_at` must not be used as submission time. Explain its expiry meaning only when the supplied object and export mapping establish it and it affects the requested result. Retain `survey.id` and `survey.version`: version increments on survey edits, so obtain wording/scale definitions before pooling changed versions. Return supported version-specific CSAT now; if useful, label the cross-version category-based share provisional rather than a comparable pooled CSAT. Access starts at Support Professional or Suite Growth; the list permits admins and responders for their own responses.

## Missing evidence and alternate shape — source S3

The documented path is updated tickets → ticket audits → detailed responses. Updated tickets alone do not prove submission. In audit events, `type=SurveyResponseSubmitted` carries non-null `survey_response_id`; link that value to response `id`. Request authorized audit and detailed-response exports only where needed to establish a missing relationship, plus invitation-cohort records if response rate is requested, never credentials. Do not require an audit chain when the supplied response already establishes its ticket and CSAT answer.

The tutorial response example uses top-level `survey_id` and `survey_version`, while S2 uses nested `survey.id/version`. Preserve the actual shape and verify its mapping rather than requiring only one representation. The tutorial identifies `unoffered` as no survey received.

## Applying this to comparisons and actions

Before respondent-mix calculations, resolve the survey-version/scoring/date basis and distinguish rating-time group from current ticket group. If these differ, return separate supported results and the specific comparability issue. Missing later strata still block complete fixed-mix estimates.

For a Zendesk-backed backlog, make an incomplete evidence chain an owned export-reconciliation task: acceptance means the supplied response evidence links to the right ticket and CSAT answer, with unconfirmed, unmatched and unscored cases reported separately. Use the audit response ID when actual audit records follow the documented schema; do not prescribe a specific event name as though it appeared in an export that has not been supplied. Preserve comment selection and survey version in follow-up measures. This task supplements documented handoff/policy tasks; schema knowledge supplies no refund eligibility or product commitments. For comments alone, use the existing action workflow without inventing Zendesk fields.

## Dated official sources

All three URLs loaded through live web retrieval on **2026-10-11 UTC**, with readable official documentation. Publication/update dates were not stated in the retrieved pages. The verification date is not a publication date.

- **S1:** [Zendesk Satisfaction Ratings](https://developer.zendesk.com/api-reference/ticketing/ticket-management/satisfaction_ratings/) — JSON format, legacy transition, list filters, count endpoint.
- **S2:** [Zendesk CSAT Survey Responses](https://developer.zendesk.com/api-reference/ticketing/ticket-management/csat_survey_responses/) — JSON format, typed subjects, survey/answer/question objects, list access.
- **S3:** [Zendesk Getting the CSAT ratings of tickets](https://developer.zendesk.com/documentation/ticketing/data-and-reporting/incremental-ticket-export-csat/) — updated-ticket/audit/response chain and alternate example shape.
