# Common claims and what the evidence says

Answer briefly from this file when the user raises one of these.

| Claim | Short answer |
|---|---|
| "p < 0.05 means a 95% chance that B is better." | No. The p-value is how surprising the data would be if there were no difference. The chance B is really better depends also on how often your ideas win (the A/B test verdict skill prints this false-positive risk). |
| "Stop the test as soon as it turns significant." | Only under a sequential method chosen before launch. Stopping at the first significant look inflates false positives; in Evan Miller's worst-case simulation, to 26.1% instead of 5%. |
| "+13% with p = 0.11 is directionally a win." | The interval runs from a loss to a large gain. That is Inconclusive; it rules out only effects outside the interval (a loss worse than the lower end or a gain above the upper end). |
| "100 conversions per arm is always enough." | The visitors needed depend on the baseline rate and the smallest lift worth having; compute them (the A/B test plan skill prints the formula). |
| "The industry average is our target." | Averages describe other sites with other traffic. Compare with your own earlier period, your strongest segment or a target you set. |
| "More variants find a winner faster." | Each extra arm splits the traffic and adds a comparison; with the correction, every arm needs more visitors. |
| "Three days is enough if we hit the sample size." | Run whole weeks so each weekday counts equally in both arms; weekday and weekend visitors often convert differently. |
| "Fewer fields always convert better." | A field that is needed to deliver or to qualify may be worth its cost. The ledger asks why each field exists; there is no fixed cost per field. |
| "A good programme wins most of its tests." | Published success rates for well-run programmes range from about 8% to about 33% of tests (Kohavi, Deng & Vermeer, KDD 2022, Table 2). |
| "Another site's winning test will work here." | Their audience, traffic and baseline differ. Treat it as an idea to test or research, not a result. |
| "Every change should be A/B tested." | Bugs, missing information and rule fixes ship without a test; tests are for uncertain changes that can finish at your traffic. |
| "The tool says 92% chance to beat control, so we are 92% right." | That figure depends on the tool's prior and model; it is not the probability that shipping is the right call. Read the interval and the gates. |
| "This segment won, so roll it out to that segment." | A segment picked after the test is a hypothesis for the next test, not a finding. |
| "Our lab speed score is 45, so users wait." | Lab scores come from one simulated load. Real-user field data at the 75th percentile shows what visitors experience. |
| "Five users told us; the conversion problem is proven." | Five-person rounds find usability problems; they do not measure rates. |
| "The step with the most people lost is where the money is." | Without a reference rate, loss counts always point at the top of the funnel. The funnel skill ranks only against a reference you name. |
| "A Bayesian calculator makes peeking safe." | Stopping whenever the posterior looks good also inflates errors unless the stopping rule is part of the method. Choose and write the rule before launch. |
| "The checkout average is 11.3 fields, so we should match it." | Reference rows describe other sites; they are context, not targets. Ask why each of your fields exists. |
