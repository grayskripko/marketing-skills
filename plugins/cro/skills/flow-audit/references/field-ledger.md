# Field ledger

One row per field, in the order the visitor meets them.

| Field as labelled | Why the business asks | Needed to finish this step? | Keep / make optional / move later / remove | Input type and autocomplete token | Issue |
|---|---|---|---|---|---|

Rules:
- A field with no stated purpose → "remove or justify".
- A field needed later (company size for sales routing, phone for delivery problems) → "move later": ask after the conversion, or derive it.
- No per-field conversion cost is ever stated; no source supports a fixed cost per field.
- A marketing-consent checkbox is separate from the order or signup and starts unticked (EU: GDPR Art. 4(11) and recital 32; CJEU C-673/17 *Planet49*, 2019-10-01: a pre-ticked box is not valid consent).
- On opt-in forms the friction rows apply; the promise, consent design and delivery of the opt-in belong to a separate review (one out-of-scope line).

## Autocomplete tokens (WHATWG HTML, autofill field names, read 2026-10-03)

| Field | type | autocomplete |
|---|---|---|
| Full name | text | name |
| Given / family name | text | given-name / family-name |
| Email | email | email |
| Phone | tel | tel |
| Company | text | organization |
| Street address | text | street-address (or address-line1, address-line2) |
| Postcode | text | postal-code |
| Country | select | country-name or country |
| Card number | text, inputmode numeric | cc-number |
| Card expiry | text | cc-exp |
| Card security code | text | cc-csc |
| Name on card | text | cc-name |
| New / current password | password | new-password / current-password |
| One-time code | text, inputmode numeric | one-time-code |

The right type also brings up the matching phone keyboard (FL-16).

## Reference row (context, never a target)

Baymard Institute, "Checkout flow average form fields", 2024-06-26, read 2026-10-03: the average checkout in its 2024 benchmark has 5.1 steps and 11.3 form fields, while most sites could manage with about 8 fields. The cart-abandonment list page (updated 2025-09-22) still prints an older US average of 14.88 fields; that figure is legacy and is not used.
