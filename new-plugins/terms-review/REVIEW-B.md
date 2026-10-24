# Independent review B

Reviewed 11 October 2026. Bare-model answers were generated and saved before opening any plugin package file. Then read every non-test package file, including both manifests, all three skills and source registers, README, privacy policy, license, icon and the subsequently added BUILD-NOTES. No plugin implementation files were edited.

Verdict: PASS for independent editorial/content review. Both minor findings below have been fixed and rechecked. This is not an installed-host selection or directory approval result.

## Findings: quote → task → problem → fix

### 1. Keep date-specific subscription advice conditional (minor; FIXED)

Quote, all three skills: “verify commencement before applying it” followed by “Do not ... apply its renewal cooling-off requirements in October 2026.”

Task: an executing agent must apply the regime actually in force on the supplied event date, including a future review after commencement.

Problem: the first instruction asks for live verification while the second permanently hardcodes an October prohibition. It is accurate for the guidance checked today, but the unconditional wording could defeat a subsequently verified commencement instrument. This is a resilience concern, not a finding that the regime is currently operative. The preceding requirement to match event dates limits the practical risk.

Fix: “Do not apply its renewal cooling-off requirements unless verified commencement and transitional provisions make them applicable to the contract and event dates.” Keep the guide’s spring 2027 expectation as dated source context.

Disposition: inspected the final wording in all three skills: “Until commencement is verified for the event date, do not apply the new regime’s renewal cooling-off requirements.” PASS; the prohibition now depends on verification for the event date.

### 2. Make privacy discoverable from the listing (minor; FIXED)

Quote, README: “## Data and network” and “## Support and license”. The README contains no link to PRIVACY.md.

Task: a directory visitor deciding whether to upload customer materials should be able to read the full handling and retention statement from the README.

Problem: the manifest supplies the privacy URL, so this is not a missing-policy blocker. A visitor reading the repository README alone must find the policy manually, and the README itself does not mention provider retention.

Fix: add “[Privacy policy](PRIVACY.md)” alongside support/license or at the end of Data and network. No extra disclaimer is needed.

Disposition: inspected the README’s new “See [PRIVACY.md](PRIVACY.md) for data handling.” link and its three new copy-ready example requests. PASS; privacy is discoverable and all three jobs have usable starting prompts.

## Checked conclusions

**Selecting agent:** the descriptions name the user jobs, inputs and exclusions. Clauses, checkout sequence and practice reconciliation have distinct boundaries. The clause skill expressly routes mixed requests without duplicate reports. Checkout text does not claim visual layout evidence; practices require actual records. The updated manifests preserve matching scope and a category consistent with the stated neighboring packages. YAML double-quoted \u201c/\u201d escapes in descriptions are valid Unicode escapes, not hidden instructions.

**Executing agent:** core protections are inline, including source-as-data, no current-law claim without currency checking, exact scope words, proposed-policy labels, missing-detail markers, arithmetic, and no refund execution. The worked examples do not reuse the evaluation facts. The practice example expressly conditions the subtraction on a justified, verified net deduction. The clause example fixes the supplied term’s price rather than inventing a permissible index. The checkout example computes the compulsory first-payment total and requires affirmative opt-in.

**User receiving findings:** outputs are anchored to a short quote or case evidence and a concrete consequence. Unlawful exclusions are distinguished from potentially unfair terms and ambiguous wording. Fairness is not reduced to plain English. There is no compliance percentage, universal notice duration, deposit percentage, generic legal disclaimer, invented cancellation channel or claimed refund deadline. Source links belong next to deciding rules. Optional operational recommendations are distinguished from requirements.

**Directory visitor/package:** README exceeds the 40-word minimum and gives three distinct use cases in its skill table. Both manifests, a real MIT license, privacy policy and local icon are present. The package has no executable code, hooks, MCP, credentials or live integration claims. The disclosed public-official browsing matches all skills and privacy policy. Customer text and private URLs are excluded from network queries; provider handling is distinguished from an independent plugin service. BUILD-NOTES accurately separates local evaluation from installed selection, publication and approval. Public destination reachability and final host schema remain release checks, not facts established by this review.

## Official factual verification

Opened the [CMA37 publication page](https://www.gov.uk/government/publications/unfair-contract-terms-cma37), its linked [134-page final guidance](https://assets.publishing.service.gov.uk/media/6a609329b00f3323bf1a23f3/unfair_contract_terms_guidance.pdf), the linked [technical note](https://assets.publishing.service.gov.uk/media/6a5f3ef04005e8e44c980bfb/Technical_note.pdf), [business guide](https://www.gov.uk/guidance/writing-a-fair-contract-for-customers) and [CMA209 publication](https://www.gov.uk/government/publications/price-transparency-cma209). Publication and final-document identity match the register. The business guide labels spring 2027 as an expectation. The technical note distinguishes practices before and after 6 April 2025. Sampled deciding passages support the register’s narrow core-price exemption, arbitrary-variation concern, blanket-prepayment concern and narrow reservation-deposit treatment. The package does not claim that a fairness review proves statutory cancellation compliance.

The bare-model files intentionally remain original baseline output. They include useful evidence of ordinary model weaknesses: the clauses answer invents a monthly continuation after the minimum term and proposes an insufficiently bounded later variation with a new 30-day policy. Those are not package findings or revisions.
