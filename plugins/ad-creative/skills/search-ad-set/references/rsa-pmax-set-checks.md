# Search text sets: roles, combination test, pinning

Limits come from `platform-specs.md` (rows G-RSA-*, G-PMX-*). The role mix below is optional inspiration, not a platform rule or an asset quota. Prefer distinct product-specific copy; do not replace missing proof or benefits with generic keyword filler.

## Responsive search ad: default role mix (15 headlines)

| Role | Count | Purpose |
|---|---|---|
| Keyword | 4 | repeat the searcher's words so the ad reads as relevant |
| Benefit | 3 | what changes for the buyer, only from F-ids; a slot the facts cannot fill becomes a keyword line |
| Proof | 2 | only from F-ids; with no proof fact, write keyword lines instead and say which fact would add proof |
| Offer | 2 | trial, price, guarantee, only from F-ids |
| Call to action | 2 | a verb and the next step |
| Brand | 1 | the name as the user writes it |
| Short | 1 | 15 characters or fewer, useful for narrow slots and reused as the Performance Max short headline |

Descriptions (4): benefit plus proof; feature plus outcome; offer plus call to action; the main objection answered.
Paths (2): words from the keyword theme, each 15 or fewer, no spaces (use hyphens).

## Checks before the set is printed

1. **Length:** every field under its hard limit with the count beside it, double-width counted 2.
2. **Fact lock:** every number, price, rating and promise maps to an F-id. Lines without one are rewritten or marked.
3. **Duplicates:** compare every headline pair and every description pair for exact duplicates and repeated core promises. Repeated names, keywords and qualifiers are not automatic failures, but do not excuse gimmicky repetition. Check representative headline/description combinations for redundancy and contradictions. Report findings and scope only when requested or when a remaining problem needs action; never claim all combinations passed from a small sample.
4. **Combination test:** headlines are shown in any order and any three may appear together. Take 8 sampled triples ("H_a | H_b | H_c"; print them only if one fails or the user asks) and read each aloud: no triple may repeat a claim, contradict itself (two different prices), read as nonsense, or contain a headline that only makes sense right after another one. Replace any headline that breaks a triple and re-run. Sampling: if a code tool exists, pick 8 random ordered triples with a fixed seed and print the seed; otherwise pick triples that pair each offer and proof line with each other once.
5. **Pinning:** default is none. Pin only text that must show every time (a legal qualifier, a regulated disclosure) and say that pinning narrows the combinations the system can test.
6. **Must-survive list:** words that filter out the wrong buyers (price floors, "for teams of 10+", "UK only"). Remind the user that Google's text customization (formerly automatically created assets) and Final URL expansion can generate new text from the landing page, so they should check the served combinations and the asset report for these words.
7. **Policy pass:** run the ad-preflight rule screen over the finished set and append its findings.
8. **Myth line where useful:** a low Ad Strength rating does not by itself stop an ad from serving and is not part of Ad Rank (answer/9921843). Do not pad the set with near-duplicates to raise it.
9. **Over-length lines** are rewritten, never trimmed mid-word; say which draft was replaced and its count.

## Performance Max text set (on request)

- 3–15 headlines of 30 or fewer, **at least one of 15 or fewer (required by the page)**; the page suggests 11 or more.
- 1–5 long headlines of 90 or fewer; the page suggests 2 or more, of 30 or more characters.
- 2–5 descriptions of 90 or fewer; the page suggests 4 or more.
- Business name of 25 or fewer, matching the domain or verified name, no promotional words (GOO-ED-BN, including the October 2026 verified-relationship rule).
- Up to 2 display URL paths of 15 or fewer.

## Paste-ready table (CSV)

Only when requested: use the user’s destination schema, or a clearly labelled one-ad worksheet row with numbered headline and description columns plus requested paths or business name. This is not an account import until required destination fields are supplied. `field,position,text,characters,role,fact_ids` is an optional audit export; position is blank unless pinned. This plugin changes no account.
