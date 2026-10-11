# Sources and authored decisions

Provenance only: execution rules are in the relevant SKILL.md; this file adds no separate workflow. Consult it when source attribution is needed. CSV-specific notes apply only during CSV preparation.

Read 2026-10-10. Platform scope: Shopify product CSV, not an API integration.

- https://help.shopify.com/en/manual/products/import-export/using-csv — current and legacy headers; required fields; column dependencies; variant and continuation rows; CSV encoding; blank versus omitted update cells; overwrite handling; changes to option values and variant IDs; inventory and metafield boundaries; SEO field limits. Core deciding rules are inline in the CSV skill.
- https://help.shopify.com/en/manual/products/details/product-descriptions/generate — Shopify warns generated product descriptions can add benefits or facts not supplied, and merchants must review accuracy. Used to motivate supplied-facts-only drafting, not to claim access to Shopify Magic.

Authored rules of thumb, not platform requirements: brief titles and snippets, useful tags from supplied facts, corrected deliverable first, the minimum necessary questions (one by default for one blocker), draft/unpublished defaults for new rows, smallest valid update, backups and representative import trials (one product by default for homogeneous batches), no automatic URL fetches. These choices avoid unsupported claims and broad changes. No keyword volume or conversion uplift is asserted.

Answer presentation: use the requested fields or file as the answer, with product-specific constraints incorporated where they matter. Paste-ready copy uses labelled fields per SKU; label proposals do not require an import export. Copy-only updates can omit untouched columns, while requested corrected full exports retain their full rows and unchanged cells; targeted SKU updates use the smallest dependency-complete file with the relevant variant mapping. Report parsing only after running it on the final CSV. These presentation choices do not relax the source-bound claims or import safeguards above.
