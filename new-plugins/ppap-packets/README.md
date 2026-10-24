# PPAP Packets

Check a PPAP package before it goes to the customer. Paste the submission index, document headers or excerpts, the drawing revision and the customer checklist, and get an element-by-element status matrix that catches stale revisions, wrong part numbers, missing cavities, date-order problems and broken special-characteristic links, with the questions a reviewer would ask. For supplier-quality and APQP engineers and PPAP coordinators at automotive suppliers. No account or connector is needed. Ford's PPAP requirements effective 15 June 2026 are built in; for other customers, paste their checklist.

| Skill | What you get |
|---|---|
| ppap-package-review | A matrix of checklist elements against files, with the identifier found in each and its status (matched, wrong part, coverage gap, date order, conflict, indexed only, missing), then reviewer questions for the open rows |
| ppap-dimensional-results | Every balloon matched to its measurements per part and cavity, pass or fail recomputed from nominal and tolerance, unmeasured and extra balloons, part-count and cavity gaps, and recomputed Ppk and gauge R&R figures with their formulas |
| ppap-special-characteristics | Each CC, SC, HI or OS characteristic traced from drawing and SCCAF through PFMEA, control plan, work instructions and capability, with the breaks and the fix for each |

Try: "Is this PPAP complete for Ford level 3? Index and headers below", "Match these dimensional results to drawing rev D, two cavities", "Is every CC on the SCCAF in our control plan?", "Is a Ppk of 1.58 on 125 readings enough for Ford?"

## What it knows

The skills match identifiers across documents: part number with prefix and suffix, drawing revision and change level, dates, cavities and characteristic numbers. For Ford they apply the PPAP and IATF 16949 customer-specific requirements effective 15 June 2026: design-record alignment, WERS Alert and Jira deviation status, at least 5 parts and every cavity in dimensional results, gauge study before capability study, gauge R&R bands of 10% and 30%, Ppk 1.67 on 125 readings, heat-treat sampling, CC controls that prevent shipment, sub-tier evidence, electronic PSW and its exceptions, and ISO/IEC 17025 compliance without accreditation for labs. Each rule has a dated source in [references](references/official-sources.md). The AIAG and IATF manuals are not reproduced.

## Limits

The plugin works only from what you paste. A file named in the index without its content cannot be confirmed. It does not sign, submit or upload a PSW.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
