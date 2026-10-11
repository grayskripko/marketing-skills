# Run protocol

The person running the panel follows these steps each period. All numbers below are heuristics chosen to keep manual work manageable while giving enough runs to see real changes; the user may change them, and the scorecard states the values used.

## Before the first run

1. Pick the engines (see `engines.md`) and fix the settings for each: signed in or out, web search on or off, country, device, language. Write them in the `settings` column as a short code, for example `out/web-on/US/desktop`.
2. Use a fresh chat for every run, so earlier messages do not influence the answer.
3. Decide the cadence: once a month, in the same week of the month.
4. Check the workload before committing: runs per period = prompt phrasings × runs per prompt × engines. A full panel of about 45 phrasings, 3 runs and 4 engines is about 540 manual runs a month; a starter panel of 10 prompts, one phrasing, 3 runs and 2 engines is 60. Start small and grow only if the team keeps up.

## Each period

1. Run every prompt and phrasing at least 3 times per engine, on different days within the period.
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

For up to 5 priority prompts, if the engine offers a research mode that shows its plan or sub-questions, copy them into a separate list with the prompt ID. They are used later for the answer-gap check.

## Bringing results back

Paste the filled sheet (or attach the CSV) and say which rows belong to which period if the `date` column does not make it clear.
