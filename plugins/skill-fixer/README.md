# Skill Fixer

Fix a weak skill or instruction: compare two separate attempts, split a long task into smaller jobs, or adjust an agent plan as results arrive.
Works from supplied text and authorized local files. No extra account or paid API is required for planning or serial text work. To run agents, your assistant needs built-in agent tools. Runs use its normal allowance. Extra agents can add usage charges.
In Claude Code, the companion Agent Workflows is a required dependency. It must be available in the same marketplace or loaded locally alongside this package.

## Choose the technique

| Skill | Give it | You get |
|---|---|---|
| reconcile-skill-results | A weak instruction, a task to test it on, source facts and checks for a correct result | Two independent attempts, a chosen or merged task result, and briefs for running the instruction again |
| split-long-instructions | A long instruction and one sample input | Clear checks, instructions split by meaning, and a decision based on the same sample |
| orchestrate-skill-work | A complicated instruction and the task it should perform | An agent plan that adjusts to results, checked work and a final result; a plan only if you did not ask to run agents |

## Examples

- “This skill gives inconsistent answers. Run it with two agents and reconcile using my source facts.”
- “This long prompt misses steps. Split it by meaning and judge both arrangements on this sample.”
- “Run this instruction as a dynamic workflow. Adapt assignments only when a completed result shows a gap.”

Forks are agents that inherit the current conversation. Use them when the task needs that history and it is safe to share. Removing sensitive details from a brief does not remove them from inherited history. If the history is unsuitable to share, use fresh agents with a summary that omits those details. Fresh agents receive a brief with everything they need. Use them when work must start without the conversation history. Each attempt stays separate until the main agent checks and reconciles it.

Before testing a split, write down what a correct answer must include. Run the original instruction, then the two-part workflow on the same input. Run parts in order when one needs another's result. Run them together when they can work independently. Split a part again only if the judge can point to a corrected omission, a corrected fact, or a clearer answer under the preferences written before the runs. Stay within the fixed limit on runs. A tie or worse result stops the process. A result on one sample does not show that the instruction works reliably on other inputs.

## Companion and fallback

The current companion slug is `agent-workflows`. Its planning, execution and checking skills support the dynamic workflow. The Claude manifest contains `"dependencies": ["agent-workflows"]`, using the documented same-marketplace form. For local development, load both package paths with `claude --plugin-dir <companion-path> --plugin-dir <skill-fixer-path>`.

Claude Code cannot load this package with its required dependency absent. The inline workflow remains usable as supplied text, or in a host that loads the skills without Claude's dependency mechanism. It covers ready tasks, dependencies, checks, repairs with a fixed limit and combining outputs. Without native agent tools, the assistant can provide assignments or do serial work; it does not describe that as independent execution. See the bundled [platform sources](skills/orchestrate-skill-work/references/sources.md).

## Data and network

Network fetches: none. No web search, URL fetching, telemetry, bundled runner, MCP server or background service. The instructions use only supplied content and authorized named files. Built-in agent tools pass needed task context to your assistant's existing model provider. The package adds no model API integration and stores nothing itself; your host can retain conversations, agent transcripts and local artifacts. See [PRIVACY.md](PRIVACY.md).

Use redacted inputs and separate worker outputs. The task's existing permissions apply to every worker. This package does not install a runtime, handle credentials, send messages or publish changes.

## Support and license

Support: https://github.com/grayskripko/marketing-skills/issues

MIT. See [LICENSE](LICENSE).
