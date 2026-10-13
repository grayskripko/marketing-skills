# FMEA Linkage

Check that your process flow diagram, PFMEA, control plan and work instructions agree, operation by operation and characteristic by characteristic, and find every row to update after a change. For process-quality engineers and FMEA facilitators at machining, moulding, casting, stamping and electronics suppliers. You paste the rows from your documents into the request; no account or connector is needed. Ford's requirements effective 15 June 2026 are built in; for other customers, paste their requirements.

| Skill | What you get |
|---|---|
| pfmea-linkage-check | The broken links between flow, PFMEA, control plan and work instructions, each with the source rows that show it: missing steps, specification and control conflicts, special characteristics not carried through, stale revisions, mismatched reaction plans |
| pfmea-change-update | After a drawing revision, process change, new control or 8D action: every row to change, document by document, with the old and new text, and any rows still carrying the old value |

Try: "Does our control plan match the PFMEA? Rows below", "Check op 10 to op 60 across flow, PFMEA, CP and WIs", "Drawing went from rev C to rev D, what changes in the PFMEA and control plan?", "Carry this 8D root cause into the FMEA and control plan".

## What it knows

The skills match rows by operation number, characteristic number, control method and revision, in both directions, applying any approved renumbering the user supplies, and cite the rows behind each finding. They know where linkage most often breaks: a PFMEA that claims 100% gauging while the control plan samples; a work instruction with a different frequency or a reaction plan without steps; a special characteristic whose class is dropped downstream; rework steps that are in the flow but nowhere else; back-up controls kept in one document only; a control plan still at the old change level. They apply IATF 16949 sanctioned interpretations and FAQs on special-characteristic cascade, control plan content, MES-linked control plans and alternate controls, and Ford's PPAP and IATF 16949 customer-specific requirements: DFMEA to PFMEA to control plan to process instructions traceability, SCCAF linkage, part and foundation FMEA alignment, CC controls that prevent shipment, reaction plans with specific steps, and the Ford symbol rules. Each rule has a dated source in [references](references/official-sources.md). The AIAG & VDA FMEA Handbook, the AIAG Control Plan manual and IATF 16949 itself are not reproduced.

## Limits

The plugin works only from the rows you paste. It does not find new failure modes or rate severity, occurrence or detection.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
