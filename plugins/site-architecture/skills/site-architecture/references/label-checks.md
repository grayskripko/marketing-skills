# Menu label checks L-01 to L-08

Run on header, dropdown, footer and breadcrumb labels. Report pass or fail with the labels and targets involved. These are judgement checks; say what a fix would look like rather than scoring.

| Id | Check | Example of a fail | Typical fix |
|---|---|---|---|
| L-01 | Vague label | "Resources" and "Learn" both open onto the same six guides | Name what is inside ("Guides", "Templates") or merge the two |
| L-02 | Two labels with overlapping scope | "Platform" and "Product" share four targets | One label per scope; move shared targets under one |
| L-03 | Internal jargon or code names | "Atlas" for the reporting module | Use the words customers use for the job |
| L-04 | Label differs from the heading of the page it opens | Menu says "Plans", page heading says "Pricing" | Match the label to the heading, or the heading to the label |
| L-05 | One target under two labels | `/integrations/slack` listed under Features and Integrations | One home (SA-01); a body link from the other section |
| L-06 | Utility links mixed into topical menus | "Careers" inside the Product dropdown | Move utility links to the utility layer (header corner or footer) |
| L-07 | One section named differently in header, footer and breadcrumb | "Docs" in the header, "Documentation" in the footer, "Help Center" in the breadcrumb | One name everywhere |
| L-08 | The customers' word is missing while an internal term is used | Customers say "invoices", the menu says "Billing objects" | Only when the user supplies customer wording (reviews, search terms, support tickets); otherwise "Not checked" |

Breadcrumbs: a section that is only one or two levels deep does not need a breadcrumb trail; show the current section clearly instead (NN-BC, guideline 7). A trail starts at the homepage, ends with the current page as plain text, and follows the hierarchy (NN-BC).
