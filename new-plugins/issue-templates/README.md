# Issue Templates

Repair GitHub issue-form YAML from pasted validation errors, existing repository labels, organization issue types and project-assignment permissions.
For repository maintainers fixing rejected forms or missing assignments. Supply YAML and the error or unwanted behavior; for routing, add label/type inventories and project permissions. No account, API key or installation is required.

## What this package runs and connects to

This is a skills-only package of Markdown instructions and reference text, JSON metadata, and a static SVG icon. It includes no executable scripts, dependencies, installers, hooks, MCP or LSP servers, or background processes. Installing it does not run a bundled program or connect an account. The Claude and Codex manifests describe the same skills for their respective hosts; neither launches a server.

Normal repairs use task text, attachments and local files you explicitly supply. Both skills permit an external read only when you request updated platform verification: your assistant fetches the relevant public GitHub Docs pages linked in [references/github-rules.md](references/github-rules.md) and their redirects. The reference register also asks for those sources to be re-opened near submission. These are real retrieval instructions, so this package is not strictly offline. No pasted private content is sent in a URL or query. Support and publisher links identify pages, not account connections.

The skills do not instruct code execution, software installation, API calls, message delivery or publication. They return proposed YAML patches and owner actions, including placing forms in `.github/ISSUE_TEMPLATE/`, creating missing labels or configuring native project auto-add workflows; they do not perform those repository or account changes. A local parser is mentioned only as a limit on what parsing can prove, not as an instruction to run one. Any output file you explicitly request is created by your assistant's existing file tools, not by a bundled program.

The publisher receives no task data and operates no collection, telemetry or storage service for this plugin. Your assistant provider processes and may retain your conversation, attachments and tool activity under its own terms. Requested public-document reads contact GitHub Docs and any redirect destinations through your assistant's retrieval tools.

| Skill | Input | Output |
| --- | --- | --- |
| repair-issue-form | YAML and validation errors | corrected form or minimal patch, with failing-field reasons |
| repair-issue-routing | YAML, labels, types and permissions | metadata patch and precise settings changes |

Use “GitHub rejects this dropdown; fix the form” or “Outside reporters miss our project; here are their permissions.” Both work from pasted text and exports. Current rules include upload fields, min_length, dropdown defaults, existing labels and project-opener permissions and auto-add workflow capacity. Sources and verification dates are in [references/github-rules.md](references/github-rules.md).

## Support and license

[Support](https://github.com/grayskripko/marketing-skills/issues). MIT; see [LICENSE](LICENSE).
