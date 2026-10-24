# Official GA4 rule register

Read 2026-10-11. All 13 URLs loaded with HTTP 200 and matching official titles. Read date means retrieval date, not an asserted publication date. Refresh the deciding pages when their rules affect a current decision. These are paraphrased field rules, not general analytics advice.

## Event naming rules - Analytics Help

- URL: https://support.google.com/analytics/answer/13316687?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Web and Android/iOS naming; current lists are explicitly non-exhaustive.
- Deciding rules: Event names are case-sensitive, start with a letter, and use letters/digits/underscores. Web prefix query_id and platform-specific event lists apply. The event/item/user-property reserved-field lists govern custom registration. Observed automatic events need operation-aware review. in_app_purchase is reserved for Web, not App. This page does not supply a tag/SDK parameter-name grammar.

## Event collection limits - Analytics Help

- URL: https://support.google.com/analytics/answer/9267744?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Tag/SDK collection per property; server transport is separate.
- Deciding rules: Event-name/name limits: 40 characters; 25 event parameters; ordinary string values 100 characters. Page title/referrer/location exceptions: 300/420/1,000. Ecommerce has 27 additional custom item parameters. User properties: 25, name 24, value 36; User-ID 256. Web distinct events have no cap; App 500 per user, automatic and enhanced excluded. Encoded URL length governs URL limits.

## [GA4] Configuration limits - Analytics Help

- URL: https://support.google.com/analytics/answer/12229528?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Standard property configured inventory.
- Deciding rules: Custom user dimensions 25, event dimensions 50, event metrics 50. Configuration cap prevents creating an additional item. Inventory capacity is separate from collection acceptance. This overview omits item scope; use the definitions and item-dimension pages for that quota.

## [GA4] About custom dimensions and metrics - Analytics Help

- URL: https://support.google.com/analytics/answer/14240153?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Standard versus 360 custom-definition capacity and reporting.
- Deciding rules: Standard/360: user dimensions 25/100; event dimensions 50/125; item dimensions 10/25; metrics 50/125. At a custom-dimension cap, wait 48 hours after deletion before creating another. Use predefined fields where available. User IDs, session IDs and timestamps are unsuitable custom dimensions; high cardinality can create (other). Custom reporting typically becomes available after 24–48 hours.

## [GA4] Create event-scoped custom dimensions - Analytics Help

- URL: https://support.google.com/analytics/answer/14239696?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Event-scoped custom-definition create workflow.
- Deciding rules: Unique display label allows spaces/underscores, not hyphens. Event scope and source parameter cannot be changed after save. Editor or Administrator required; verify collection before registration. App integer values are not parsed for event-scoped custom dimensions like web integer values; alphanumeric categories are recommended. Admin > Data display > Custom definitions supplies the create form.

## Create item-scoped custom dimensions - Analytics Help

- URL: https://support.google.com/analytics/answer/14239695?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Item-scoped definitions for custom ecommerce fields.
- Deciding rules: Collection can carry 27 custom item fields while registration supports 10 Standard or 25 in 360. Display-label hyphens prohibited; scope and source immutable after save. Item custom dimensions cannot be added to standard reports; use explorations. These collection numbers must not override MP sending-events transport limits.

## [GA4] Create user-scoped custom dimensions - Analytics Help

- URL: https://support.google.com/analytics/answer/14239618?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: User-scoped definition fields.
- Deciding rules: User scope reads a user property. Unique display name has no hyphens. Scope and source user property cannot change after saving. Editor or Administrator needed; reporting uses the sent custom data and definition, with 24–48-hour availability guidance.

## Validate events  |  Google Analytics  |  Google for Developers

- URL: https://developers.google.com/analytics/devguides/collection/protocol/ga4/validating-events
- Read: 2026-10-11; HTTP 200.
- Scope: MP validation replies, not SDK numeric error events.
- Deciding rules: Debug endpoint /debug/mp/collect returns fieldPath, description and validationCode; it does not populate reports or validate api_secret/firebase_app_id. Codes: VALUE_INVALID invalid value; VALUE_REQUIRED missing; NAME_INVALID invalid name; NAME_RESERVED reserved; VALUE_OUT_OF_BOUNDS too large; EXCEEDED_MAX_ENTITIES too many; NAME_DUPLICATED duplicate name. Develop using ENFORCE_RECOMMENDATIONS, omit validation_behavior in production. Empty messages do not prove report delivery.

## Measurement Protocol reference  |  Google Analytics  |  Google for Developers

