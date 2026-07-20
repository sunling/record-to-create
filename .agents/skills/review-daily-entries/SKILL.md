---
name: review-daily-entries
description: Review daily inputs and only the journal context needed for a specified period, identify recurring questions, tensions, connections, actions, and changes in judgment, then recommend one to three grounded directions for continued observation, expression, experimentation, or direct action. Use when the user asks to review the past week or month, find what keeps returning, connect recent notes, or decide what may be worth creating next.
---

# Review Daily Entries

## Goal

Help the user return to a period of real records and notice what is repeatedly happening in their attention and life.

A review is not a polished productivity report. It discovers, connects, and helps choose a next direction. It does not automatically create an article, project, or collection of derivative files.

## Read before reviewing

- `README.md` and `AGENTS.md`;
- `daily/inputs/` files within the requested date range;
- only the `daily/journal/` files needed to understand lived context, actions, or changes;
- only other files the user explicitly identifies as relevant.

Do not scan the entire repository merely to appear comprehensive.

## Date range

- Follow explicit start and end dates exactly.
- “Last 7 days” includes today in the user's timezone and the previous six local dates.
- If no period is given, default to the last seven days.
- Check adjacent year or month directories when the period crosses a boundary.
- Prefer dates in filenames, frontmatter, and content over Git modification time.

## Review principles

### Use records as evidence

Ground each meaningful observation in a specific date and relative path. Do not infer a stable personality, diagnosis, or life trajectory from a few short-term notes.

### Find recurrence; do not manufacture a theme

Look for:

- questions, phrases, scenes, emotions, or situations that recur;
- real connections between inputs and lived experience;
- tensions, contradictions, or changes in judgment;
- plans that became actions and plans that remained ideas;
- material that may have enough energy and evidence to become an output.

Keep only connections supported by the records. A review does not need one grand narrative.

### Distinguish possible directions

For each important thread, decide which direction currently fits best:

1. **Keep capturing** — it is still unfolding and does not need an output.
2. **Keep observing** — it recurs but needs more lived evidence, a counterexample, or another attempt.
3. **Create or share** — it is ready for a real form such as a note, essay, conversation, presentation, prototype, workshop, or contribution.
4. **Act directly** — the best next step is a choice, conversation, or experiment rather than another file.

Do not push every thread toward public output.

## Default response

Respond in the conversation. Do not write a review file unless the user asks.

```md
## Review range
- Period:
- Main sources:
- Additional context:

## What kept returning
### 1. {question or direction}
- Evidence: {dates and relative paths}
- What is happening:
- What is still missing:

## Connections and changes
- {Evidence-backed connection, tension, or change}

## Possible directions
- Keep capturing:
- Keep observing:
- Create or share:
- Act directly:

## The 1–3 directions most worth continuing
1. {Direction and why}
```

Use a shorter response when the source material is limited. Do not invent content to fill every heading.

## Moving toward output

When a thread appears ready, recommend the smallest honest form that can meet reality:

- one scene before a full essay;
- a short conversation before a workshop;
- a small prototype before a large project;
- a private reflection before public publishing;
- a direct action when writing would only postpone the decision.

Name the relevant source paths and what remains uncertain. Create the output only after the user chooses its form or explicitly asks for a draft.

## Privacy and factual boundaries

- Use private journal, health, work, relationship, and third-party details only to help the user understand their own experience.
- Before recommending public expression, separately flag details that require removal, anonymization, or permission.
- Do not describe a temporary feeling as a permanent trait.
- Do not describe a plan as completed action.
- Do not present an AI inference as the user's confirmed judgment.

## Completion response

Briefly state:

1. the reviewed date range and main materials;
2. the few recurring questions or changes found;
3. the one to three strongest next directions;
4. what still needs the user's confirmation;
5. that no new file was created unless one was requested.
