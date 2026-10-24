# Supplied post intake and relationships

Official sources checked 2026-10-11; publication dates are not stated on these pages. These mappings describe supplied data, not instructions to retrieve it. Runtime network scope remains none.

## Official account archive: select only post material

[X archive help](https://help.x.com/en/managing-your-account/how-to-download-your-x-archive), checked 2026-10-11, describes a ZIP and machine-readable HTML/JSON account material containing posts alongside Direct Messages, address-book data, follower/following lists, media and inferred interests/demographics. The archive is an account snapshot, not a topic-search dataset or a complete conversation collected from other accounts.

For intake, accept selected post text or post-only CSV/JSON with available IDs, dates, author labels and relationships. Prefer the relevant date/topic subset. Do not request the full ZIP or unrelated account files. If already supplied, use only post material and do not repeat private account contents. The archive help page does **not** publish a stable post filename, wrapper or field schema. Do not promise that every archive has a particular file or API-shaped object. Inspect supplied keys and the archive's own documentation first. If a post file is JavaScript-wrapped JSON, treat the wrapper as text; never evaluate it or run archive scripts. Do not invent missing mappings. If text cannot be isolated safely, request a post-only excerpt.

## Documented API-shaped JSON, supplied by the user

This is a documented export/input option, **not a claim about the account archive schema**. [X data dictionary](https://docs.x.com/x-api/fundamentals/data-dictionary), checked 2026-10-11:

| Field | Interpretation in supplied input |
|---|---|
| `id` | String post ID; preserve as text to avoid numeric precision loss. |
| `text` | Post text; use supplied `note_tweet.text` for a longer post's full body when present. |
| `author_id` | Author identity ID; a handle requires a supplied author mapping. |
| `created_at` | Creation timestamp for this object, in ISO format. |
| `conversation_id` | Conversation root ID, not necessarily this post's immediate parent. |
| `referenced_tweets` | Related post IDs with relationship types. |
| `edit_history_tweet_ids` | Related versions; do not mistake a revision for a later change of opinion. |
| `public_metrics` | Engagement at collection time, not truth or audience representativeness. |

Missing optional fields remain unknown. A short `text` alone may omit longer-post content. Do not silently replace a supplied post with unseen expanded text.

[X expansions documentation](https://docs.x.com/x-api/fundamentals/expansions), checked 2026-10-11, places related objects in `includes`. Join `author_id` to `includes.users[].id` for `username`, and referenced IDs to `includes.tweets[].id`. Array positions do not establish relationships. Included posts are context, not automatically extra observations in the selected account/date dataset. Count them as observations only if they independently meet the requested scope. Missing expansions are missing context, not proof of deletion or privacy.

## Relationship mapping and dates

[X data dictionary reference](https://docs.x.com/x-api/fundamentals/data-dictionary/reference), checked 2026-10-11, documents the following `referenced_tweets[].type` values:

| Type | Interpret supplied material as |
|---|---|
| `replied_to` | Reply to the referenced ID; not merely an @mention. |
| `quoted` | Own comment plus a referenced post; keep the two authors' words separate. |
| `retweeted` | Repost of the referenced object; do not attribute its wording to the reposter. |

Keep all relationship flags: a reply can also quote a post. Call an item an original only when the supplied export establishes that relationship fields were included and none apply; absent fields in a reduced export mean unknown type. A visible `RT @…` prefix is a clue, not a complete relationship contract.

Use the outer post's supplied creation time for that event, and the referenced object's timestamp for the target statement. If only target text/date is present, the repost event's date is unknown. Do not borrow it for account chronology. A conversation root ID does not supply missing replies or their order. Preserve supplied offsets; never assume local calendar dates equal UTC dates.

## Worked interpretations

Illustrative inputs, constructed 2026-10-11 from the documented fields above; not real account observations or evidence of parser execution:

- Row `Q` says “Might work”; it has `quoted → P`, and supplied `P` says “Always works.” Account claim: “Might work.” Topic “always” matches the quoted author only. Without supplied `P`, its words are unknown.
- Row `R` has `replied_to → P` and `conversation_id → ROOT`. Immediate parent is `P`; do not attach it directly to `ROOT` or reconstruct missing intermediate text.
- Row `S` has `retweeted → P`. Its outer timestamp dates the repost when supplied; `P.created_at` dates the target. Neither reposting nor quote commentary alone proves endorsement.
- Row `L` includes both a shortened `text` and full `note_tweet.text`. Analyze the full supplied body; do not count both bodies as separate posts. An edit-history relationship is version context, not evidence that an account later reversed its position.

Retain supplied URLs as citations without opening them. Where IDs or author mappings are absent, use row/excerpt labels and do not manufacture URLs, unique-post counts or identities.
