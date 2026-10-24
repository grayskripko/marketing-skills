# Reading supplied conversation structure

Read [supplied post intake and relationships](../../twitter-account-research/references/sources.md) for structured data. It contains dated official field mappings and examples separating replies, quotes, reposts and event dates.

Follow immediate `replied_to` edges when supplied. Shared conversation-root IDs group a conversation but do not establish a complete thread or a direct reply edge. Join related objects by ID, not array position. A reply can also quote another post; distinguish the parent being answered from the quoted author's words. When full longer-post text is supplied, use it rather than a shortened body. Missing posts, quoted bodies, attachments and previous versions remain unknown. Thread numbering alone does not reconstruct any of them. Links stay citations and are not opened.
