# How each platform counts characters

Read 2026-10-03 on the pages listed in `platform-specs.md`. Where a page says nothing, the method below is this plugin's convention and the output must say "count method not stated by the platform".

| Platform | What the page states | Convention used here when the page is silent |
|---|---|---|
| Google Ads | Each Chinese, Japanese or Korean (double-width) character counts as 2. Emoji are not accepted in ad text at all (they fall under unsupported characters), so their count never matters. | Every other character, space and punctuation mark counts 1. |
| Meta | No counting method on the ads guide pages read. | Count each visible character as 1, an emoji as 1, a line break as 1. Say that Meta's own preview is the final word. |
| LinkedIn | The recommended introductory length counts spaces, emoji and punctuation. | Line breaks count 1. |
| TikTok | Display name: 10 double-width characters or 20 others. Caption: no counting method and no maximum stated. | Display name counted like Google (double-width = 2, limit 20). Caption length is reported but not judged. |

## Procedure

1. Count each field exactly as it will be uploaded, spaces and punctuation included, after the user's own placeholders are filled in. If the user's text still holds a placeholder such as `{city}`, count the longest value the user gives, or report "count depends on the inserted value".
2. Use the host's code tool when present. A reliable test for double-width: characters whose East Asian Width property is W or F.
3. Counting by hand (no code tool): count each word's letters, add the spaces and punctuation separately, and print the sum (`14+1+…`) for any field within 3 of a limit or over it. Re-count over-limit fields once before reporting, and label the table "counted by hand".
4. Compare against the hard limit first (over = must cut), then the recommendation (over = will be cut in the feed; show the preview).
5. Truncation preview: the first N characters at the recommended length, with no ellipsis added, so the user sees exactly where the cut falls.
6. Print the counting rule used in the field table's "Rule" column (for example "double-width = 2" or "count method not stated").

## Worked counts (computed by script)

| Text | Plain characters | Google count | Limit | Result |
|---|---|---|---|---|
| カームリー公式アプリ | 10 | 20 | 30 (headline) | fits |
| 請求書を2分で送信 | 9 | 17 (one digit counts 1) | 30 | fits |
| Call 0800 123 456 Now | 21 | 21 | 30 | fits on length, fails the phone-number rule |

## Edge cases

- Emoji built from several code points (skin tones, flags, joined sequences): count the visible emoji as 1 and add "emoji: the ad tool's count may differ".
- Line breaks: no page read states how they count. Count each as 1 and say so.
