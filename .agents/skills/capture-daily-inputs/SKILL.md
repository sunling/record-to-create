---
name: capture-daily-inputs
description: Capture a rough idea, quote, observation, question, or reaction to a book, podcast, video, article, conversation, or everyday experience as a lightly organized Markdown note under daily/inputs. Use when the user says “capture this,” “save this thought,” “add this to my inputs,” or shares material they want to remember without yet turning it into a finished output.
---

# Capture Daily Inputs

## Goal

Preserve a real moment of attention before pressure to categorize, explain, or publish causes it to disappear.

This skill captures and lightly organizes an input. It does not automatically turn the material into an article, project, task list, or mature conclusion.

## Storage

Write to:

```text
daily/inputs/{YYYY}/{YYYYMM}/{YYYYMMDD}-{source}-{keywords}.md
```

Examples:

```text
daily/inputs/2026/202607/20260714-podcast-learning-to-listen.md
daily/inputs/2026/202607/20260714-conversation-asking-better-questions.md
```

Rules:

- Use the user's local date. Read the timezone from `AGENTS.md`; ask if it is unknown and the date could differ.
- Create missing year and month directories safely.
- Use lowercase, hyphenated English for `source` and `keywords` when the note is in English. Follow the user's language when another script is more natural.
- Use `other` when the source type is genuinely unknown. Do not guess the author, show, platform, or URL.
- If the same input already has a file, update it instead of creating `v2`, `final`, or another duplicate.

## Capture principles

### Preserve the real input

Every note should retain:

- what entered the user's attention;
- why it felt worth keeping now;
- the user's original words or a faithful excerpt from them.

Clean obvious transcription errors, broken sentences, and low-information filler. Do not rewrite a rough thought into a polished essay.

### Expand only when the material supports it

Optional sections may include:

- necessary source or concept context;
- a real connection to the user's life, work, relationships, or existing projects;
- a judgment that the input supports, challenges, or changes;
- an unresolved question;
- one possible action or output direction.

Omit sections that would contain invented or generic filler.

### Do not force action or output

An input may simply remain captured. Add a next step only when the user has expressed real interest in one.

Do not create downstream drafts or project files unless the user explicitly asks.

## Markdown formats

Use the smallest format that preserves the material.

### Minimal note

```md
---
title: "{title}"
date: {YYYY-MM-DD}
source: {known source type or other}
tags:
  - {one to three useful tags}
---

## What entered my attention
{The idea, observation, or necessary context}

## Why I want to keep this
{The user's present reaction, question, or connection}

## My original note
> {The user's original words}
```

### Add only when useful

```md
## My connections
{A specific connection grounded in the user's experience}

## Questions I am keeping
- {An unresolved question}

## Possible next direction
- {One real action, output, or “keep observing”}
```

Do not include empty headings or write “none yet” to fill the template.

## Completion response

After writing, briefly report:

1. the relative file path;
2. the central reason this input was kept;
3. any important source detail or interpretation that remains unconfirmed.

Do not repeat the full note unless the user asks to preview it.
