# Official Uber Eats menu knowledge

Read 2026-10-11. These are observations of accessible official documentation on that date. Pages did not expose a revision date. Planned submission: 2026-10-22; reopen the listed pages before submission and update changed rules and dates together. Runtime skills use these embedded notes without fetching pages.

## 1. Upload Menu schema — deciding field rules

URL: https://developer.uber.com/docs/eats/references/api/v2/put-eats-stores-storeid-menu

Loaded: Upload Menu, current documented V2 route `PUT /v2/eats/stores/{store_id}/menus`. Read 2026-10-11.

Sections to check: MenuConfiguration; Menu; MultiLanguageText; Category; Item; PriceRules/PriceOverride; QuantityConstraint/QuantityConstraintOverride; Suspension; TaxInfo; VisibilityInfo; ModifierGroup; Classifications.

Root arrays are menus/categories/items/modifier_groups. Category entities and modifier options are ITEM references. Upload translations contain one language-country locale. Item price is required, integer, including zero. Money uses one-hundredth denomination, including yen. Override types are MENU/ITEM/MODIFIER_GROUP with context IDs; no cross-type priority is specified.

Positive option minima are mandatory unless optional=true; default=false. Required minima exceeding group max make the parent unorderable. Defaults fit inclusive bounds; unique bounds are group-only. Thresholds are paired, nonnegative, no greater than max, ordered around default.

Core price is at least price; container deposit is metadata. Tax rate adds tax on first-level items; VAT rate is included. Future suspension seconds mean unavailable. External data max: 1024 characters. Fulfillment modes permanently split after non-delivery upsert; delivery first; dine-in Australia/NZ only. Successful upload returns 204 with no body. PriceRules also lists in_store_price and in_store_discounted_price without optional labels; retain this requirement when assessing completeness, and do not infer those prices. Alcohol classification cannot be reversed through later zero/null updates.

## 2. Editing your menu — visibility and merchant editing path

URL: https://help.uber.com/en/merchants-and-restaurants/article/edycja-menu?nodeId=156909ff-4025-44c7-a200-20b339f9fa93

Loaded: Editing your menu in English despite the localized slug. Read 2026-10-11.

An item needs category membership to display. POS-integrated menus are edited through the Menu API rather than Menu Maker. Some updates require menu-team verification and may take up to 24 hours. Menu Maker photos undergo a separate review, typically three days or less. Do not apply these timings as API response guarantees. This help page requires allergens/additives and nutritional information for prepackaged goods; apply to missing merchant metadata, not as permission to invent nutrition or as a universal jurisdictional law.

## 3. Menu submission information — original and working locale

Requested URL: https://help.uber.com/merchants-and-restaurants/article/-mit%C3%A4-valikoimaa-koskevia-tietoja-minun-pit%C3%A4%C3%A4-antaa-uber%C2%A0eatsia-varten?nodeId=83ae0158-34aa-45d7-9fff-6bab96354072

That route returned an access error on 2026-10-11. English variants and the bare article route also failed.

Working official URL, same node ID: https://help.uber.com/fi-FI/merchants-and-restaurants/article/-mit%C3%A4-valikoimaa-koskevia-tietoja-minun-pit%C3%A4%C3%A4-antaa-uber%C2%A0eatsia-varten?nodeId=83ae0158-34aa-45d7-9fff-6bab96354072

Loaded: Finnish title, English body “Requirements when submitting your menu to Uber Eats.” Read 2026-10-11. The reader reported a crawl two months earlier; no page revision date was shown.

The submission checklist calls for current legible, nonhandwritten items and prices, delivery hours, additions/removals, add-on prices/flavors and special instructions. Descriptions are recommended, not a universal required API field. Its English/French/Spanish/Mandarin submission wording is this article's intake scope, not a restriction on every API locale. It links the prohibited-item page below.

## 4. Menu Integration — scope, images and editing authority

URL: https://developer.uber.com/docs/eats/guides/menu-integration

Loaded: Menu Integration. Read 2026-10-11.

Upload replaces existing menus. Single-item updates require the original menu to have been uploaded through the API. Avoid concurrent Menu Maker edits for API-managed menus. Store hours are the union of menu service availability. Item visibility applies to parents; modifier options inherit parent visibility. Category-level availability is unavailable; item visibility can express it for each item.

