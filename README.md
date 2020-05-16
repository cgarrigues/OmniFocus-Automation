# OmniFocus-Automation

The Process Inbox automation processes tasks in the inbox and matches them with a collection of TaskPaper templates stored in [Bear](https://bear.app).

The TaskPaper templates have placeholders which are delimited thusly: `«placeholder»`

Default values are specified like `«placeholder|default»`

Based on where the placeholder is in the TaskPaper, Process Inbox can determine what type of field to prompt to the user and if it is in a `@tags(Path : to : «placeholder»)` construct, will provide a selector for appropriate tags.

Conditionals can be set up by putting the «placeholder» inside a `@dropped(«placeholder»)` construct with the negation looking like this: `@dropped(!«placeholder»)`

Either `@defer(«placeholder»)` or `@due(«placeholder»)` will prompt for a date, and you can have a default like this: `@defer(«placeholder|2w»)` to defer 2 weeks. A second task that says `@defer(«placeholder»+3d)` will be deferred 3 days later than the first one.

The Bear notes have a header with the name of the Template and are tagged with **#taskpaper** and sometimes **#mustmatch**. The template name may have placeholders in it. If so, the template is only offered if the task matches the name. The template with a **#mustmatch** tag is also only offered if it matches.

An expanded task may be saved back to Bear with the **#mustmatch** added to save from re-entering tasks that recur frequently.

If there are no placeholders to expand, the template is applied without prompting.

More information in [the wiki](https://github.com/cgarrigues/OmniFocus-Automation/wiki).
