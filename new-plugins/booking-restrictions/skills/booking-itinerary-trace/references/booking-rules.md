# Booking.com field reference

Read 2026-10-11. Applies to the current official Connectivity documentation, B.XML v1.1 unless stated. Reopen these sources before the planned 2026-10-23 submission; the build observation does not cover a future date. Relative update labels below are reported labels, not invented publication dates.

## Sources and deciding rules

1. https://developers.booking.com/connectivity/docs/b_xml-availability
   Loaded successfully; page showed “Last updated 1 week ago”. Field table separates room and rate updates, stay-through and arrival restrictions, arrival and checkout flags, zero-price unavailability and exclusive range end. Stock is normally shared across rates. Closing preserves other fields; reopening requires an explicit room-level change. Stock limit 254, sentinel 255, larger values reset to 254. Advance limits XDYH up to 360D; date support yesterday in CET through five years. Currency must match property. Child inherited restrictions/prices cannot be written directly; child closure is an exception, parent closure propagates. HTTP 200 may contain partial failures. One hotel, delta-only monthly batching is the documented recommendation, not a hard batch-size limit. Version-specific €50,000 price statement is labelled v1.0; do not impose it as a v1.1 universal cap.

2. https://developers.booking.com/connectivity/docs/b_xml-roomrateavailability
   Loaded successfully; page showed “Last updated 1 month ago”. Request number_of_days is 1–31, default 31; omitted start_date begins tomorrow. Room-level retrieval uses room_level=1; default is rate level. Rate-level stock can be inaccurate for a shared room-inventory property and omits room closure. Require matching room-level stock plus rate restrictions, unless documented configuration establishes the per-rate exception. Room-level retrieval excludes rooms without room-level availability; retain its warnings and never fill excluded rows with defaults. On existing elements in a verified complete raw response, integer attributes default to 0 and noninteger attributes to an empty string; do not extend this to trimmed exports or absent elements. Readback maps rooms_to_sell to roomstosell; min/max_stay_through to minimumstay/maximumstay; min/max_stay_arrival to minimumstay_arrival/maximumstay_arrival; exact_stay_arrival to exactstay_arrival; closed_on_arrival/closed_on_depart to closedonarrival/closedondeparture. Same closed label must retain its room/rate nesting. Availability snapshots need checkout rows for departure restrictions. Advance durations can be normalized on retrieval (25H becomes 1D1H). Occupancy and prices depend on Standard, OBP, RLO or LOS configuration. FPLOS length_of_stay is a special enabled-provider pattern, not a scalar stay minimum; get the actual configuration before interpreting it.

3. https://developers.booking.com/connectivity/docs/understanding-pricing-types
   Loaded successfully; page showed “Last updated 1 month ago”. Overlapping restriction conflicts need itinerary evaluation: the API does not validate these conflicts or emit warnings for them. Standard, derived and occupancy-based flows differ from LOS pricing. LOS pricing’s inventory/pricing path does not add ordinary restrictions. Room type, rate plan, roomrate and pricing type must exist before inventory is created.

4. https://developers.booking.com/connectivity/docs/b_xml-availability-troubleshooting
   Loaded successfully; page showed “Last updated 1 week ago”. Errors are scope-specific:
   - WARN_DUPLICATE_DATES: first occurrence processed, later duplicates ignored.
   - RATE_LEVEL_INVENTORY: this configured room requires rate_id for stock updates; exception to the ordinary shared-stock model.
   - RATE_IS_A_SLAVE_RATE: specified attribute follows rate relations; trace its parent owner.
   - RATE_NOT_ACTIVE_FOR_ROOM: rate not activated for that room; compare allowed roomrates.
   - ROOM/RATE_EDITABLE_ONLY_ON_EXTRANET: use the extranet for that entity.
   - NOT_A_VALID_RESTRICTION: certain regional special products require minimum zero or greater than 31; preserve product/region scope.
   - INVALID_CURRENCY_CODE: supplied currency differs from property currency.
   - NOT_A_VALID_DATE / INVALID_DATE: invalid format or window; preserve returned bounds rather than copying old examples.
   - HTTP 200: at least one successful update, potentially others failed. HTTP 400: schema issue or all updates errored. Inspect body and fresh values.
   The range error message allows equality, while the main request table requires from before to. Use a single date value for one day and strictly increasing ranges.

5. https://developers.booking.com/connectivity/docs/enablelongstays
   Loaded successfully; page showed “Last updated 1 month ago”. Default property maximum is 30 nights; long-stay support can permit 45, 60, 75 or 90. Require the property’s supplied enabled/max setting before proposing a larger restriction. The HDCN route was deprecated December 2024 and sunsets 2026-12-31; current settings use Property Details property_settings.long_stay.enabled and max_length_of_stay. Do not propose new HDCN setup.

6. https://developers.booking.com/connectivity/docs/content-api-modules/property-details-api/implementing-property-api-settings
   Read 2026-10-11; loaded successfully. Current Property Details settings expose `property_settings.long_stay.enabled` and `max_length_of_stay`. Use these property settings alongside the long-stay guide rather than starting deprecated HDCN setup.

## Authored method

The blocker table, minimal delta, unchanged-field preservation and evidence-needed markers are workflow choices. No generic occupancy/sales rule or invented stock buffer is bundled. Missing export fields are not API defaults: an export may omit current settings. An outbound request is a delta, not proof of present availability.
