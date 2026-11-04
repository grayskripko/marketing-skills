# Output formats

Every value in these formats comes from the tool's rows. The example rows show the shape only; take the real names, dates and links from the tool.

## Table

Dates in ISO or the user's own date style. Newest first; oldest first for a timeline.

| Update (Google's name) | Kind | Start | End | Days | Source |
|---|---|---|---|---|---|
| <name> | <kind> | <begin> | <end, or «still rolling out»> | about <days> | [Google](<google_url>) |

Days = the tool's `days` field: calendar days from the begin date to the end date on Google's dashboard (21 May to 2 June = 12). Google gives no day count, so in text write «about <n> days»; a column headed «Days (approx.)» is fine. A row still rolling out has no day count; write the days so far as of the as-of date if the user needs one.

## Annotation rows

For analytics tools that take one note per date (GA4 annotations, Looker Studio, a spreadsheet column):

`<begin> | Google <name> starts (ends <end>) | <google_url>`

One note per update at the start date, with the end date in the text. Add a second note at the end date only if the user asks for both. Never invent the end of an update still rolling out.

## CSV

Only when the user wants to import or paste; write it as a file only if asked.

```
start_date,end_date,name,kind,days,source_url
<begin>,<end>,<name>,<kind>,<days>,<google_url>
```

Leave `end_date` and `days` empty for an update still rolling out.

## Chart bands

When the user's chart is built in code in this chat: one shaded vertical band per rollout window, labelled with the short name, pale enough that the user's line stays readable. An update still rolling out gets a band up to the as-of date with an open edge.

- matplotlib: `ax.axvspan(start, end, alpha=0.12)` and `ax.text(start, ax.get_ylim()[1], name, rotation=90, va='top', fontsize=8)`
- plotly: `fig.add_vrect(x0=start, x1=end, opacity=0.12, line_width=0, annotation_text=name, annotation_position="top left")`

Change nothing else in the user's code.

## Client paragraph

«Between <since> and <as_of>, Google confirmed <n> Search ranking updates: <names with month>. Each rolled out over about <min> to <max> days. These dates show when Google changed its ranking systems; they do not by themselves show that any one site was affected. If a traffic change lines up with one of them, it is a lead to check against the site's own data, not proof.»

Then the short list with Google's links, and the as-of line.
