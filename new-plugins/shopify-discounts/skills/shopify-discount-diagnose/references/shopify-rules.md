# Shopify discount source notes

Read and rechecked 2026-10-11. These official pages were retrieved on the observation date. Observation date is not a publisher revision date; none was displayed. Scope: Shopify native discount settings and checkout, with plan/app qualifications. Reopen the relevant official page when current behavior matters. No store-specific configuration was verified.

## Combinations
https://help.shopify.com/en/manual/discounts/discount-combinations

Relevant sections: Eligibility requirements; Discount limits; Calculation; Same line item; Multi-class combinations; Troubleshooting. Both sides' allowed classes decide compatibility, including every class in multi-saving offers. Plus same-line setup needs reciprocal tags. The detailed plan table permits the Buy X get Y customer-gets exception; broad troubleshooting/FAQ language elsewhere on the same page omits it. Use the specific table, not a blanket prohibition. The shipping-conflict section also qualifies the broad best-discount wording.

The page still mentions legacy Scripts and checkout.liquid. Do not infer they are usable in a current store or direct a merchant to install them. Supported ordinary combination channels are Online Store, Storefront API and POS; external checkouts are excluded. Custom manual POS/draft discounts bypass other offers' combination settings. Obtain observed allocations for exact manual arithmetic. The final native Plus mixed same-line example applies the percentage before the fixed product amount.

## Code errors and availability
https://help.shopify.com/en/manual/discounts/discounts-faq

Relevant sections: used-code hold; expiry; rollout effective status; code-entry visibility; invalid codes. Payment submission can hold usage until completion/failure; history is not cleared by renaming/reactivation. Effective rollout state can differ from dates. Segment-restricted discounts apply to existing customers: a new first-checkout customer without a profile joins the segment only after the first order completes. Purchased gift cards are not eligible for ordinary order discounts; the exception is a product-specific discount selecting that gift-card product. Minimum qualification is a separate question. The three error categories in the diagnosis skill distinguish inactive/missing codes, item scope, and combination conflicts. Diagnose from the exact visible text; paraphrases may obscure the category.

## Amount-off field semantics
https://help.shopify.com/en/manual/discounts/discount-types/percentage-fixed-amount

Relevant sections: Minimum purchase requirements; fixed amount once per order. Product minimums use eligible items after earlier product reductions; gift cards count only when specifically selected. Native automatic amount-off discounts at retail require POS Pro and enabled POS availability. Order minimums have two simultaneous tests, including different gift-card and purchase-type treatment; other order reductions do not reduce that base. Fixed product discounts need the once-per-order field. Amount-off discounts do not discount shipping. The article's allocation example has unexpectedly coarse amounts; do not use it to infer cent-level rounding. Use supplied checkout allocations when rounding affects the result; if missing, ask the user to report the relevant allocation before payment.

## Buy X get Y
https://help.shopify.com/en/manual/discounts/discount-types/buy-x-get-y

Relevant sections: Considerations; Minimum purchase; Customer gets. The reward must be placed in the cart. Only qualifying Customer buys products count, at full prices, excluding already product-discounted items. Shipping/tax are excluded. Purchase type and per-order uses cap matter. Purchased gift cards can count when selected; redeemed credits do not change qualification. POS Lite excludes this native promotion at retail checkout; POS Pro supports it.

## Shipping offer fields
https://help.shopify.com/en/manual/discounts/discount-types/free-shipping

Relevant sections: Minimum purchase requirements; Countries; rate exclusion. Discounted product prices form the minimum, including gift cards purchased. Redeemed credits do not change it. Country scope and rate ceiling are distinct from the merchandise minimum. Use the supplied actual shipping rate, or ask the user to report it when rate eligibility affects the result; an excluded expensive rate is not a cart-value exclusion.

## App-created offers
https://shopify.dev/docs/api/functions/latest/discount

Official Discount Function API loaded. Apps can implement product, order and shipping savings. Their actual conditions and operations are needed to reproduce checkout amounts; native field descriptions do not establish arbitrary app logic. Use this URL only as public documentation; do not call store APIs or implement Functions under this skill.

## Analysis conventions

The input ledger, conditional totals, comparison table and no-payment observation checklist are author workflow choices, not Shopify requirements. Screenshots described in text are evidence only for the fields the user describes. Missing fields remain unknown.
