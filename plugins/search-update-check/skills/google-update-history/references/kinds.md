# Kinds

The tool sorts each confirmed update into one kind by Google's own name. This file only maps the user's words to a kind; it holds no facts about what an update did, so nothing here goes stale.

| The user says | `kind` | What to say |
|---|---|---|
| core, broad core, core algorithm | `core` | |
| spam, link spam, spam policy | `spam` | |
| reviews, product reviews | `reviews` | |
| Discover | `discover` | |
| «Google update», «algorithm update», «algo update», no kind named | omit | all kinds |
| helpful content, page experience, anything else Google named | omit, then read the names | Report only rows whose Google name contains the user's words; they come back as kind `other`. If none match: «No confirmed update under that name in the list.» |
| AI content, scaled content, site reputation, expired domains | omit, then the `spam` rows by name | «The list holds Google's update names and dates, not what each update targeted. Google describes spam policies such as scaled content abuse on its spam policies page.» Never say which update targeted which practice. |
| penalty, manual action | do not call | «A manual action is not an update; it shows in Search Console under Manual actions.» |
| Google Ads, Maps, Bing, Yandex | do not call | Out of scope: the list covers Google Search ranking updates only. |
