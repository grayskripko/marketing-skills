# GA4 ecommerce field register

All pages below loaded and were read 2026-10-11. This records current content on that date, not a forecast of the 2026-10-24 submission. Refresh these same official URLs before submission. Read dates are maintained here, not printed in routine user answers.

## GTM transport

https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtm&hl=en

Scope: Google Tag Manager ecommerce guide. Examples clear the previous ecommerce object with an ecommerce-null push. Parameters live under ecommerce; currency accompanies value. The guide maps ecommerce.transaction_id, items and value to GA4 event parameters. Refund examples retain the purchase transaction ID and item information. The items array allows 200 entries and up to 27 custom item parameters beyond prescribed fields. Missing a clear from an excerpt does not demonstrate the surrounding state.

## gtag transport

https://developers.google.com/analytics/devguides/collection/ga4/ecommerce

Scope: gtag.js ecommerce guide. gtag event calls use flat parameters. Purchase and refund use the original transaction ID; refund item IDs and quantities support item refund measurement. Currency is event-level for value data. Item actions describe the affected products; a view_cart describes the cart. Do not transform a whole-cart snapshot into a single-item action without supplied action facts.

## Supported cart and checkout events

https://developers.google.com/analytics/devguides/collection/ga4/reference/events

Read 2026-10-11. Supported non-transaction schemas: view_item_list, select_item, view_item, add_to_cart, remove_from_cart, view_cart, begin_checkout, add_shipping_info and add_payment_info require items, with item_id or item_name per item. Transaction ID is not required for these events. The shipping_tier, payment_type, coupon and list identifiers are optional. The guide distinguishes added/removed items from the cart being viewed; use action quantities, not the post-action balance. Promotion/custom schemas require their own event-specific source check. This boundary avoids applying purchase requirements to every ecommerce event. The GTM and gtag ecommerce guides specify that add_payment_info fires on submission of payment information, not arrival at the payment step; payment_type remains optional.

## Deciding event fields

https://developers.google.com/analytics/devguides/collection/ga4/reference/events#purchase
https://developers.google.com/analytics/devguides/collection/ga4/reference/events#refund

Scope: purchase/refund event schema. Purchase requires transaction_id and items; refund requires transaction_id but items are optional and recommended for item reporting. Each item requires item_id or item_name. Value is the sum of price times quantity, excluding tax and shipping; currency is required with value, in three-letter ISO 4217 form. Price is discounted unit price; discount is a unit monetary amount; omitted quantity defaults to 1. Event/item coupons are independent. Affiliation and location_id are item-only. Monetary parameters and quantity are numeric. Correcting transport does not establish collection.

## Duplicate purchases

https://support.google.com/analytics/answer/12313109?hl=en

Scope: transaction IDs and web-stream purchase deduplication for the same user. User identity and collected-event evidence are needed to apply that rule to repeated capture attempts. Deduplication does not apply to app streams. IDs must be unique per order and omit customer-identifying information. Reused IDs can undercount purchases; an empty string deduplicates purchases with empty IDs. Do not infer that repeated refunds are removed or that a copied payload amended a historical purchase.

## Collection boundaries

https://support.google.com/analytics/answer/9267744?hl=en

Scope: tag/SDK collection. 25 event parameters, 40-character event and parameter names, ordinary string parameter values up to 100 characters; page_title 300, page_referrer 420, page_location 1,000. Item custom parameters have a separate 27 limit. Fields exceeding limits are not logged. Count parameters after mapping, rather than unrelated data-layer keys. Count encoded URL characters for URL values. Server-to-server limits are separate.

## Supplied SDK errors

https://firebase.google.com/docs/analytics/errors

Scope: Firebase SDK diagnostics, not a browser-tag diagnostic promise. Page last updated 2026-10-08 UTC. Code 17: arrays exceeding 200 are truncated. Code 18: missing value or invalid value parameter type causes value to be dropped; a string type is distinct from an incorrect numeric amount. Code 19: missing currency on a conversion event causes value to be dropped. Code 28: item custom parameters beyond 27 are dropped. The firebase_error field is a parameter, not an event name. Nested item array parameters are unsupported (code 22). Explain an observed code only within the supplied SDK context.

## Local workflow decisions

These are task methods, not additional Google requirements: match only explicitly linked orders; preserve receipt identifiers separately; reconcile only aligned coverage and currencies; never allocate aggregate amounts to invented SKUs; show unknowns outside executable examples. They implement the supplied-facts-only job.

Targeted source check 2026-10-12: transaction-ID Help and Firebase diagnostics were read again; payment submission timing was confirmed in the official ecommerce guides. Other source read dates remain unchanged.
