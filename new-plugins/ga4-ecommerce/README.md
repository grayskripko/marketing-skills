# GA4 Ecommerce

Check my GA4 ecommerce events and map purchases and refunds to my order facts, then give me field-level defects and corrected example payloads.
For ecommerce analysts and developers reviewing GA4 or GTM instrumentation. Needs pasted event messages or readable exports and matching order/refund facts. No account, keys, installation or paid API is needed.

## Jobs

- **ecommerce-field-check:** Check exact field paths, numbers, currency, item fields and GTM state; return defects and corrected examples in the supplied transport.
- **purchase-refund-map:** Link purchases and returns to supplied orders; distinguish full and partial refunds, preserve original transaction IDs, and reconcile merchandise separately from tax and shipping.

Paste messages as text, or supply readable JSON/CSV exports. Include order IDs when available, currency, net unit prices, quantities, tax, shipping and refunded merchandise. Aggregate-only facts produce an aggregate reconciliation and precise missing details for item examples.

Routine use fetches nothing. A requested source refresh reads only the Google Developers, Analytics Help and Firebase documentation URLs in the bundled field register. The package includes no connector, executable service or telemetry. It drafts text and payload examples.

## Examples of requests

“Check these purchase pushes against the order totals.”
“Map these partial refunds to their original purchases.”
“Only these aggregate facts are available; reconcile the event totals.”

Sources were checked on 2026-10-11. Source dates, decisions and validation evidence are in BUILD-NOTES.md and tests/.
