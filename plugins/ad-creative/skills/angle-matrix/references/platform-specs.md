# Platform text and asset specs (checked table)

Every row was read on the platform's own page on the date shown. "Hard" is the most the field accepts; "Rec." is the platform's recommendation, usually the point where text is cut in the feed. "—" means the page states no value: treat it as unknown, never guess it. If the run date is more than 6 months after a row's read date, print "re-check this row at its link".

## Google Ads

| Id | Format | Field | Count per ad | Hard | Rec. | Source | Read |
|---|---|---|---|---|---|---|---|
| G-RSA-H | Responsive search ad | Headline | 3–15 | 30 | — | support.google.com/google-ads/answer/7684791 | 2026-10-03 |
| G-RSA-D | Responsive search ad | Description | 2–4 | 90 | — | same page | 2026-10-03 |
| G-RSA-P | Responsive search ad | Display path | 2 fields | 15 each | — | same page | 2026-10-03 |
| G-PMX-H | Performance Max | Headline | 3–15 (page suggests 11 or more) | 30, and at least one must be 15 or fewer | — | support.google.com/google-ads/answer/14528373 | 2026-10-03 |
| G-PMX-LH | Performance Max | Long headline | 1–5 (page suggests 2 or more) | 90 | page suggests 30 or more | same page | 2026-10-03 |
| G-PMX-D | Performance Max | Description | 2–5 (page suggests 4 or more) | 90 | — | same page | 2026-10-03 |
| G-PMX-P | Performance Max | Display URL path | up to 2 | 15 each | — | same page | 2026-10-03 |
| G-PMX-BN | Performance Max | Business name | 1 | 25; must match the domain or the verified business name, no promotional words (GOO-ED-BN) | — | same page | 2026-10-03 |

Notes read on the same pages:
- Double-width characters (Chinese, Japanese, Korean) count as 2 toward Google limits (answer/7684791).
- Pinning a headline or description to a position is possible, and the page says it is not recommended for most advertisers and can lower Ad Strength. Text pinned to headline 1, headline 2 or description 1 always shows; headline 3 and description 2 are not guaranteed to show, and ad text may be shortened with an ellipsis (answer/7684791).
- Performance Max "text customization" (the page notes it was formerly called automatically created assets) and Final URL expansion can generate headlines and descriptions from the landing page, so qualifier words must be checked in the served ads (answer/14528373).
- Ad Strength is a feedback rating; it does not directly decide serving eligibility and is not used for Ad Rank (answer/9921843, read 2026-10-03).

## Meta (Facebook and Instagram)

The ads guide lists recommendations per placement and per objective. The two rows below are the ones read today; both pages scope them to the Awareness objective. Other objectives and placements are not in this table.

| Id | Placement (objective) | Field | Hard | Rec. | Asset | Source | Read |
|---|---|---|---|---|---|---|---|
| M-FBF-IMG | Facebook Feed, image (Awareness) | Primary text | — | 50–150 | 4:5, 1440×1800, JPG or PNG, up to 30 MB, min width 600 | facebook.com/business/ads-guide/update/image | 2026-10-03 |
| M-FBF-IMG-H | Facebook Feed, image (Awareness) | Headline | — | 27 | as above | same page | 2026-10-03 |
| M-IGR-IMG | Instagram Reels, image (Awareness) | Primary text | — | 44 | 9:16, 1440×2560, up to 30 MB, min width 500 | facebook.com/business/ads-guide/update/image/instagram-reels | 2026-10-03 |
| M-IGR-SZ | Instagram Reels, image | Safe zone | keep 14% top, 35% bottom, 6% each side clear of text and logos | — | — | same page | 2026-10-03 |

Not in the table (unknown, never sized to): Meta carousel card text, Stories text, video placement text, any hard maximum for primary text or headline.

## LinkedIn

| Id | Format | Field | Hard | Rec. | Source | Read |
|---|---|---|---|---|---|---|
| L-SI-INT | Single image ad | Introductory text | 3,000 | 150 (spaces, emoji and punctuation count) | linkedin.com/help/lms/answer/a426534 (page said "updated 2 months ago") | 2026-10-03 |
| L-SI-H | Single image ad | Headline | 200 | 70 | same page | 2026-10-03 |
| L-SI-D | Single image ad | Description | 300 | 100 | same page | 2026-10-03 |
| L-SI-IMG | Single image ad | Image | JPG, PNG or GIF (GIF up to 250 frames), up to 5 MB, up to 7680×4320; ratios 1.91:1, 1:1 and 4:5; images under 401 px wide show as thumbnails | — | same page | 2026-10-03 |

Not in the table: carousel, video, document, message and text ad fields.

## TikTok

| Id | Format | Field | Rule | Source | Read |
|---|---|---|---|---|---|
| T-IF-DN | In-feed ad | Display name | one line, 20 characters, or 10 in Chinese, Japanese or Korean | ads.tiktok.com/help/article/tiktok-auction-in-feed-ads (page updated June 2026) | 2026-10-03 |
| T-IF-CAP | In-feed ad, non-Spark | Caption | no clickable links, no @ mentions, no hashtags; **maximum length not stated → unknown** | same page | 2026-10-03 |
| T-IF-CAPS | In-feed ad, Spark | Caption | shows at most 4 lines, emoji included; character maximum not stated | same page | 2026-10-03 |
| T-IF-AR | In-feed ad, non-Spark | Video ratio | 9:16 recommended; 16:9 and 1:1 accepted | same page | 2026-10-03 |
| T-IF-VID | In-feed ad, non-Spark | Video file | up to 500 MB and 10 minutes; 540×960 or larger recommended for 9:16; safe-zone templates (standard, right-to-left, and with-anchor versions) are downloadable on the page | same page | 2026-10-03 |

Not in the table: caption character maximum, TikTok safe-zone pixels. For text placement on TikTok, tell the user to use TikTok's own safe-zone guide for their format.

## Conflicts and rows left out on purpose

- Some copied spec tables give LinkedIn introductory text a maximum of 600 and TikTok display names 40; the platform pages above say 3,000 and 20.
- A "TikTok ad text 1–100 characters" figure circulates on blogs; no platform page read on 2026-10-03 states it, so it is not used.
- LinkedIn's marketing-site spec page (business.linkedin.com, single image ad specs, read 2026-10-03) gives 70 as the recommended description length and says the description shows only on the LinkedIn Audience Network; the help page used above gives 100. Size descriptions to 70 when the ad runs on the Audience Network.

## Not in this plugin's checked table

Microsoft Advertising, Pinterest, Reddit, Snapchat, X, Google Demand Gen and display formats, Meta carousel, Stories and video placements, LinkedIn video, carousel, document, message and text ads. Answer "not in this plugin's checked table — check the platform's current spec", with no number. If the user pastes the current limit from their ad tool, use it and label it "limit given by you".
