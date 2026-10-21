# Privacy: Plugin Packaging

This skills-only package contains Markdown instructions and references, JSON manifests, a license and a static SVG icon. It bundles no executable program, hook, MCP or LSP server, connector or background process.

- Reviewing supplied text and files runs no commands, fetches no URLs and does no web search.
- Authorized local repair uses your assistant's existing tools to read and write the package folder you name and to run `claude plugin validate ./<package-directory>`.
- A check you ask to be run uses only a harmless skill and skips packages with hooks, MCP servers or `bin/`. Such a check runs in your existing host, which sends prompts and the files it reads to that host's model provider and may write session logs.
- The skills do not install dependencies, call MCP companions, connect accounts, send messages, publish or change settings.

The publisher operates no collection, telemetry or storage service and receives no task data through this package. Your assistant and host providers keep conversations, attachments and session logs under their own terms. Credentials are never needed; remove them and unnecessary personal data from files you paste and from public support requests.

Questions: https://github.com/grayskripko/marketing-skills/issues
