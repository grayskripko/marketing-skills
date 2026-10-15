# Claude plugins by Sergey Skripko

38 free skills-only plugins in the Claude plugin directory. Each plugin lives in its own folder under `plugins/` on its own branch, with its own README, license and privacy note. Install them from the Claude plugin directory.

## AI agents and skills

| Plugin | What it does |
|---|---|
| [Agent Debugging](https://github.com/grayskripko/marketing-skills/tree/pl-agent-debugging/plugins/agent-debugging) | Debug a failed AI agent run from traces, logs, configuration, transcripts and output files; find the supported fault and get a repair or reproducible escalation. |
| [Agent Design](https://github.com/grayskripko/marketing-skills/tree/pl-agent-design/plugins/agent-design) | Design an AI agent for one process: decide whether an agent is needed, then write its implementation specification. |
| [Agent Evaluation](https://github.com/grayskripko/marketing-skills/tree/pl-agent-evaluation/plugins/agent-evaluation) | Plan agent evaluation and verify agent output against supplied requirements, artifacts, action receipts and escalation records. |
| [Agent Guardrails](https://github.com/grayskripko/marketing-skills/tree/pl-agent-guardrails/plugins/agent-guardrails) | Define and check agent permissions, human approval and agent escalation for a real workflow. |
| [Agent Recovery](https://github.com/grayskripko/marketing-skills/tree/pl-agent-recovery/plugins/agent-recovery) | Plan recovery of an interrupted AI agent run from checkpoints and action receipts; identify what can resume and which effects need checking before retry. |
| [Instructions Cleanup](https://github.com/grayskripko/marketing-skills/tree/pl-instructions-cleanup/plugins/instructions-cleanup) | Fix conflicting CLAUDE.md and AGENTS.md instructions: map the active scopes, repair stale references and return a minimal patch that preserves approvals. |
| [MCP Debugging](https://github.com/grayskripko/marketing-skills/tree/pl-mcp-debugging/plugins/mcp-debugging) | Troubleshoot MCP connection, authentication and missing-tool errors in my actual client from pasted traces, logs, configs, transcripts or files. |
| [Plugin Packaging](https://github.com/grayskripko/marketing-skills/tree/pl-plugin-packaging/plugins/plugin-packaging) | Repair a skills-only Claude plugin that fails to install, load skills or find its resources. |
| [RAG Evaluation](https://github.com/grayskripko/marketing-skills/tree/pl-rag-evaluation/plugins/rag-evaluation) | Evaluate and debug wrong RAG answers, retrieval quality, missing documents and grounded citations from the question, source documents, retrieved passages and response. |
| [Tool Schemas](https://github.com/grayskripko/marketing-skills/tree/pl-tool-schemas/plugins/tool-schemas) | Fix AI agent tool contracts when connections work but tool choices, arguments or results fail. |

## Marketing and sales

| Plugin | What it does |
|---|---|
| [Ad Copy & Creative Preflight](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/ad-creative) | Checks ad text before it runs and reads creative tests after. |
| [AI Search Visibility & Brand Mentions (GEO/AEO)](https://github.com/grayskripko/marketing-skills/tree/main/plugins/ai-seo) | Check whether AI answers mention your brand in ChatGPT, Perplexity and Google AI Overviews, using answers you paste or log to show how often you appear, how your business is described and which sources get cited instead. |
| [Blog Content Strategy, Calendar & Content Audit](https://github.com/grayskripko/marketing-skills/tree/wind/plugins/content-strategy) | Decide what your team should publish next: plan blog topics and content marketing priorities around your goals and company evidence, and turn your backlog into a weekly editorial calendar that fits your writers' hours, for your own team or your agency's clients. |
| [Churn Prevention](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/churn-prevention) | Five skills for subscription churn, each computed from your own data. |
| [Cold Email, LinkedIn Outreach & Deliverability](https://github.com/grayskripko/marketing-skills/tree/wind/plugins/cold-email) | Draft B2B cold outreach and prospecting emails, follow-ups and LinkedIn connection notes and messages from your offer and audience; review and rewrite cold emails getting no replies, keeping every number, name and claim. |
| [Community & Reddit Marketing](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/community-marketing) | Community marketing without astroturfing. |
| [Copyedit & Proofreading](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/copy-editing) | Editing tools for prose you already have, from help articles and notices to reports and policies. |
| [CRO Checkout Audit and Test](https://github.com/grayskripko/marketing-skills/tree/squall/plugins/cro) | Conversion rate optimization (CRO) for your own pages, forms, checkouts and A/B tests. |
| [Customer Research Kit](https://github.com/grayskripko/marketing-skills/tree/wind/plugins/customer-research) | Turn interview notes, reviews, support tickets and cancellation reasons you paste into findings you can check: the main themes first, each with how many customers said it, in their exact words, and where they disagree. |
| [Lead Magnets](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/lead-magnets) | Pick a lead magnet for what you sell and decide whether to gate it; draft it from your own material with no invented figures; check an opt-in page, form, thank-you page and confirmation email against dated US, EU and UK consent and sender rules; plan what each sign-up may receive given the consent it gave; and compare sign-up and sales-call rates by magnet, with honest ranges for small numbers. |
| [Marketing Ideas & Growth Experiments](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/marketing-ideas) | Helps a small team decide which marketing ideas deserve money, and whether a test worked. |
| [Marketing Psychology & Dark Pattern Check](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/marketing-psychology) | Evidence grades and consumer-protection rule checks for the psychology in your marketing. |
| [Programmatic SEO Gate](https://github.com/grayskripko/marketing-skills/tree/breeze/plugins/programmatic-seo) | For template-based SEO pages built from a dataset (a page per city, tool, integration or product), not programmatic advertising. |
| [RevOps Metrics & Forecast Accuracy](https://github.com/grayskripko/marketing-skills/tree/gust/plugins/revops) | Check stated stage probabilities against what actually closed, build an ARR bridge with gross and net revenue retention (GRR, NRR) that reconciles to zero, backtest forecast methods on your own history, plan a revenue target back to deals, SQLs and team capacity, and measure funnel conversion by cohort and source. |
| [Sales Enablement & Role-Play](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/sales-enablement) | Coaching and practice for sellers. |
| [SEO Audit](https://github.com/grayskripko/marketing-skills/tree/main/plugins/seo-audit) | Use cases: SEO audit, website audit, ecommerce store SEO, organic traffic drop, technical and on-page SEO, Google Search Console errors, pages Google is not indexing. |
| [Site Architecture & Faceted Navigation](https://github.com/grayskripko/marketing-skills/tree/storm/plugins/site-architecture) | Plan a website's information architecture: a page tree where every page has exactly one parent, URL rules, navigation labels and breadcrumbs; a link plan computed from a links export (source and target) that uses only your own URLs and shows click depth before and after; hub page and child page link specs; which filter URLs get indexable pages, with the URL count worked out; and a redirect map checked for chains, loops and homepage targets for URL changes and site moves. |
| [Website Copywriting & Positioning](https://github.com/grayskripko/marketing-skills/tree/main/plugins/copywriting-kit) | Edit, diagnose and rewrite copy for your own small-business or SaaS website: edited text first with every number, name and claim kept, a plain diagnosis of what is broken before any rewrite, claims checked against your own evidence, page drafts from your facts, and a brand voice guide from your own writing. |

## Small business and documents

| Plugin | What it does |
|---|---|
| [Booking FAQ](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/booking-faq) | Write booking FAQs, explain how to book, draft booking replies and check existing booking text using your approved terms. |
| [Client Briefs](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/client-briefs) | Check client emails, discovery notes and a draft brief before quoting. |
| [CSV Cleanup](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/csv-cleanup) | Clean and merge Excel and CSV exports without changing the originals. |
| [Hiring Interviews](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/hiring-interviews) | Prepare hiring interviews from approved role requirements and organize the panel's notes. |
| [Newsletter Review](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/newsletter-review) | Check and edit your newsletter using the draft, source excerpts and approved offer terms you supply. |
| [Product Returns](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/product-returns) | Analyze product return reasons and reviews to find listing fixes, product investigations and supplier briefs for each product code (SKU). |
| [Scope Changes](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/scope-changes) | Check whether a new client request is extra work by comparing it with the approved scope and later approved changes. |
| [SKU Margin](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/sku-margin) | Calculate product margins after costs, returns and ads. |
| [Tenant Replies](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/tenant-replies) | Draft tenant replies from signed leases, amendments and case facts you provide. |
| [Voice Messages](https://github.com/grayskripko/marketing-skills/tree/reef/plugins/voice-messages) | Clean up voice notes and dictated transcripts so they are easy to read and still sound like you. |

## Author

Sergey Skripko. I build AI agents and fix poorly working skills.

If a plugin or a skill of yours works wrongly for your task, write in [GitHub Discussions](https://github.com/grayskripko/marketing-skills/discussions) — I read every message. Bugs: [GitHub Issues](https://github.com/grayskripko/marketing-skills/issues).

## License and privacy

Each plugin folder has its own LICENSE (MIT) and PRIVACY.md. The plugins contain no code and store nothing.
