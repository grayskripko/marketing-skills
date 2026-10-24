# Sources

Every URL below was opened on 2026-10-12 and the stated passage was read on the page. The package makes no network requests at run time; these are build-time sources. Section numbers are those printed on the page. Where a figure is our own recomputation, it says so.

## Standards

### IEC 61649:2008 — Weibull analysis
https://webstore.iec.ch/en/publication/5698 — read 2026-10-12.
Edition 2.0, published 2008-08-13, TC 56 Dependability, stability date 2027. Scope: methods for analysing data from a Weibull distribution (time, cycles, stress) for random samples tested or in service, to estimate population reliability; edition 2 adds analytical methods to graphical ones and replaces IEC 61649:1997. Cited as the standard for Weibull analysis. The full text is sold; no clause from inside it is quoted in the skills.

### IEC 61710:2013 — Power law model: goodness-of-fit tests and estimation methods
https://webstore.iec.ch/en/publication/5732 — read 2026-10-12.
Edition 2.0, 2013-05-22, TC 56. Covers parameter estimation, confidence intervals for failure intensity, prediction intervals and goodness-of-fit for the power-law model of repairable items; assumes data from one item or identical items under the same conditions. Cited for the repairable-system model; formulas used come from NIST below.

## NIST/SEMATECH e-Handbook of Statistical Methods, chapter 8 (current hosted pages, undated)

### §8.1.3.1 Censoring
https://www.itl.nist.gov/div898/handbook/apr/section1/apr131.htm — read 2026-10-12.
Type I (fixed time T; survivors give only a lower bound), Type II (stop at r-th failure), readout/interval, multicensored. With several failure modes, analyse each separately and treat other modes' failures as censoring times.

### §8.1.3.2 Lack of failures
https://www.itl.nist.gov/div898/handbook/apr/section1/apr132.htm — read 2026-10-12.
Precision of estimates varies inversely with the square root of the number of failures, not units on test or test length; 5 failures out of 10 tell more than 2 out of 1000.

### §8.1.6.2 Weibull
https://www.itl.nist.gov/div898/handbook/apr/section1/apr162.htm — read 2026-10-12.
F(t) = 1 − exp[−(t/α)^γ], R(t), h(t) = (γ/α)(t/α)^(γ−1), mean α Γ(1 + 1/γ); γ = 1 is exponential. Three-parameter form: no failure before the location μ; if μ is known subtract it and fit two parameters. Symbols vary; some software swaps α and β roles.

### §8.1.7.2 NHPP power law
https://www.itl.nist.gov/div898/handbook/apr/section1/apr172.htm — read 2026-10-12.
M(t) = a t^b; also called Duane or AMSAA model. The "Weibull process" name is misleading and should be avoided because it mixes a non-repairable life distribution with repair inter-arrival times.

### §8.1.8.1 Competing risk model
https://www.itl.nist.gov/div898/handbook/apr/section1/apr181.htm — read 2026-10-12.
If modes are independent and the first mode to fail ends the unit: R_c = Π R_i, h_c = Σ h_i. Analyse each mode with other modes as censored run times.

### §8.2.1.1 Based on failure mode
https://www.itl.nist.gov/div898/handbook/apr/section2/apr211.htm — read 2026-10-12.
Life distribution and acceleration models typically apply only at the individual failure-mode level.

### §8.2.1.5 Kaplan-Meier
https://www.itl.nist.gov/div898/handbook/apr/section2/apr215.htm — read 2026-10-12.
K-M needs exact failure times; censored units count in the risk set only up to their removal. Modified K-M for plotting: R(t_i) = [(n+0.7)/(n+0.4)] Π_{j∈S, t_j ≤ t_i} (n − j + 0.7)/(n − j + 1.7).

### §8.2.2.1 Probability plotting
https://www.itl.nist.gov/div898/handbook/apr/section2/apr221.htm — read 2026-10-12.
Median-rank positions 100(i − 0.3)/(n + 0.4) with n units on test; readout positions 100 Σ r_i / n; modified K-M for multicensored data. Plot each failure mode separately. Weibull plot: log ln[1/(1−F)] vs log t, slope = shape. First few points vary most. Worked example: 20 units, 10 failures by 500 h; regression of log y on log x gives slope 1.46 and α = 657. Our recomputation: 657 follows from the rounded slope; with the unrounded slope α ≈ 667.

### §8.2.3.4 Trend tests
https://www.itl.nist.gov/div898/handbook/apr/section2/apr234.htm — read 2026-10-12.
Reverse arrangement test with one-sided critical tables for r = 4–12 and normal approximation for r > 12; Military Handbook test χ² = 2 Σ ln(T_end/T_i), df 2r; Laplace test z = √(12r) Σ(T_i − T_end/2)/(r T_end). Small numbers of repairs rarely give significant results. Note: the page's prose pairs high Laplace values with improvement, but its own improvement case study (failures 5 … 1478 h, end 1500 h) gives z ≈ −1.33 by our recomputation; the skills follow the formula's sign (positive = failures late = rate rising).

