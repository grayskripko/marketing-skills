# Statistics for creative results

z = 1.96 for 95%. All formulas below are standard; cite them by name.

## Data gate (run first)

- clicks ≤ impressions; conversions ≤ clicks when conversions are click-based (say so if they are view-based); 3-second views and ThruPlays ≤ impressions.
- Same date range and same attribution setting for every row, or list the difference.
- A row with zero impressions is dropped and listed.
- Missing columns are listed under "Not checked" with what they would have allowed.

## Primary metric (declared before reading)

The user's choice. If none is given, use conversions per impression, because it rewards an ad for both pulling the click and bringing the buyer. CTR, hook rate and hold rate are guardrails: shown, never used alone to name a winner.

## Wilson 95% interval for a rate k/n

p = k/n; centre = (p + z²/2n) / (1 + z²/n); half-width = z·√(p(1−p)/n + z²/4n²) / (1 + z²/n). (Wilson, JASA 22:209–212, 1927.)

## Difference of two rates (Newcombe method 10)

d = p_B − p_A. With Wilson limits (l_A, u_A) and (l_B, u_B):
lower = d − √((p_B − l_B)² + (u_A − p_A)²); upper = d + √((u_B − p_B)² + (p_A − l_A)²). (Newcombe, Statistics in Medicine 17:873–890, 1998.)

"Resolved" only when the interval excludes 0; otherwise "not resolved yet".

## More than two variants

Compare each variant with one named reference. Order the p-values from a two-proportion z-test and apply Holm: the i-th smallest of m is tested at 0.05/(m − i + 1), stopping at the first that fails (Holm, Scandinavian Journal of Statistics 6:65–70, 1979). If the user does not want p-values, label all comparisons "exploratory" instead.

## Design label

- **Observational:** ads share one ad set or ad group and the platform's delivery chose who saw which. Delivery shifts spend toward whatever it predicts will work, so audiences differ between ads; a difference is a lead, not proof of cause.
- **Randomised:** only when the user says the platform's experiment or A/B test tool split the audience.

## Sample size per arm (two proportions, two-sided α 0.05, power 80%)

n = (1.96·√(2·p̄(1−p̄)) + 0.8416·√(p₁(1−p₁) + p₂(1−p₂)))² / (p₁ − p₂)², with p̄ = (p₁+p₂)/2. Print it in impressions and in days at the user's daily impressions per arm (more days needed = (n − impressions so far) / daily impressions, rounded up). "Not feasible at this delivery" is a valid answer; then offer a bigger difference to detect or an earlier-funnel primary metric chosen in advance.

## Peeking

Stopping a test when a difference first looks resolved inflates false winners. Fix the sample or the end date before the test starts; if the user checks daily, say so in the readout.

## Video diagnostics

- Hook rate = 3-second views ÷ impressions.
- Hold rate = ThruPlays ÷ impressions.
Both get Wilson intervals and the label "diagnostic, not a sale". No good/bad bands are given.

## Verdict per concept

- **keep testing** — primary difference not resolved and the sample is still short of the planned size;
- **iterate one variable** — resolved on a guardrail only on a randomised design, or the concept is mixed across formats. On an observational design a guardrail-only gap gives keep testing, and any reason for the gap is a guess to test;
- **retire** — the upper bound of its primary difference vs the reference is below 0;
- **likely winner** — the lower bound is above 0 on a randomised design (on an observational design say "lead: confirm with a split test"). This names the better ad only; it is not advice on spend.
- Roll single ads up to concept and format before judging ads with few conversions.

## Worked numbers (computed by script)

Rows: A 12,000 impressions, 240 clicks, 18 conversions; B 9,000, 207, 12; one ad set, 10 days.
- CTR A 2.00% (1.76–2.27), B 2.30% (2.01–2.63); B − A +0.30 pp (−0.09 to +0.71): not resolved.
- Conversions per impression A 0.150%, B 0.133%; B − A −0.017 pp (−0.121 to +0.097): not resolved.
- To detect CTR 2.0% → 2.4%: 21,109 impressions per arm. At 1,200 a day A needs 8 more days; at 900 a day B needs 14 more; the test needs about 14 more days.
