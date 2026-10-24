# Sources for gage study rules

Every page below was opened on 2026-10-12. The package makes no network requests at run time; these notes were embedded when it was built. Minitab pages are current, undated vendor documentation. Where Minitab quotes the AIAG Measurement Systems Analysis manual (MSA, 4th edition, 2010), the guidance is attributed to AIAG by Minitab; the manual itself is sold by AIAG and was not opened. Customer requirements, company procedures and the application decide approval; these are guidelines, not regulatory limits.

## 1. Acceptance bands differ by output column

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/supporting-topics/gage-r-r-and-wheeler-s-emp-studies/is-my-measurement-system-acceptable/ — read 2026-10-12.

- AIAG-attributed guidance on Total Gage R&R in %Study Var (also applied to %Tolerance and %Process): under 10% acceptable; 10% to 30% acceptable depending on application, cost of the measurement device, cost of repair or other factors; over 30% not acceptable.
- Variance-component guidance on %Contribution: under 1% acceptable; 1% to 9% acceptable depending on application and costs; over 9% not acceptable.
- Number of distinct categories: 5 or more.
- The 1/9 bands are the squares of the 10/30 bands (0.10² = 0.01; 0.30² = 0.09). Using 10/30 on %Contribution is a common error: 9% contribution already equals 30% study variation. (Arithmetic of this plugin, consistent with section 3.)

## 2. Number of distinct categories

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/supporting-topics/gage-r-r-and-wheeler-s-emp-studies/using-the-number-of-distinct-categories-in-a-gage-r-r-study/ — read 2026-10-12.

- ndc = 1.41 × (StdDev Parts / StdDev Gage), truncated; set to 1 if below 1.
- AIAG recommends 5 or more. Below 2 the system is of no value for controlling the process; 2 splits parts only into high/low, 3 into low/middle/high.

## 3. Crossed Gage R&R formulas (ANOVA method)

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/methods-and-formulas/gage-r-r-table/ — read 2026-10-12 (formula images opened).

Notation: a = number of parts, b = number of operators, n = number of replicates.
- Full model: Repeatability = MS_Repeatability; Operator = (MS_Operator − MS_Operator×Part)/(a·n); Operator×Part = (MS_Operator×Part − MS_Repeatability)/n; Part-to-Part = (MS_Part − MS_Operator×Part)/(b·n).
- Reduced model (interaction removed): Operator = (MS_Operator − MS_Repeatability)/(a·n); Part-to-Part = (MS_Part − MS_Repeatability)/(b·n).
- Reproducibility = Operator + Operator×Part (full) or Operator (reduced). Total Gage R&R = Repeatability + Reproducibility. Total Variation = Total Gage R&R + Part-to-Part.
- A negative variance component is reported as zero.
- %Contribution = VarComp/Total VarComp × 100, sums to 100. StdDev = √VarComp. Study Var = 6 × StdDev (or the chosen multiplier). %Study Var = Study Var/Total Study Var × 100; it is the square root of %Contribution and does not sum to 100.
- %Tolerance = Study Var / (USL − LSL) × 100.
- %Process = Study Var / (6 × historical standard deviation) × 100.

## 4. ANOVA versus Xbar-R, interaction removal, one operator

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/perform-the-analysis/enter-your-data/ — read 2026-10-12.

- "The ANOVA method usually estimates the variances more accurately and provides more information about interactions."
- The Xbar and R method cannot calculate the operator-by-part interaction variance.
- With one operator, leave Operators empty and use ANOVA.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/methods-and-formulas/method-of-analysis/ — read 2026-10-12.

- Interaction removed when its p-value is greater than or equal to alpha (default 0.05); the reduced model has Part and Operator main effects only.
- Xbar-R: repeatability from the average within-cell range, reproducibility from the range of operator averages, part-to-part from the range of part averages, all divided by the appropriate d2.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/perform-the-analysis/specify-the-options/ — read 2026-10-12.

- Default study variation multiplier 6 (99.73%). Alpha to remove interaction is user-set; 0.10 or 0.25 keep the interaction more often, 0.01 less often.
- Historical standard deviation = known total variation (part-to-part plus measurement), used instead of the estimate from the study parts.

## 5. One-sided tolerance

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/supporting-topics/gage-r-r-and-wheeler-s-emp-studies/calculation-of-percent-tolerance-with-a-one-sided-tolerance/ — read 2026-10-12.

- One-sided %Tolerance = (Study Var / 2) / |spec limit − mean of all measurements| × 100.
- Not calculated when the overall mean lies beyond the specification limit.

## 6. Crossed study design

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/before-you-start/data-considerations/ — read 2026-10-12.

