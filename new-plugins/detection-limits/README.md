# Detection Limits

Check EPA method detection limit (MDL) studies and annual verifications under 40 CFR 136 Appendix B, Revision 2, and keep your MDL tables in line with them. For technical managers, QA officers and data reviewers at environmental and QC laboratories. You paste the spike and blank results, the lab's calculation output or MDL table into the request; no account, connector or setup is needed.

| Skill | What you get |
|---|---|
| mdl-study-check | The MDL for an initial study, recomputed from your spikes and blanks, with the data or calculation problems that change it |
| mdl-annual-verification | Whether the existing MDL can stay, the verified MDL, and missing quarterly spikes or wrongly included data |
| mdl-table-reconcile | The rows of a LIMS, SOP or report MDL table that disagree with the latest study, are stale or are missing, with the replacement value |

Try: "Check this MDL study for lead and recompute the MDL", "Can we keep our MDLs after this year's verification?", "Which MDLs in our LIMS table are out of date?"

## What it does

Each skill first lines up your records: analyte names and CAS numbers, matrix, instrument, batch, preparation and analysis dates, spike level and units. It catches results that appear in one record and not the other, unit slips, mixed spike levels, wrong counts and stale values, then applies the Revision 2 rules where a plain answer often goes wrong: seven spikes and seven blanks over three dates, per-instrument minimums, ND versus numerical blanks in MDLb, the 99th-percentile rule for 100 or more blanks, the 13-month and 24-month windows, and the 0.5–2.0× plus 3% test for keeping an existing MDL. Each rule has a dated source in [references](references/official-sources.md).

It does not set reporting limits or LOQs, and it keeps EPA MDLs separate from ICH Q2 detection and quantitation limits.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. It works only on what you paste into the request. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
