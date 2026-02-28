# agent-skills

A collection of [OpenClaw](https://openclaw.dev) agent skills for macOS productivity tools. Each skill lives in its own top-level folder and can be published independently to a marketplace or plugin registry.

## Skills

### rem-cli
Manage macOS Reminders from the terminal. Creates, lists, updates, completes, deletes, searches, and exports reminders and lists. Supports natural language due dates, filtering, import/export, and multiple output formats.

Source: [github.com/BRO3886/rem](https://github.com/BRO3886/rem)

### ical-cli
Manage macOS Calendar events and calendars from the terminal. Full CRUD for events and calendars, natural language dates, recurrence rules, alerts, interactive mode, import/export (JSON/CSV/ICS), and multiple output formats.

Source: [github.com/BRO3886/ical](https://github.com/BRO3886/ical)

### gtasks-cli
Manage Google Tasks from the command line. View, create, update, delete tasks and task lists. Supports sorting, filtering, flexible date parsing, and multiple output formats (table, JSON, CSV). Requires Google OAuth2 credentials.

Source: [github.com/BRO3886/gtasks](https://github.com/BRO3886/gtasks)

### healthsync
Query Apple Health data stored in a local SQLite database. Read heart rate, steps, SpO2, VO2 Max, sleep, workouts, HRV, blood pressure, body metrics, and more. Read-only — never writes to the database.

Source: [github.com/BRO3886/healthsync](https://github.com/BRO3886/healthsync)

## Structure

Each skill folder contains:

```
<skill-name>/
  SKILL.md          # skill definition (name, description, system prompt)
  references/       # reference docs the skill uses (commands, schema, etc.)
```

## Keeping Skills Up to Date

When a new CLI version ships with updated skill files, run `/sync-skills` to fetch the latest from each source repo on GitHub and commit the changes here.
