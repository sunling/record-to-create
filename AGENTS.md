# Project Instructions

This repository helps the user capture daily life and inputs, review what is recurring, and move selected ideas toward expression or action.

## User settings

- Timezone: `YOUR_TIMEZONE`
- Preferred language: follow the language used by the user in the current request.

If the timezone is still a placeholder and the correct local date matters, ask the user once. Do not silently use UTC.

## Core rules

- Treat the user's words and records as the source of truth.
- Never invent events, quotes, sources, names, feelings, motivations, or conclusions.
- Preserve uncertainty, contradiction, and unfinished thinking when they are present.
- Make recording easy. Do not require perfect categorization or a complete template.
- Prefer one useful file over several derivative files.
- Do not turn every record into a task, article, or project.
- When reviewing, support observations with specific dates and relative file paths.
- Protect privacy. Flag sensitive details before suggesting public output.

## Storage

```text
daily/inputs/YYYY/YYYYMM/
daily/journal/YYYY/YYYYMM/
```

- New material normally begins in `daily/`.
- Reuse an existing file when the same item or day is already present.
- Never create `v2`, `final`, or similar duplicate filenames for the same record.
- Use only repository-relative paths in files and responses.

## Skills

Use the matching workflow in `.agents/skills/`:

- `capture-daily-inputs` for ideas, media, conversations, questions, and observations.
- `capture-daily-journal` for lived events, voice transcripts, and personal reflection.
- `review-daily-entries` for looking back across a date range and choosing what to continue.

The user's current instructions override these defaults.
