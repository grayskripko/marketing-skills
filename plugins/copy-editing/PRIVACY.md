# Privacy

Copyedit & Proof Kit consists of instructions and reference tables that an AI assistant reads. It has no server, no account and no storage of its own.

- Network scope: this plugin runs no web search and calls no service. Only the content-refresh skill may fetch, and only one public page at a URL you give plus that site's `/robots.txt`, through your assistant's own fetch tool. It skips the page if robots.txt disallows it, and never logs in, submits forms or tries to get past bot protection; if the fetch fails, is disallowed or no such tool exists, it asks you for the text instead. Nothing is stored, and no files or settings are changed unless you ask. If your assistant has a code tool, the skills may use it to compute counts, weekdays, totals and differences.
- Categories of data: the text you paste or attach, and the one public page (plus that site's robots.txt) you may ask it to fetch. The skills need no personal data. Names inside your text are treated as fixed and are not changed.
- Purpose: editing that text during the conversation.
- Recipients: the text goes to the provider of the AI assistant you use, under that provider's terms. The plugin sends it nowhere else. If you ask for a page to be fetched, that site receives a request from your assistant's fetch tool.
- Retention: the plugin keeps nothing. Retention of your conversation is set by your assistant provider.
- Your controls: remove contact details and other personal data that are not part of the job before pasting. Tables never repeat emails or phone numbers.

Questions: https://github.com/grayskripko/marketing-skills/issues
