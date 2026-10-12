# Run protocol

The person running the panel follows these steps each period. The numbers below are workload and descriptive-monitoring heuristics chosen to keep manual work manageable; they do not guarantee statistical power. The user may change them, and the scorecard states the values used.

## Before the first run

1. Pick the engines (see `engines.md`) and fix the settings for each: signed in or out, web search on or off, country, device, language. Write them in the `settings` column as a short code, for example `out/web-on/US/desktop`.
2. Use a fresh chat for every run, so earlier messages do not influence the answer.
3. Default cadence: monthly, the same week. Use weekly equal-length periods for within-month movement visible in dated logs or a weekly decision cycle; use intervention-aligned equal-length windows when a change date is given. State the cadence and period dates used.
4. Calculate workload from the chosen design: actual phrasings × repetitions × engines. The default 25-ID allocation has 41 phrasings: 16 two-phrasing IDs plus 9 one-phrasing IDs. At 3 repetitions across 4 selected engines this is 492 runs. The older 45 × 3 × 4 = 540 is an illustrative workload, not the new default. If the plan exceeds stated capacity, use the 10-unbranded-ID, one-phrasing starter: 30 runs per engine, 60 for two engines. Use only selected relevant engines; do not fabricate IDs or observations to meet a gate. State actual workload and any breadth limitation.

## Each period

1. Default: 3 runs per prompt/phrasing/engine on different days, fresh chats, fixed settings, in the same week each month. Use all supplied 1-2 repetitions for a labelled exploratory snapshot, report observed rates, and give no default clear-change verdict. When supplied repeats disagree and the stated budget permits, propose 5 repetitions per affected cell in the next collection, keeping matched cells equally allocated across compared periods; 5 is a workload convention, not a guarantee of independence or statistical power. Use equal-length weekly windows for a supplied weekly decision cycle, or intervention-aligned equal-length windows when a change date is supplied. State repetitions, distinct collection dates, period boundaries and workload; never combine changed settings.
2. For each run, fill one row of the sheet:
   - `brand_mentioned`: yes if the brand name (or an obvious variant) appears anywhere in the answer text.
   - `brand_position`: the order in which the brand is first named among all brands named (1 = first), or empty.
   - `brand_cited_url`: a URL on the brand's own domain that the answer links as a source, or empty.
   - `competitors_mentioned`: tracked competitors named in the answer, separated by `;`.
   - `cited_urls`: every source URL the answer shows, separated by `;`.
   - `notes`: anything wrong the answer says about the brand, copied briefly.
3. Keep the settings unchanged. If something had to change, write it in `notes`.

## Definitions

- **Mention**: the brand is named in the answer text.
- **Citation**: the answer links a page on the brand's own domain as a source. A mention without a link is not a citation.
- **Run**: one prompt, one phrasing, one engine, one fresh chat, one date.

## Fan-out capture (optional)

Default: capture visible research plans or sub-questions for up to 5 priority prompts. Use all when fewer than 5 supplied prompts have a relevant unresolved gap; use more only when additional supplied prompts address distinct unresolved buyer questions requested in the analysis. State the count used. Capture only what the engine actually exposes.

## Bringing results back

Paste the filled sheet (or attach the CSV) and say which rows belong to which period if the `date` column does not make it clear.
