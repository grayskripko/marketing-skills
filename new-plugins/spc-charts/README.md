# SPC Charts

Make SPC control charts and calculate control limits from your inspection data, list every out-of-control signal with its source row, and check Cpk and Ppk when the data support it. For quality and process engineers in factories and industrial QC labs. You need chronological measurements or counts pasted in your request or as an export (CSV, spreadsheet) you name or attach for it, with units and how the samples were taken. No account, API key, connector or install.

| Skill | Result |
|---|---|
| control-chart-setup | Chart choice, baseline, center line and limits with formulas, frozen rule set, computed chart |
| control-chart-signals | Signal register against frozen limits: rule, rows, values, what to investigate |
| process-capability | Cp, Cpk, Pp, Ppk with formulas, or a clear list of what is missing before any verdict |

Try "Set up an I-MR chart for these readings", "Check this week's points against our limits with Western Electric rules", or "Is this feature capable? Spec is 12.00 ± 0.05".

## How it works

The skills follow the Shewhart chart family of ISO 7870-2:2023, the formulas of the NIST/SEMATECH e-Handbook of Statistical Methods, and the data guidance of common SPC software. Each limit and index is shown with its formula and inputs. Every plotted point keeps its source row, so the result can be audited.

Missing information limits the conclusions supported by the data; usable descriptive charts and calculations can still be provided. Short baselines give preliminary limits, clearly marked. Points are never deleted to remove a signal. Results support, but do not replace, the sign-off of your quality engineer and your customer's requirements. If your customer names a specific SPC manual or edition, that document governs.

Not covered: gage R&R and measurement system studies, designed experiments, reliability analysis, lab out-of-specification investigations, live production control or product release.

## What this package runs and connects to

This is a skills-only package: Markdown instructions and references, JSON metadata, an MIT license and a static SVG icon. It bundles no scripts, dependencies, hooks, MCP servers or background processes. It makes no network requests and has no telemetry. When your assistant can run local code, the skills may compute limits and draw the chart in a local script using the assistant's existing tools, and save it where you ask. Otherwise the arithmetic is shown in the answer.

[Sources](references/sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
