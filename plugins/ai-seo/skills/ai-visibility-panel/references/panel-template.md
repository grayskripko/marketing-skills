# Panel sheet template

The panel is delivered as a CSV code block with these columns, in this order. The scorecard skill expects the same columns.

| Column | Filled by | Values |
|---|---|---|
| prompt_id | panel | P01, P02 ... stable across periods |
| bucket | panel | discovery, use-case, comparison, alternatives, problem, brand-direct |
| branded | panel | yes or no |
| phrasing | panel | a or b |
| prompt | panel | the exact prompt text |
| engine | panel | a short engine label, one per row |
| run | person running | 1, 2, 3 ... |
| date | person running | YYYY-MM-DD |
| settings | person running | short code, for example `out/web-on/US/desktop` |
| brand_mentioned | person running | yes or no |
| brand_position | person running | 1, 2, 3 ... or empty |
| brand_cited_url | person running | a URL on the brand's domain, or empty |
| competitors_mentioned | person running | names separated by `;` |
| cited_urls | person running | URLs separated by `;` |
| notes | person running | free text, for example a wrong fact the answer stated |

## Example

```csv
prompt_id,bucket,branded,phrasing,prompt,engine,run,date,settings,brand_mentioned,brand_position,brand_cited_url,competitors_mentioned,cited_urls,notes
P01,discovery,no,a,"invoicing software for a 20-person agency",Engine A,,,,,,,,,
P01,discovery,no,b,"We are a 20-person agency. What invoicing software should we look at?",Engine A,,,,,,,,,
P14,brand-direct,yes,a,"What does Acme Invoicing cost and who is it for?",Engine A,,,,,,,,,
```

Deliver one row per prompt, phrasing and engine with the run columns empty. The person running the panel copies each row for runs 2 and 3.
