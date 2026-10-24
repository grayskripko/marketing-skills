# X draft formats and validation

Sources checked 2026-10-11. These are bundled facts as of that check, not a live account or composer check. Source pages do not state publication dates unless noted. Runtime network scope remains none.

## Standard posts and thread parts

[X counting documentation](https://docs.x.com/fundamentals/counting-characters), checked 2026-10-11: standard text has a **280 weighted-character** ceiling. Normalize to NFC before counting. Recognized URLs occupy **23** weighted characters each; count surrounding spaces separately. Emoji sequences, including skin-tone and joined families, count as **2** each; CJK characters count as **2**. Hashtags and manually typed mentions count normally. Auto-populated reply recipients are excluded; do not exclude handles typed into a plain draft. Official-client attached media occupies no text characters; a pasted media URL still needs URL detection.

The [official twitter-text configuration](https://github.com/twitter/twitter-text/blob/master/config/v3.json), checked 2026-10-11, uses weight **1** for code points U+0000–U+10FF, U+2000–U+200D, U+2010–U+201F and U+2032–U+2037; default weight is **2**, with emoji parsing enabled. These ranges are counting configuration, not permission to insert control characters. Raw bytes, JavaScript string length and visible glyph count are not substitutes for the official parser. Configuration alone does not implement URL or emoji recognition.

Worked arithmetic, derived 2026-10-11 from the counting rules above:

- `Hi 👨‍👩‍👧‍👦` = `2 letters + 1 space + 2 emoji weight = 5`.
- `Read https://example.com/long/path` = `4 letters + 1 space + 23 URL weight = 28`.
- `你好` = `2 CJK characters × 2 = 4`.
- `café` and `cafe` followed by a combining acute accent both normalize to `café`: **4**.

Do not open example URLs; they are counting inputs. Count each thread part independently, including any numbering actually pasted into the composer. Preserve qualifiers when shortening. A split should not detach a caveat from its claim. If no trusted compatible counter is already available, do not install software or claim exact automated validation. Leave comfortable room and label any uncertain count as an estimate when it affects readiness. A final composer check remains the user's publishing check; this package does not publish.

## Longer posts

[X post types](https://help.x.com/en/using-x/types-of-posts), checked 2026-10-11, describes longer posts up to **25,000 characters**, requiring X Premium to create. It also says mentions after the first **280 characters** do not notify the mentioned account, and mention-only reply controls require mentioning the account within that opening segment. Do not assume subscription or that this format is available in the user's composer. This help page does not specify a separate long-post counting algorithm; the standard twitter-text validity result does not certify long-post eligibility. Articles are a different format and are outside this bundled limit. Default to standard posts unless the user chooses a longer format; offer a thread when appropriate.

## Drafts intended for publication

[X Authenticity policy](https://help.x.com/en/rules-and-policies/authenticity), page dated April 2025; checked 2026-10-11: prohibits bulk unsolicited replies/mentions, repeated identical or near-identical posts, irrelevant promotional replies, unrelated hashtag spam and coordinated engagement inflation. Do not turn a reply request into a repeated outreach template or fabricate independent supporters. Ordinary factual drafting needs no policy lecture. Mention the applicable rule only when it changes the requested publication plan. No engagement or reach prediction follows from these rules.
