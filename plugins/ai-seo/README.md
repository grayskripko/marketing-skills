# AI Search Visibility Kit

## What it does

Measure how ChatGPT, Perplexity, Google AI Overviews and other AI answers mention and cite your brand, check whether your pages can be quoted accurately, and plan honest work on the third-party sites those answers draw on. The plugin never queries AI engines itself and never invents their answers: you run a fixed prompt panel or paste what you saw, and every number comes with its calculation.

## Skills

Each skill is chosen by what you give it:

| You give | Skill |
|---|---|
| "Do we show up in ChatGPT?" with a brand, a category and competitors, no results yet | `ai-visibility-panel`: prompt panel as CSV and a run protocol |
| A filled panel sheet or many logged runs | `ai-visibility-report`: per-engine scorecard, a clear-change-or-noise verdict per engine, sources cited instead |
| A Bing AI Performance export, a Search Console generative AI report or AI Assistant channel data | `ai-citation-data`: pages ranked by value against citation share |
| One page, and a question about being quoted in AI answers | `ai-page-audit`: a plain verdict, the changes that matter, rewrites, a 0-18 checklist score and a warning if the page hides text aimed at AI |
| One query plus answers you copied | `ai-answer-gap`: what to add or correct, with a sub-question coverage matrix |
| URLs cited in answers, or "how do we get described correctly elsewhere" | `ai-offsite-plan`: source table and fact pack |

## Examples

- "Our AI visibility panel: Engine A mentioned us in 3/30 runs in Aug, 9/30 in Sep; 4 prompts rose, 0 fell. Real change or noise?"
- "Can AI answers quote this? <div data-nosnippet>Invoices over $5,000 need two signers.</div> Target: two-signer approval"
- "Build an AI visibility prompt panel for Acme Invoicing, a B2B invoicing app. Competitors: Northwind Pay and Globex Billing."

To try the scorecard and the export analysis with files, use the small fictional panel logs and exports in the repository: https://github.com/grayskripko/marketing-skills/tree/main/samples/ai-seo

## How it works

The panel skill writes 20-30 buyer prompts in fixed buckets and a protocol: each engine measured separately, several runs per prompt, fixed settings. You run it on the engines you care about, for example ChatGPT, Perplexity, Google AI Overviews and AI Mode, Gemini, Claude or Microsoft Copilot, and log the results in the sheet. The scorecard prints every rate with its sample size and uses a written rule to separate a clear change from run-to-run variation. Pages that lose out go to the page check and the answer gap; third-party sources go to the off-site plan, which only uses disclosed, rule-abiding routes. Claims such as "add llms.txt" or "schema gets you cited" are answered from sourced notes, not repeated as advice.

## Data and network

Network scope: this plugin fetches only URLs you type or paste, including URLs inside logs or exports you paste, plus the robots.txt file of those sites. It fetches public pages only, never logs in or submits forms, and skips paths a site's robots.txt disallows. At most 10 page fetches per run; robots.txt files do not count. Web search is used only when you explicitly ask for it, at most 10 queries per run, and every query is listed in the output. The plugin never queries AI answer engines, runs no code of its own and stores nothing; if the assistant has a code or spreadsheet tool, it may use it to compute the tables you see.

Logs, exports and brand names you share stay in your conversation with the assistant.

## Troubleshooting

- **No web tool:** paste the page source ("view source") and robots.txt.
- **Export not recognized:** say which report produced it, or paste the header row.
- **Thin sample warning:** run each prompt at least three times per engine before comparing periods.
- **Mixed settings in the log:** keep one setting per engine, or split the log.

## Support

Report problems and requests through GitHub Issues: https://github.com/grayskripko/marketing-skills/issues

## License and privacy

MIT License, see [LICENSE](LICENSE). Privacy policy: [PRIVACY.md](PRIVACY.md).
