# Privacy: UTM Governance

UTM Governance reads pasted campaign links, naming rules and readable campaign-register exports to produce naming and correction proposals in the current conversation.

- Data: campaign names, IDs, channel vocabulary, owners and dates; supplied URLs may also contain personal data, access codes or signatures. Redact those values before sharing. Output uses row references and masked sensitive fields.
- Network: none. No campaign URLs, robots.txt, redirects, analytics accounts or remote files are fetched. Bundled references are read locally.
- Recipients: the assistant provider processes the supplied conversation and files. The package sends no data to another service and has no telemetry.
- Storage: the package operates no service and retains no data of its own. Conversation and file retention follow the assistant's settings.
- Controls: provide only relevant columns, redact identifiers that are not needed, and use the assistant's conversation/file deletion controls.

[Support](https://github.com/grayskripko/marketing-skills/issues)