- At least 10 parts; 15 to 35 parts give a much better estimate when no historical process variation is available; 10 is acceptable with a historical estimate.
- 3 to 5 operators; not fewer than 3 unless fewer people use the system. Choose operators at random; only the best or worst biases results.
- Each operator measures each part at least twice, all parts in random order within a replicate.
- Parts from the entire process range; not consecutive parts, one shift or line, or the reject pile.
- Crossed: every operator measures every part.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/before-you-start/overview/ — read 2026-10-12.

- Crossed requires a balanced design with random factors.

## 7. Charts in the Gage R&R output

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/crossed-gage-r-r-study/interpret-the-results/key-results/ — read 2026-10-12.

- Xbar chart by operator: most points should fall beyond the control limits, because the parts reflect part-to-part variation.
- R chart by operator: points should stay within the control limits when operators measure consistently.
- Non-parallel or crossing lines in the Operator×Part plot indicate interaction.

https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc321.htm — read 2026-10-12.

- Range chart upper limit = D4 × R̄; D4 = 3.267 (n=2), 2.575 (n=3), 2.282 (n=4), 2.115 (n=5); D3 = 0 for n ≤ 5.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/control-charts/how-to/time-weighted-charts/ewma-chart/methods-and-formulas/unbiasing-constants-d2-d3-and-d4/ — read 2026-10-12.

- d2 = 1.128 (N=2), 1.693 (3), 2.059 (4), 2.326 (5), 2.534 (6), 3.078 (10), 3.472 (15).

## 8. Destructive tests, nested and expanded designs

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/supporting-topics/gage-r-r-and-wheeler-s-emp-studies/gage-studies-with-destructive-testing/ — read 2026-10-12.

- You must be able to assume all parts within one batch are identical enough to count as the same part; otherwise within-batch part variation masks measurement variation.
- All operators measure parts from each batch → crossed or expanded. Each batch measured by one operator → nested or expanded. Extra factors, fixed factors, mixed crossed and nested factors, or unbalanced data → expanded.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/nested-gage-r-r-study/before-you-start/overview/ — read 2026-10-12.

- Nested is for when every operator cannot measure all parts; no operators measure the same part.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/nested-gage-r-r-study/interpret-the-results/key-results/ — read 2026-10-12.

- Nested ANOVA terms: Operator; Part(Operator), parts nested within each operator; Error or repeatability.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/expanded-gage-r-r-study/before-you-start/overview/ — read 2026-10-12.

- Expanded for unbalanced designs, more than two factors (for example operator, gage and part), fixed factors, or both crossed and nested factors.

## 9. Type 1 gage study and resolution

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/type-1-gage-study/methods-and-formulas/methods-and-formulas/ — read 2026-10-12.

- Cg and Cgk use K = percent of tolerance (default 20) and the study variation (default multiplier 6; 5.15 covers 99%). Cgk also uses the mean and the reference value. Bias = mean − reference; t-test with n − 1 degrees of freedom.
- Resolution guideline: not greater than 5% of the tolerance.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/type-1-gage-study/before-you-start/data-considerations/ — read 2026-10-12.

- 50 measurements for an adequate study (minimum 10 for the statistics); one reference part with a known value; one operator.

https://support.minitab.com/en-us/minitab/help-and-how-to/quality-and-process-improvement/measurement-system-analysis/how-to/gage-study/type-1-gage-study/interpret-the-results/key-results/ — read 2026-10-12.

- 1.33 is described as a "commonly used benchmark" for Cg and Cgk, without a cited standard.

https://www.itl.nist.gov/div898/handbook/mpc/section4/mpc451.htm — read 2026-10-12.

- The number of digits displayed does not indicate the resolution of the instrument; resolution should be checked under actual measurement conditions.

https://www.itl.nist.gov/div898/handbook/mpc/section4/mpc42.htm — read 2026-10-12.

- More than two artifacts and a random sample of more than two operators from the pool; if only one operator uses the gauge, measurements on more than two days.

## This plugin's rules of thumb (no external source)

- The F-test for the interaction uses F = MS_Operator×Part / MS_Repeatability with (a−1)(b−1) and a·b·(n−1) degrees of freedom; the reduced model pools those two sums of squares. This is the standard two-way random-effects ANOVA arithmetic behind section 3.
- Spreadsheets based on the AIAG average-and-range form use K1, K2, K3 constants from the manual. K1 for 2 and 3 trials is approximately 1/d2 (0.8862, 0.5908); the manual's K2 and K3 come from a different table than plain d2. Do not mix tables; use the constants the user's template shows.
- 6 × σ versus 5.15 × σ changes %Study Var by nothing (both columns scale) but changes %Tolerance by a factor of 6/5.15 ≈ 1.165.
