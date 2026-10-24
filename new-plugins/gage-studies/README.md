# Gage Studies

Review Gage R&R results and measurement tables to decide whether a measurement system is acceptable. For metrologists and quality engineers in machining, molding, electronics and test laboratories. You paste or export the software output or the raw part, operator and trial readings; no account, connector or installation is needed.

| Skill | What you get |
|---|---|
| gage-rr-review | Verdict band per purpose (process control or sorting against tolerance), the deciding figure with its denominator, design and chart issues that change the verdict, and the questions still open |
| gage-rr-calculate | Crossed Gage R&R from raw readings: ANOVA table, interaction test, variance components, %Contribution, %Study Var, %Tolerance and distinct categories, with formulas and inputs |
| gage-study-plan | A study plan: crossed, nested, expanded or Type 1; number of parts, operators and trials; part selection, run order and the figures to report |

Try: "Is my gage R&R acceptable? Here is the Minitab session output", "Run a gage R&R on this table", "Our engineer says 7% contribution passes, is that right?", "How do I do GRR on a destructive pull test?"

## What it knows

The skills carry the conventions that most often change a verdict: which acceptance bands belong to which column (10/30% on study variation and tolerance, 1/9% on variance contribution), how %Tolerance is computed with one specification limit, the 6 versus 5.15 multiplier, how distinct categories are calculated and truncated, when the operator-by-part interaction is dropped, why a printed zero variance component may be a negative estimate, what the Xbar and R charts in the output should look like, and when a destructive test needs a nested or expanded design. Each rule has a dated source in [references](references/official-sources.md). The guidelines come from Minitab's documentation of the AIAG Measurement Systems Analysis manual (4th edition) and the NIST/SEMATECH e-Handbook. Customer manuals and company procedures you name take precedence.

## Limits

The plugin works only from the data you supply. It refuses a verdict when the data cannot support one, for example with a single trial per part or an unknown output column. It does not qualify a gage, issue calibration certificates or release product. Its results support the sign-off of the qualified metrologist or quality engineer; they do not replace it. Attribute agreement studies are out of scope for this version.

## Network and data

This is a skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. It contains no scripts, servers, connectors or hooks and makes no network requests. If your assistant has a code tool, the calculation skill may use it locally to execute the arithmetic on the data you supplied. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
