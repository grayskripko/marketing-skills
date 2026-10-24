# Booking Restrictions

Check why a Booking.com stay is unavailable, including minimum-stay settings and closed arrival or departure dates. Return the blocking fields and proposed settings changes.
For property managers and revenue teams. Needs pasted text or readable inventory/restriction exports, itinerary dates, room/rate identifiers and requested room count. No account, keys or installation is required for this path.

| Skill | Input | Output |
|---|---|---|
| booking-itinerary-trace | Itinerary and current inventory/restriction rows | Blocking dates and fields, proposed settings and missing evidence |
| booking-settings-review | Current rows, proposed settings or B.XML, optional response body | Corrected change list, affected dates/rates and before/after itinerary result |

Try: “Why can’t we sell this three-night stay? Here are the calendar rows.” Or: “Will these settings changes fix the stay without opening other rates?”

Exports should include occupied nights and the checkout date for departure restrictions. Include capture time, pricing model, occupancy and parent/child rate settings where relevant. A sent update is not a current-state snapshot; include its response and a later export if you want to confirm the outcome.

The skills draft changes from supplied evidence. Apply the reviewed changes in your existing Booking.com extranet or channel manager, then supply fresh rows for comparison.

Network: none during normal analysis. If you request a documentation refresh, the assistant may fetch public pages on developers.booking.com and official Booking.com links from those pages. It must send no itinerary, export or property data with those requests. No Booking.com account endpoints, connectors, telemetry or paid APIs are used.

See [PRIVACY.md](PRIVACY.md). Source rules and their observation dates are bundled in each skill’s references. The package contains instructions and a static icon, with no executable helpers.