### §8.3.1.2 Lognormal or Weibull tests
https://www.itl.nist.gov/div898/handbook/apr/section3/apr312.htm — read 2026-10-12.
No two-parameter estimate without at least two failures. At least 10 exact failures usually give reasonable estimates; below 10 the shape may be hard to estimate; below 5 estimates are often very inaccurate. Readout data need failures in three or more intervals. Known-shape plans: α_u = AT / [−ln(1 − p0)]^(1/γ0).

### §8.4.1.2 Maximum likelihood estimation
https://www.itl.nist.gov/div898/handbook/apr/section4/apr412.htm — read 2026-10-12.
MLE handles every form of censoring. With fewer than 5 failures (sometimes fewer than 10) MLEs can be heavily biased and large-sample properties do not apply.

### §8.4.1.3 Weibull MLE example
https://www.itl.nist.gov/div898/handbook/apr/section4/apr413.htm — read 2026-10-12.
20 units, failures at 54, 187, 216, 240, 244, 335, 361, 373, 375, 386 h, 10 survivors at 500 h. MLE η = 606.5280 h, β = 1.7208, mean 540.737 h, log-likelihood −75.135; AIC 154.27 Weibull vs 154.39 lognormal. Our recomputation reproduces these; fitting the 10 failures alone gives β ≈ 3.06, η ≈ 309 h.

### §8.4.5.1 Constant repair rate (HPP) model
https://www.itl.nist.gov/div898/handbook/apr/section4/apr451.htm — read 2026-10-12.
MTBF = total operating time / failures (the MLE, censored or complete). Confidence-factor tables; a two-sided 100(1−α) % interval's ends are one-sided 100(1−α/2) % bounds; r = 0 gives only a lower bound (80 % table 0-row lower factor 0.4343).

### §8.4.5.2 Power law (Duane) model
https://www.itl.nist.gov/div898/handbook/apr/section4/apr452.htm — read 2026-10-12.
Time-truncated bias-corrected estimate b = (r − 1)/Σ ln(T/t_i); case study failures 5, 40, 43, 175, 389, 712, 747, 795, 1299, 1478 h, end 1500 h.

## Software documentation (vendor conventions that change results)

### Minitab — least squares vs maximum likelihood
https://support.minitab.com/en-us/minitab/help-and-how-to/statistical-modeling/reliability/supporting-topics/estimation-methods/least-squares-and-maximum-likelihood-estimation-methods/ — read 2026-10-12.
MLE is Minitab's default and performs better than least squares with few failures. Least squares regresses time (X) on transformed percent (Y), ignores censored observations, and reports no standard errors, confidence intervals or parameter tests.

### Minitab — probability plot points (right censoring)
https://support.minitab.com/en-us/minitab/help-and-how-to/statistical-modeling/reliability/how-to/parametric-distribution-analysis-right-censoring/methods-and-formulas/probability-plot — read 2026-10-12.
Methods: median rank (Benard, default), modified Kaplan-Meier, Herd-Johnson, Kaplan-Meier. Ties containing failures and suspensions: failures are treated as occurring before suspensions.

### Minitab — goodness of fit, Distribution ID plot
https://support.minitab.com/en-us/minitab/help-and-how-to/statistical-modeling/reliability/how-to/distribution-id-plot-right-censoring/interpret-the-results/goodness-of-fit — read 2026-10-12.
Smaller Anderson-Darling (adj) generally means better fit; with least squares a correlation coefficient (≤ 1, higher better) is shown. Slight differences may not be practically relevant; values for different distributions may not be directly comparable; use the plots too.

### ReliaSoft (HBM Prenscia) — The Weibull distribution reference
https://help.reliasoft.com/reference/life_data_analysis/lda/the_weibull_distribution.html — read 2026-10-12.
Rank regression on Y minimises vertical deviations, on X horizontal. Third parameter used when data do not fall on a straight line; a negative location may indicate failures before the test start; MLE asymptotic properties do not hold for the location. Fisher-matrix bounds on regression results are theoretically not applicable. β < 1 decreasing, = 1 constant, > 1 increasing failure rate. Likelihood-ratio bounds: −2 ln[L(θ)/L(θ̂)] = χ²(α; 1).

### JMP — Weibayes report
https://www.jmp.com/support/help/en/19.1/jmp/weibayes-report.shtml — read 2026-10-12.
Zero-failure data get a Weibayes analysis with a user-set Weibull β, following Nelson (1985); when at least one failure is present the full report appears, and the page notes its maximum likelihood results might not be useful, so Weibayes may be preferable.

## Derived results and rules of thumb (no external source)

- B-life t_p = η[−ln(1 − p)]^(1/β): algebra from the NIST CDF (§8.1.6.2).
- Weibayes zero-failure bound η_L = [Σ t_i^β / (−ln(1 − C))]^(1/β): from R(t) and P(no failure) = Π R(t_i). Cross-check: β = 1, C = 0.90 gives factor 0.4343, matching NIST §8.4.5.1.
- Power-law current intensity r b / T_end and current MTBF T_end/(r b): from M(t) = a t^b with a = r / T^b.
- Rule of thumb of this plugin: age basis (calendar vs run time), units already in service before records began (left truncation), and pooling across designs, suppliers or duty are flagged as questions, not silently pooled.
- Rule of thumb of this plugin: when two distributions fit comparably, report the lower B-life alongside the other.
