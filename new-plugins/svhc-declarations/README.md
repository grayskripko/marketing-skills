# SVHC Declarations

Check supplier SVHC declarations against your bill of materials and the REACH Candidate List, then write the Article 33 notice for customers and the follow-up request to suppliers. For product-stewardship and supplier-quality engineers at component makers and distributors selling into the EU. You paste the BOM rows, part masses and supplier statements into the chat; no account or connector is needed.

| Skill | What you get |
|---|---|
| svhc-coverage-check | One row per part: the matched declaration, the Candidate List date it covers, any SVHC above 0.1% of the component with the arithmetic, and the gap (stale, near-match part number, no declaration, wrong basis) |
| svhc-article-notice | The Article 33 notice for business customers, or the reply to a consumer request with its 45-day due date |
| svhc-supplier-requests | An email to the supplier with one numbered request per open part: exact part number, list entries still to cover, mass basis |

Try: "Which of these parts have no SVHC declaration that covers the February 2026 list?", "A customer asks if our HX-40 contains SVHCs, draft the reply", "Ask Kestrin for an updated declaration for these three cables".

## What it knows

The skills match part numbers and revisions exactly, date each declaration against the list it covers, and compute concentrations on the right basis. They carry the current Candidate List state (253 entries, last updated 4 February 2026, next update expected June 2027) and the entry count after each update since 2023, so a declaration that says "250 substances" can be traced to the June 2025 list and its missing entries named. They apply the 0.1% threshold to each component, not the whole product (Court of Justice C-106/14), convert homogeneous-material and ppm figures to the component, and follow ECHA's rules for adhesives, coatings and packaging. Each rule has a dated official source in [references](references/official-sources.md): the REACH text, the C-106/14 judgment, the ECHA Candidate List table and ECHA guidance on substances in articles.

## Limits

The skills work only from what you paste. A part with no declaration is reported as missing, never as free of SVHCs. They do not cover REACH restrictions or authorisation, RoHS, SCIP dossier entry or ECHA notifications beyond saying when one applies.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. Messages are drafts; nothing is sent. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