- URL: https://developers.google.com/analytics/devguides/collection/protocol/ga4/reference
- Read: 2026-10-11; HTTP 200.
- Scope: Measurement Protocol envelope, payload reservations and per-event parameters.
- Collection reservations: event names `ad_activeview`, `ad_click`, `ad_exposure`, `ad_query`, `ad_reward`, `adunit_exposure`, `app_clear_data`, `app_exception`, `app_install`, `app_remove`, `app_store_refund`, `app_update`, `app_upgrade`, `dynamic_link_app_open`, `dynamic_link_app_update`, `dynamic_link_first_open`, `error`, `firebase_campaign`, `firebase_in_app_message_action`, `firebase_in_app_message_dismiss`, `firebase_in_app_message_impression`, `first_open`, `first_visit`, `notification_dismiss`, `notification_foreground`, `notification_open`, `notification_receive`, `notification_send`, `os_update`, `session_start`, `user_engagement`. App-only: ad_impression, in_app_purchase, screen_view. Web MP page_view is not in the reserved list. Event parameter firebase_conversion and prefixes _, firebase_, ga_, google_, gtag. are prohibited. User properties first_open_time, first_visit_time, last_deep_link_referrer, user_id, first_open_after_install and prefixes _, firebase_, ga_, google_ are prohibited. These apply without registration; root user_id is a separate envelope field.
- Deciding rules: 2xx signals HTTP receipt even for malformed/unprocessed data. Up to 25 events and 25 params/event; 25 user properties; body under 130 kB. Standard/360 parameter values 100/500 characters. Event names 40. Timestamp micros, backdate up to 72 hours. session_id plus engagement_time_msec supports accurate session/engagement and Realtime metrics; credentials remain outside this export-review workflow.

## Send Measurement Protocol events to Google Analytics  |  Google for Developers

- URL: https://developers.google.com/analytics/devguides/collection/protocol/ga4/sending-events
- Read: 2026-10-11; HTTP 200.
- Scope: MP sending-events Limitations; transport-specific difference.
- Deciding rules: Parameter/item names max 40, alphabetic first character, alphanumeric/underscore thereafter. String values 100 Standard or 500 in 360. Item fields have a maximum of 10 custom parameters on this page. Do not apply the tag/SDK allowance of 27 to MP. screen_view, ad_impression and in_app_purchase are App-only for MP. Route uncertain collection method to a missing-detail marker, preserving both branches.

## Analytics error codes  |  Google Analytics for Firebase

- URL: https://firebase.google.com/docs/analytics/errors
- Read: 2026-10-11; HTTP 200.
- Scope: Firebase Analytics SDK diagnostic codes; do not generalize to MP or every web flow.
- Deciding rules: 2 invalid event name: event ignored. 3 invalid param name: diagnostic replacement. 4 long value: parameter dropped. 5 over 25 params: extras dropped. 6 invalid user-property name/7 long value: property ignored. 8 over 500 app event types: extras dropped. 9 over 25 user properties: change ignored. 13 reserved event: ignored. 14 reserved param: replaced. 15 reserved property: change ignored. firebase_error_value identifies affected names where documented.

## Best practices to avoid sending Personally Identifiable Information (PII) - Analytics Help

- URL: https://support.google.com/analytics/answer/6366371?hl=en
- Read: 2026-10-11; HTTP 200.
- Scope: Ordinary Analytics event/custom-dimension fields, URLs, titles and entered text.
- Deciding rules: Remove personally identifying information before collection, including email addresses in URL paths, query strings, titles and free text. Web redaction is best-effort and is not a replacement for repairing the outgoing contract. Dedicated user-provided-data features have separate requirements; do not turn ordinary event params into a hashed-email workaround.

## Source reconciliation and local procedure

The configuration overview lacks item scope; the dedicated custom-definitions pages supply it. The collection page describes tag/SDK limits and points server-to-server readers elsewhere. MP sending-events currently states 10 custom item fields; tag/SDK collection states 27. Keep the transport explicit. 

Local procedure, not a platform rule: preserve owners and triggers; deduplicate new definitions by kind/scope/exact source, checking metric unit and Currency Data type compatibility; distinguish create/reuse/defer; keep undecided removals visible; never interpret receipt as runtime acceptance.

## Create custom metrics

- URL: https://support.google.com/analytics/answer/14239619?hl=en
- Read: 2026-10-11; HTTP 200; matching official title.
- Scope: Custom metrics, always Event scope.
- Deciding rules: Admin > Data display > Custom definitions > Custom metrics. Provide unique metric label (no hyphens), event parameter and measurement unit. Description is optional. Standard is shown for a unitless count. Currency requires cost/revenue Data type; Distance supports Feet/Miles/Meters/Kilometers; Time supports Milliseconds/Seconds/Minutes/Hours. No Mass/Grams option is documented. Using Standard while recording grams in the label/description is a proposed local representation requiring agreement, not a native unit. Event parameter is immutable after saving. Editor or Administrator required.
