# Platform ad rules (numbered, dated)

Each row: our id, the rule in our own words, an example we wrote ourselves (never the platform's own sample text), the page, and the date read. Severity used in findings:
- **likely disapproval** — the text matches a stated "not allowed" item;
- **restricted** — the category is allowed with conditions set on the page;
- **needs proof** — allowed only if the user holds evidence; goes to the claim ledger as Hold until shown;
- **info** — something to check outside the text (a setting, a label, a page).

Rows older than 6 months at run time get "re-check this row at its link".

## Google Ads

| Id | Rule (our wording) | Our example | Severity | Source | Read |
|---|---|---|---|---|---|
| GOO-ED-CAP | Capitals must be used normally. Whole words in capitals or alternating case for emphasis are out; common abbreviations, coupon codes and brand or product names with their own casing may be allowed after a review. | "SAVE BIG on Tiles" → "Save on Tiles" | likely disapproval | support.google.com/adspolicy/answer/14848295 | 2026-10-08 |
| GOO-ED-RP | The same punctuation mark or symbol twice in a row is out, and so is gimmicky use of dots, numbers or symbols. A single "!" is not addressed by the page and is **not** flagged. | "Tiles!!" → "Tiles!" or "Tiles" | likely disapproval | support.google.com/adspolicy/answer/14847994 | 2026-10-03 |
| GOO-ED-SYM | Emoji, other unsupported characters, and non-standard symbols such as bullets or stars used as decoration are out. | "★ Tiles ★" → "Tiles" | likely disapproval | same page | 2026-10-03 |
| GOO-ED-PH | A phone number typed into ad text is out; use the call asset instead. | "Call 020 7946 0000" → move the number to a call asset | likely disapproval | support.google.com/adspolicy/answer/6021546 | 2026-10-03 |
| GOO-ED-REP | Gimmicky or unneeded repetition of a name, word or phrase is out, inside one asset or across assets in the same ad group, campaign or account. The page gives no keyword exception. This plugin's own convention lets one keyword appear in several assets and keeps any phrase of three or more words to one asset. | A headline "Oak Tiles Oak Tiles" | likely disapproval | support.google.com/adspolicy/answer/6021546 | 2026-10-08 |
| GOO-ED-SPC | Missing spaces, extra spaces or gimmicky spacing are out. | "T i l e s" | likely disapproval | same page | 2026-10-03 |
| GOO-ED-SPL | Text must use accepted spelling and grammar and make sense. | "Tilez 4 u" | likely disapproval | same page | 2026-10-03 |
| GOO-ED-BN | The business name field holds the domain, the advertiser's recognised name or the app name, with no promotional words. From October 2026 a name may differ from the domain only where a verified direct relationship exists; resellers and affiliates may not use a brand they resell. | "Cheapest Tiles Ltd" when the firm is "Harbour Tiles" | likely disapproval | same page; update support.google.com/adspolicy/answer/18287059 (posted 2026-10-01) | 2026-10-03 |
| GOO-ED-ID | The ad or page must name what is being promoted. | an ad that never says what is sold | likely disapproval | same page | 2026-10-03 |
| GOO-MR-UC | Inaccurate claims, or claims that lure with an improbable result. | "Fluent Spanish in 3 days" | needs proof / likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-03 |
| GOO-UNREL | Unreliable claims: an improbable result must not be presented as the likely outcome; a results testimonial needs a visible note that results vary; a guaranteed result needs an easy-to-find refund policy. Unrealistic weight-loss timeframes and "risk-free" returns are named examples. | "Lose 8 kg in 2 weeks" | needs proof / likely disapproval | support.google.com/adspolicy/answer/15936857 | 2026-10-03 |
| GOO-MR-UO | Promising products, services or offers that are not actually available. | "40% off" when the page shows no discount | likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-08 |
| GOO-MR-DP | Hiding how payment works or giving a false picture of the cost. | "$0 setup" when a fee is due at checkout | likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-08 |
| GOO-MR-CB | Clickbait or sensational text or images used to pull clicks, including using death, illness, accidents, arrests or bankruptcy to push fear-driven action. | "You won't believe what tiles did" | likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-08 |
| GOO-MR-AD | Elements that look like working buttons, or design that hides that it is an ad. | an image of a "Play" button that does nothing | likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-08 |
| GOO-MR-UR | The promotion does not match the landing page. | ad offers "free samples", page sells only full boxes | likely disapproval | support.google.com/adspolicy/answer/6020955 | 2026-10-08 |
| GOO-AI | Labelling image or video as AI-made or AI-edited is optional (a text or visual label, or the label setting); using it does not by itself meet local laws (the page names EU, India and New York rules). Election ads carry a mandatory "altered or synthetic content" disclosure; this plugin declines election ads anyway. | — | info | support.google.com/adspolicy/answer/17257106 (posted 2026-07-09) | 2026-10-03 |

## Meta

| Id | Rule (our wording) | Our example | Severity | Source | Read |
|---|---|---|---|---|---|
| META-PA | The ad must not state or hint that the advertiser knows a personal attribute of the viewer: race or ethnicity, religion, age, sexual orientation or practices, gender identity, physical or mental health, disability, vulnerable financial status, voting status, union membership, criminal record, name. Questions or "you" lines that presume the attribute are the usual trigger. | "Struggling with your arthritis?" → "Joint-friendly workouts for every morning" | likely disapproval | transparency.meta.com/policies/ad-standards/objectionable-content/privacy-violations-personal-attributes/ (change log lists an update dated 2024-06-26; the newest entry showed no date when read) | 2026-10-08 |
| META-HW | Health and wellness: weight-loss, cosmetic-procedure and supplement ads must be aimed at people 18 and over; no clickbait promises of a specific result in a set time without a disclaimer; no statements that put down someone's body or appearance; no fat-pinching close-ups. | "Drop two sizes in 10 days" | restricted / needs proof | transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/ (updated 2026-07-22) | 2026-10-08 |
| META-SAC | Special ad categories: housing, employment, financial products and services (this replaced "credit" from 2025-01-14 for US campaigns), and issues, elections or politics. The first three fix age at 18–65+, allow no gender targeting, need a radius of at least 15 miles or 25 km (15 km in Europe), allow no postal codes, and allow no lookalike audiences. The skill only names the category; it gives no audience advice. | a debt-consolidation loan ad | restricted | developers.facebook.com/docs/marketing-api/audiences/special-ad-category/ | 2026-10-08 |

## LinkedIn (policy revised 2025-11-18)

| Id | Rule (our wording) | Our example | Severity | Source | Read |
|---|---|---|---|---|---|
| LI-CL | Every claim needs factual support. | "Cuts audit time by half" with no study | needs proof | linkedin.com/legal/ads-policy | 2026-10-03 |
| LI-CMP | No deceptive or inaccurate claims about a competitor's product. | "Unlike X, we never lose data" | needs proof / likely disapproval | same page | 2026-10-03 |
| LI-END | Do not imply an affiliation or endorsement that was not given. | a partner's logo used without permission | likely disapproval | same page | 2026-10-03 |
| LI-FMT | No wrong spelling, grammar or punctuation, excessive emoji or capitals, or unrelated hashtags. | "BOOK NOW 🔥🔥🔥 #monday" | likely disapproval | same page | 2026-10-03 |
| LI-POL | Political ads are prohibited. | — | declined | same page | 2026-10-03 |

## TikTok (policy pages updated April 2026)

| Id | Rule (our wording) | Our example | Severity | Source | Read |
|---|---|---|---|---|---|
| TT-MIS-EX | No promised or overstated product effects, and no cures for incurable conditions. | "Clear skin overnight" | likely disapproval | ads.tiktok.com/help/article/tiktok-ads-policy-misleading-and-false-content | 2026-10-03 |
| TT-MIS-RANK | No absolute terms about a product in relation to time, region or brand; the page's examples are "Number 1" claims, and it gives no exception for claims that can be checked. | "The No. 1 planner app" | likely disapproval | same page | 2026-10-08 |
| TT-MIS-BA | No before-and-after comparisons that could give a false idea of results. | split-screen "week 1 / week 4" | likely disapproval | same page | 2026-10-03 |
| TT-MIS-UI | No fake play buttons, close buttons or similar decoys. | a drawn "X" in the corner | likely disapproval | same page | 2026-10-03 |
| TT-MIS-LP | Discounts, products and promotions in the ad must match the landing page. | "30% off" ad, page at full price | likely disapproval | same page | 2026-10-03 |
| TT-AIGC | Content made or significantly changed with AI must be labelled (the AIGC label, a caption, sticker, watermark or disclaimer); minor edits such as lighting, colour or background removal need no label. Undisclosed AI content is rejected or restricted. | — | info / likely disapproval if missing | same page | 2026-10-08 |
| TT-FMT | Caption and on-screen text without spelling or grammar errors and without excessive capitals, spacing, numbers, symbols or punctuation; language and currency fit the target market; caption, text, visuals and CTA consistent with the landing page; no QR codes in ad content (a QR code on product packaging or in an app, and unscannable codes such as barcodes, are allowed); ad and landing page show the same brand. | "BEST DEAL $$$ !!!" | likely disapproval | ads.tiktok.com/help/article/tiktok-ads-policy-ad-format-and-functionality | 2026-10-08 |
| TT-CAP | Non-Spark in-feed captions take no clickable links, @ mentions or hashtags. | "Shop now @harbourtiles #tiles" | likely disapproval | ads.tiktok.com/help/article/tiktok-auction-in-feed-ads (updated June 2026) | 2026-10-03 |

## Cross-platform claim groups (this plugin's own grouping of the rows above and in `legal-rules.md`)

| Id | What triggers it | Rows it combines (each dated in its own table) | Built |
|---|---|---|---|
| GEN-CL-RANK | "best", "#1", "leading", "top-rated", "fastest" | US-FTC-SUB, UK-CAP-3.7, UK-CAP-3.33 / 3.34 (superlative read as a comparison), GOO-MR-UC, TT-MIS-RANK, LI-CL | 2026-10-03 |
| GEN-CL-ENDORSE | "doctors recommend", "as used by", expert or celebrity backing | US-FTC-SUB (stated level of support), US-FTC-END, UK-CAP-3.47 | 2026-10-03 |
| GEN-CL-OUTCOME | a result, a time to result, "saves X hours" | US-FTC-SUB, US-FTC-END (typical results), UK-CAP-3.11, GOO-MR-UC, GOO-UNREL, META-HW, TT-MIS-EX | 2026-10-03 |
| GEN-URG | "today only", "last chance", "only 3 left" | UK-CAP-3.30, EU-UCPD-7 (unverified wording), GOO-MR-UO | 2026-10-03 |
| GEN-PRICE | discounts, "from" prices, "save", was/now prices | UK-CAP-3.17 to 3.22, UK-CAP-3.39, GOO-MR-DP, GOO-MR-UO, TT-MIS-LP | 2026-10-03 |
| GEN-FREE | "free", "free trial" | UK-CAP-3.23 to 3.26, GOO-MR-DP | 2026-10-03 |
| GEN-RV | review scores, testimonials, "customers say" | US-FTC-RV, UK-CAP-3.44 to 3.50, EU-UCPD-23b (unverified wording) | 2026-10-03 |
| GEN-GREEN | "eco-friendly", "green", "sustainable", "carbon neutral", eco labels (EU audience) | EU-UCPD-4a, EU-UCPD-4c, EU-UCPD-2a | 2026-10-03 |

## Not covered

Gambling, alcohol, crypto and dating rules beyond naming the category ("check the platform's page for this category"), trademarks in ad text, and any platform not listed above. Political, electoral and social-issue ads are declined.
