# Privacy

This package contains skills and references. It operates within the assistant conversation.

Data read: pasted model metadata, prompts, text samples, vector arrays, schemas, tokenizer counts and error exports, or files the user selects. These may contain personal or proprietary data. Use redacted identifiers and omit credentials; do not repeat unnecessary personal data in findings.

Purpose: embedding settings and vector/index contract review. Recipients: the assistant provider processes the conversation and any local calculation tools used by the assistant receive only the selected data. The package runs no service, stores no data, and adds no telemetry. The host controls conversation retention and deletion.

Network: none during ordinary audits. Only on a requested documentation refresh, the assistant reads relevant official documentation URLs listed in references/official-sources.md or official URLs supplied by the user, plus robots.txt, respecting robots restrictions. Redirects stay within official documentation sites. No vectors, source text, schemas, credentials or conversation context are transmitted in those requests. No embedding API, database, login or account access is used.

Controls: redact unnecessary fields, select only the relevant export, and delete the conversation through the host controls. Support: https://github.com/grayskripko/marketing-skills/issues
