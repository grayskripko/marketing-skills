# Privacy: Skill Fixer

This package contains instructions, reference text and an icon. It has no telemetry or service of its own.

- Data read: supplied instructions, sample inputs, results and authorized named local files. These can contain confidential or personal information. Use relevant excerpts and redact secrets and unnecessary identifiers.
- Purpose: produce independent task attempts, split long instructions and coordinate checked agent workflows.
- Network fetches: none. No web search or URL fetching. Native agents use the assistant's existing tools and send required task context to its model provider; forks inherit the current conversation, including history outside the worker brief. Redacting a brief does not redact that history. Use fresh agents with a redacted summary when the inherited history is unsuitable to share. Every worker brief carries the no-network restriction. This package adds no model API integration.
- Recipients: the assistant's existing provider. A separately authorized provider may process task context under its own terms; no other recipient is added by this package.
- Retention: no plugin storage service. The assistant may retain conversations, agent transcripts and usage logs. Authorized edits and saved task artifacts persist in the chosen workspace until removed.
- Controls: minimize shared context, redact secrets before dispatch, use fresh briefs when the whole conversation is unnecessary, keep output ownership separate, and use the host's controls to remove records.
- Actions: existing task permissions and allowance apply to every agent. No credentials, messaging, publishing or account integration are handled by this package. Claude Code may resolve the declared companion dependency through its own plugin installation process; the skills themselves fetch nothing.

Questions: https://github.com/grayskripko/marketing-skills/issues
