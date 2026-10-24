# Reddit Research

Research supplied Reddit threads and public JSON exports about a topic, product or pain point.

For product teams, researchers and founders reviewing feedback. The workflow starts with material you supply; you select the threads and comments to analyze. Supply thread text with its links, or a JSON export you already have permission to use. No accounts, keys or paid APIs are required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a program or connect an account.

These skills work only from task text, attachments, and local files that you explicitly supply. They do not instruct the assistant to run code, install software, search the web, fetch URLs or robots.txt, call APIs, send messages, publish content, or change account settings. URLs in this package identify sources or support pages; they are not connection endpoints or retrieval instructions. A supplied URL is treated as text: paste the relevant content instead.

The publisher receives no task data and operates no collection, telemetry, or storage service for this plugin. Your assistant provider still processes and may retain your conversation and attachments under its own terms. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

| Skill | Ask for | Result |
|---|---|---|
| reddit-themes | Summarize complaints, needs or competing product experiences | Themes, contrary views and short supporting quotes with links |
| reddit-quotes | Pull exact customer wording from comments | A quote table with source links and context |

Paste comments with their thread/comment URLs and dates where available. Or attach public JSON content; nested comment replies are included. If all you have is a topic or a link, paste the relevant material first. The assistant can walk you through what to copy: post title/text, relevant comments, parent replies, permalink, community and date. Do not paste credentials or unnecessary personal details.

Counts refer to the supplied readable records. Matching copies with the same ID or permalink count once; conflicting copies count as one known comment with unresolved theme membership. Overall fractions distinguish confirmed minimums from resolved-record subtotals. Omitted and deleted comments are not filled in. Quotes keep the speaker's wording and exceptions. Missing links remain visible. A selected sample does not prove market prevalence, causes of churn or current Reddit-wide sentiment.

Network: none. The skills analyze text and files you supply in the current conversation. They do not fetch URLs or robots.txt, run searches, log in, post, message, install dependencies or connect to an API. Source links in the answer come from your supplied metadata; their current availability is not checked. There is no telemetry or plugin-owned storage. Your assistant's processing and conversation retention apply; see [PRIVACY.md](PRIVACY.md).

Examples:

- “What are people complaining about in these pasted threads?”
- “Pull exact quotes about onboarding, with the links I supplied.”
- “Compare these two products from this Reddit JSON export.”

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
