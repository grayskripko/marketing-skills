# Remittance Denials

Explain insurance denial codes and EOB adjustments, and identify the evidence needed to correct or appeal them.
Checks supplied US ERA/EOB group codes, CARCs, RARCs and payer notes for code-usage conflicts and deciding evidence.
For US medical billing teams working from pasted text or ERA/EOB exports. Needs group codes, CARCs, RARCs, payer notes and claim/line labels; anonymous labels work. No account, key, connector or paid API is required.

## Skills

- **explain-remittance** — explains each adjustment, responsibility shown, conflicting code usage and missing context.
- **denial-evidence** — builds a correction or appeal evidence worklist tied to the actual adjustment and supplied payer policy.

Paste de-identified rows or provide a local text/CSV export. Include remittance date, payer type, billed/paid/adjustment amounts and which remarks belong to which line when available. For payer-specific next steps, supply a public policy URL or excerpt. No setup is needed.

## Sources and network

The assistant fetches public X12 CARC/RARC pages and the X12 code-update listing to verify the codes in your case, plus relevant CMS remittance and Original Medicare redetermination and timely-filing manual pages. It may search those official domains using code IDs or policy names only. A payer policy is read from a public URL you supply; direct fetches include the site's robots.txt and normal redirects. Claim text and identifiers are never included in public queries or URLs. No login or subscription download is used. If a lookup is unavailable, the result identifies the exact source or policy needed. There is no telemetry or plugin storage.

Dated decision notes are embedded in each skill's references. They cover qualifying remarks, restricted group combinations, adjustment amount constraints, provider-level separation and Original Medicare correction versus appeal procedure. Code pages were read 2026-10-11.

## Examples

“Explain CO16 with M51 on this exported service line and tell us what field evidence is missing.”
“Build an evidence checklist for this timely-filing denial using the receipt history and payer policy below.”

[Privacy](PRIVACY.md) · [License](LICENSE)
