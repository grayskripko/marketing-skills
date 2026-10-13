# Mill Certificates

Check mill test certificates (MTRs, MTCs, EN 10204 3.1 and 3.2) against your purchase order and material specification, and trace every received item to its heat. For receiving QA inspectors, material controllers and supplier-quality engineers at stockholders, fabricators and equipment makers. You paste the certificate text, PO lines and receiving rows, or an export of them; no account or connector is needed. Grade limits come from your PO or your own licensed copy of the specification.

| Skill | What you get |
|---|---|
| mill-cert-review | A requirement-by-requirement table: value as printed, converted value with formula, test condition and status (meets, does not meet, missing, not required, cannot compare), the certificate-type finding on its own line, and supplier questions |
| heat-traceability | A register with one row per received item linked to certificate, heat, piece or test number, grade and quantity, with exceptions for unmatched and near-match heats, quantities over the certificate, stockist paperwork and lost markings |
| cert-supplier-queries | A message to the supplier, stockist or mill with one numbered request per open point and the document that would close it |

Try: "Does this MTR meet PO 4410 line 3?", "Is a 2.2 test report OK when we ordered 3.1?", "Match these receiving rows to the certs by heat", "Ask the stockist for the mill cert and the missing Charpy results".

## What it knows

The skills carry the conventions that most often change a receiving decision: the difference between certificate type and material grade; what EN 10204 2.1, 2.2, 3.1 and 3.2 contain and who validates them; how the 1991 names (3.1.B, 3.1.C) map to today's types; why an "intent of 3.2" is not a 3.2; the PED rules on certificates of specific product control, stockist paperwork and who counts as the material manufacturer; ladle versus product analysis; the IIW carbon equivalent and Pcm formulas; ReH versus Rp0.2; elongation gauge lengths; Charpy averages, the 70% single-value rule, sub-size specimen factors and retests; ksi, kgf/mm², ft·lbf and °F conversions; and US Buy America and nuclear traceability rules where a PO invokes them. Each rule has a dated source in [references](references/official-sources.md): the PED and its Commission guidelines, IACS Unified Requirements W2 and W11, 10 CFR 50 Appendix B, 23 CFR 635.410, NIST SP 811 and inspection-body guidance on EN 10204. Your PO, customer requirements and governing code take precedence.

## Limits

The plugin works only from the data you supply. It refuses a conclusion when the data cannot support one, for example when no requirement or limit is given, a value is unreadable in a scan, or the unit or test condition is unknown. It does not authenticate certificates, accept material or release heats. Its results support the sign-off of the qualified receiving inspector or materials engineer; they do not replace it.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. Supplier messages are drafts; nothing is sent. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
