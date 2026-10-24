# SDS Reviews

Review supplier safety data sheets (SDS) for missing or contradictory information under US OSHA HazCom (29 CFR 1910.1200). For EHS coordinators and product stewards at chemical formulators, distributors and industrial sites. Paste SDS text, a PDF text extract, an inventory list or an SDS index export. No account, connector, API key or extra software is needed.

| Skill | Input | Result |
|---|---|---|
| sds-gap-review | One SDS, plus market, substance or mixture, and label text if available | Section-by-section gaps and contradictions with quoted passages, and numbered supplier questions |
| sds-inventory-match | Inventory list and SDS index or SDS texts | Product-by-product match table (matched, identity mismatch, missing, superseded, old format) and a request list by supplier |
| sds-revision-compare | Old and new SDS for the same product | Change table by section, site follow-ups and supplier questions |

Try: "Check this SDS for missing sections", "Which of our chemicals have no SDS?", "What changed between these two SDS versions?"

## What the reviews cover

- Appendix D minimum content for sections 1-11 and 16, the 16 headings in order, and the difference between a blank field and a stated "no applicable information".
- The 2024 HazCom amendments and the compliance dates as extended on 2026-01-15: 2026-05-19 for substances and 2027-11-19 for mixtures (suppliers); older-format SDSs are not reported as violations before those dates.
- Checks the SDS can answer from its own data: flash point against flammable liquid category, pH against corrosion classes, stated ATE against acute toxicity category, signal word and pictogram precedence, prescribed trade-secret concentration ranges, PEL coverage for every listed ingredient, and product identity against label and inventory.
- Rules often applied wrongly: an SDS has no OSHA expiry date; EU-format extras are not US requirements; superseded SDSs are kept as exposure records rather than deleted.

The reviews quote the passages they rely on and stop where pages are missing or OCR is unreadable. They do not classify a product, write a replacement SDS or certify compliance. Results support, but do not replace, sign-off by your qualified EHS reviewer, and corrections come from the supplier. Reviews follow federal OSHA; State Plan states may add requirements.

## Data and network

The skills read only the text and files you supply in the conversation. They make no web requests, run no programs, store nothing and send nothing. Supplier questions are drafted for you to send. Your assistant provider processes the conversation under its own settings. See [PRIVACY.md](PRIVACY.md).

## Sources

Official OSHA and Federal Register sources, with the clauses used and the date each was read (2026-10-12): [references/osha-hazcom-sources.md](references/osha-hazcom-sources.md).

MIT - [LICENSE](LICENSE). Support: https://github.com/grayskripko/marketing-skills/issues
