# Flare Records

Turn pasted refinery and chemical-plant flare data into 15-minute compliance blocks, and find where the flare records disagree with each other. For environmental and flare-compliance engineers at refineries and petrochemical plants, and for the emissions consultants who prepare their reports. You paste historian rows, routing and pilot logs, gas analysis results, visible-emission observations or a draft report table into the request; no account or connector is needed.

| Skill | What you get |
|---|---|
| flare-blocks | The 15-minute block table with NHVvg, NHVcz, NHVdil and tip velocity worked from your flows and gas analysis, pilot-deviation blocks, and the blocks that fall below a limit or cannot be calculated |
| flare-discrepancies | One record per mismatch between your logs: routing vs historian flow, pilot signal vs routing, superseded lab revisions, missing daily Method 22 observations, root-cause events and a draft periodic report vs the block evidence |

Try: "Which of these blocks were below 270 Btu/scf?", "Was the pilot loss at 02:12 a deviation?", "Reconcile our draft semiannual flare table against these logs", "The lab reissued this GC result, which blocks change?"

## What it knows

The skills carry the 40 CFR 63.670 and 63.671 rules that decide a block: fixed blocks from midnight, the one-minute pilot rule, the 270 and 800 Btu/scf NHVcz limits, the NHVcz, NHVdil, Vtip and Vmax equations, the Table 12 heating values (hydrogen counts as 1,212 Btu/scf, not 274), which gas result belongs to which block under the direct, feed-forward and grab-sample methods, exclusion of out-of-control data, and the daily visible-emission and 45-day root-cause triggers. They also carry the changes the HON (63.108) and ethylene (63.1103) rules make to the refinery text. Each rule has a dated source in [references](references/official-sources.md). Your permit, monitoring plan and any approved site-specific limits take precedence.

## Limits

It does not give supplemental gas, steam or valve settings or shutdown advice, and its discrepancy records are candidates for your review, not compliance findings. It does not cover Subpart Ja H2S limits, LDAR or tank emission estimates.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/discussions)