Images must be JPG, WEBP or PNG, strictly below 25 MB, with each dimension 320–6000 pixels inclusive. API images may take hours to process. Core price is intrinsic modifier refund value; bundled items describe included components shown in support/refund, not customizable during purchase. Alcohol sales depend on enabled markets and supplied classifications; do not infer eligibility from a menu label.

## 5. Errors — HTTP meaning, not a guessed field cause

URL: https://developer.uber.com/docs/eats/guides/errors

Loaded: Errors. Read 2026-10-11.

| HTTP / code | Meaning for a supplied menu report |
|---|---|
| 400 / validation_failed | Input validation failed; types or required fields may be wrong. Need detail to locate the defect. |
| 403 / user_not_allowed | Caller lacks access to the referenced store/order. Changing modifiers does not repair access. |
| 404 / resource_not_found | Referenced store/order does not exist. Check the supplied resource/path. |
| 500 / internal_server_error | Uber-side internal error; table marks it nontransient. Do not prescribe repeated menu rewrites or blind retries. |
| 503 / service_unavailable | Transient service/connectivity failure. The guide recommends backoff for transient failures; the skills perform no retry. |

Do not apply order-specific 409 status conflicts to a menu validation report.

## 6. Troubleshooting menu errors — exact boundaries and exceptions

URL: https://developer.uber.com/docs/eats/references/api/v2/troubleshoot-errors

Loaded: Troubleshooting Errors from the Menu API. Read 2026-10-11.

Menus and some weekly service availability are required. Emptying them is not the pause-store operation. “nil item” means malformed or nonexistent item ID on the referenced menu; “invalid uuid” concerns store ID in the path; orgUUID errors concern store organization linkage.

Overlapping item visibility periods cause invalid visibility. Invalid Price Info can mean price exceeds a configured ceiling; $375 is explicitly an example. Do not turn it into a universal limit.

The short-hours prose says intervals greater than 60 minutes, uses inclusive endpoints, and accepts a consecutive overnight example 23:30–23:59 plus 00:00–00:30 at a 60-minute threshold. Preserve this exact-boundary distinction; do not reject the two fragments separately or invent a universal 61-minute minimum. At an unresolved boundary, get the actual error/threshold.

Previously positive alcoholic classification needs a Support correction to revert; API zero/null does not revert it.

## 7. Get Menu — readback shape and a documented discrepancy

URL: https://developer.uber.com/docs/eats/references/api/v2/get-eats-stores-storeid-menu

Loaded: Get Menu. Read 2026-10-11.

Readback shape helps map a pasted response into entity references. Do not assume all GET response conventions are valid PUT input. GET's refund_under row says it cannot be less than max_permitted; PUT's row says it cannot be greater than max_permitted. Use PUT's write constraint for proposed configuration and retain this discrepancy for source refresh. GET translation wording also describes fallback behavior and additional-translation limitations, while PUT asks for exactly one translation. Use PUT's one-locale shape for new upload specifications.

## 8. Prohibited items — intake policy link

URL: https://help.uber.com/merchants-and-restaurants/article/what-can-i-include-in-my-menu?nodeId=67ce5ca4-82d7-490e-b890-4240587c40b6

Loaded: What items are prohibited on Uber Eats? Read 2026-10-11. Reached through the submission-information article; the old /restaurants/ path redirects to /merchants-and-restaurants/.

Use the actual listed category and applicable market if a user asks whether an item may be published. The opened page does not identify a country scope. It lists prohibited and restricted categories with agreement-dependent exceptions; establish the applicable market and merchant terms before applying an item restriction. This package's main job is configuration, so it does not infer policy violations from ambiguous names or reproduce a worldwide product-policy taxonomy.

## Local method choices

These are this plugin's rules of thumb, not Uber schema requirements: trace the menu-parent-group-option context; return the smallest intent-preserving correction; exhibit a feasible parent selection and a selection containing each intended option; keep missing fields unresolved; avoid competing context overrides when priority is unspecified. Formula derivations use the supplied currency and tax basis. They do not establish server rounding, account eligibility, live visibility or upload acceptance.
