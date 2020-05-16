# OmniFocus-Automation

The Process Inbox automation processes tasks in the inbox and matches them with a collection of TaskPaper templates stored in [Bear](https://bear.app).

The TaskPaper templates have placeholders which are delimited thusly: `«placeholder»`

Default values are specified like `«placeholder|default»`

Based on where the placeholder is in the TaskPaper, Process Inbox can determine what type of field to prompt to the user and if it is in a `@tags(Path : to : «placeholder»)` construct, will provide a selector for appropriate tags.

Conditionals can be set up by putting the «placeholder» inside a `@dropped(«placeholder»)` construct with the negation looking like this: `@dropped(!«placeholder»)`

Either `@defer(«placeholder»)` or `@due(«placeholder»)` will prompt for a date, and you can have a default like this: `@defer(«placeholder|2w»)` to defer 2 weeks. A second task that says `@defer(«placeholder»+3d)` will be deferred 3 days later than the first one.

More information in [the wiki](https://github.com/cgarrigues/OmniFocus-Automation/wiki).
