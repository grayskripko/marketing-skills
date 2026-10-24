# Weibull Analysis

Fit and review Weibull analyses of component failure and suspension data: shape (beta), scale (eta), B10 life and confidence bounds. For reliability and equipment-test engineers at OEMs, test laboratories and asset-intensive plants. You paste or export ages with failed/survived flags, repair histories, or the output of Minitab, Weibull++, JMP, Python, R or a spreadsheet; no account, connector or installation is needed.

| Skill | What you get |
|---|---|
| weibull-life-fit | A data check (one unit per row, censor flags, failure modes, age basis, failure count), then an MLE Weibull fit with survivors kept as suspensions: beta, eta, B-life, likelihood-ratio bounds, a lognormal comparison, or a clear "not estimable" verdict. Zero-failure Weibayes bounds when you supply a prior shape. |
| weibull-results-review | A verdict on someone else's Weibull output or report: dropped survivors, flipped censor flags, mixed modes, swapped parameter labels, regression direction, unsupported confidence statements, extrapolated B-lives — each with the figure that proves it. |
| repair-trend-check | For repairable equipment: reverse-arrangement, Military Handbook and Laplace trend tests on the repair history, then a constant-rate or power-law (Crow-AMSAA) model and the current MTBF, before anyone fits Weibull to times between failures. |

Try: "Run a Weibull on these 14 pump bearings, 6 failed", "Most of our units are still running, can I still get a B10?", "Why does Minitab give beta 1.6 and Excel 1.46?", "Check this supplier's B1 life claim", "Are failures on compressor C-2 getting more frequent?"

## What it knows

The skills carry the conventions that most often change a Weibull result: keeping survivors as suspensions (dropping them halved the scale in the NIST worked example), mapping the censor flag, separating failure modes and treating other modes as suspensions, the failure counts below which estimates are unreliable (2, 5, 10), median-rank and modified Kaplan-Meier plotting positions, which way rank regression runs in Minitab versus the NIST example, why least-squares fits in Minitab carry no confidence intervals, one- versus two-sided bounds, when a three-parameter fit is justified, Weibayes with an assumed shape, and why a "Weibull process" on repair data is the wrong model until a trend test says otherwise. Each rule has a dated source in [Sources](references/official-sources.md): IEC 61649:2008 (Weibull analysis), IEC 61710:2013 (power-law model), the NIST/SEMATECH e-Handbook chapter 8, and Minitab, ReliaSoft and JMP documentation. Company or customer procedures you name take precedence.

## Limits

The plugin works only from the data you supply and refuses a conclusion the data cannot carry, for example a shape estimate from one failure or a confidence bound the software never computed. It does not set replacement or overhaul intervals, remaining safe life, fitness-for-service or certification. Its results support the sign-off of the qualified reliability engineer or safety review; they do not replace it. Accelerated life testing models and degradation analysis are out of scope for this version.

## Network and data

Skills-only package: Markdown instructions, a reference file, JSON metadata, a license and an SVG icon. No scripts, servers, connectors or hooks, and no network requests. If your assistant has a code tool, the skills may use it locally to compute fits and test statistics on the data you supplied. The publisher receives no data. See [Privacy](PRIVACY.md).

[Sources](references/official-sources.md) · [Privacy](PRIVACY.md) · [MIT license](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
