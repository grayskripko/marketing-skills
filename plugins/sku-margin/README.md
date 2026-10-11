Calculate product margins after costs, returns and ads, and compare your proposed prices, discounts and ad budgets.
For sellers and the accountants who review their decisions. Upload exports or paste tables for sales, refunds, fees, shipping, product and packaging costs, and ads. Include the period, country, currency and fee terms. Include your tax and accounting treatment where known.

No accounts, keys, store connection or paid API are required. To use uploaded CSV or Excel files, your AI app must be able to read them. Larger tables need a local calculation tool. Scans need text recognition (OCR). You can paste readable tables without setup. Using your AI app or obtaining your existing exports may cost money.

## What this package runs and connects to

The seller-analysis skills use only task text, attachments and local files you explicitly supply, plus bundled method notes. They instruct no web search, URL or robots.txt retrieval, API calls, account connections, software installation, message delivery, publishing, price changes or ad-account changes. Repository and support URLs identify reference pages, not retrieval instructions. Paste the relevant content instead of supplying only a URL.

This workflow can use your assistant's existing file-reading, OCR and local calculation tools to read authorized exports and calculate from supplied values. Any worksheet or output file you request is created by your assistant's existing tools in your requested workspace. Tool execution and temporary files are managed by your assistant provider. No seller runtime, installer, dependency setup, hook, MCP or LSP server, or background process is provided; installing the plugin does not launch a program or connect an account. The `.claude-plugin` and `.codex-plugin` directories contain platform metadata.

The current folder also retains development evidence, including `tests/run-eval.py`; it is not invoked by the skills or manifests. If manually run, this harness copies existing Codex authentication into `/tmp/seller-margin-check-codex`, launches the locally installed Codex CLI with `gpt-6.1-sol`, sends test prompts and skill text to the configured assistant provider, and writes inputs, answers, logs and evaluation JSON under `tests/` (or `SELLER_EVAL_DIR`). It also creates `/tmp/seller-margin-check-eval`. It is a network-capable development harness, so this folder is not a clean no-execution release package. Before submission, move tests, evaluation records, `BUILD-NOTES.md` and `REVIEW.md` outside the submitted folder as directed by the packaging rules.

The publisher operates no task-data collection, telemetry or storage service for these skills. Your assistant provider processes and may retain conversations, attachments and tool outputs under its own terms. The seller-analysis workflow makes no plugin-directed network requests; this does not describe the assistant provider's inference traffic or the separately run development harness.

## Skills

- [Reconcile seller exports](skills/reconcile-seller-exports/SKILL.md): match rows and totals, explain differences and show missing costs.
- [Calculate SKU contribution](skills/calculate-sku-contribution/SKILL.md): show the amount left after included variable costs, before and after ads.
- [Compare price and ad scenarios](skills/compare-price-and-ad-scenarios/SKILL.md): compare your proposed prices, discounts or ad budgets with clearly stated assumptions.

Ask: “Can I afford this discount? Here are my sales, fees and costs.” Or: “Which SKUs still contribute after ads and refunds?” The result is a calculation table linked to your input rows, with formulas and missing inputs. Shared costs need a stated split. Different currencies stay separate unless you supply conversion terms.

Contribution is not net profit. Missing costs do not become zero; fixed overhead stays separate. Scenarios do not predict demand. The result states the country or jurisdiction and tax/accounting treatment you supply. Missing details stay unresolved.

The seller-analysis skills fetch nothing from the network, including URLs or robots.txt. No usage tracking, live account access, price changes, ad changes or background monitoring. Only authorized inputs are read; buyer contact details are unnecessary. Your AI app handles the conversation and any generated worksheet under its own settings. See [PRIVACY.md](PRIVACY.md) and [LICENSE](LICENSE).
