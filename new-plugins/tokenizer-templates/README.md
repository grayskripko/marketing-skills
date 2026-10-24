# Tokenizer Templates

Paste tokenizer config, template, special-token map and rendered transcript; receive a serialization audit and corrected template/caller text.
For AI and agent builders checking chat inputs for inference, prefills or training.
Needs pasted text or exported files; no account, connector, API key or installation is required.

| Skill | Ask for | Receive |
|---|---|---|
| audit-chat-serialization | Check config, template, token map, messages, caller and rendered transcript | Evidence-backed serialization findings and corrected fragments |
| repair-chat-template | Fix a failing template, caller or message shape | Copyable patch and expected message boundaries |

Checks cover effective file/object selection, empty-tool template choice, named-field continuation, completed-training masks and token-variable overrides.

Paste the checkpoint/revision and Transformers version when available. Include escaped whitespace and caller flags. Tool and multimodal exports can be audited as text; exact format edits use the supplied checkpoint's rules.

Network: none for normal work. Only an explicitly requested documentation refresh fetches relevant official Hugging Face documentation or Transformers source pages on GitHub. Pasted content is not uploaded; transcript links, media and weights are not fetched. This package contains instructions, references and an icon, with no runtime code or telemetry.

[Privacy](PRIVACY.md) · [License](LICENSE) · [Support](https://github.com/grayskripko/marketing-skills/issues)
