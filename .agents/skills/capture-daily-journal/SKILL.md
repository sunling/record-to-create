---
name: capture-daily-journal
description: Lightly organize rough notes or a voice transcript into a faithful personal journal entry and create or append the matching dated file under daily/journal. Use when the user says “journal this,” “add this to today’s journal,” “record what happened today,” or asks to clean up a diary transcript while preserving their voice, facts, emotions, uncertainty, and unfinished thoughts.
---

# Capture Daily Journal

## Goal

Turn rough speech or fragments into a natural, readable record that lets the user re-enter the day later.

The default editing level is **clean, not rewrite**. Preserve the user's wording, emotional intensity, hesitation, contradictions, and lack of resolution. Increase the level of editing only when the user explicitly asks.

## Non-negotiable rules

- Never invent an event, time, place, person, quote, opinion, feeling, motive, cause, or conclusion.
- Do not intensify emotion or add a positive lesson.
- Do not make unfinished thinking sound resolved.
- Treat the journal as private material. Do not pre-polish it for public sharing.
- When a name or proper noun is uncertain, preserve the transcription and flag it instead of guessing.

## Light cleanup

- Repair obvious sentence breaks and transcription noise.
- Remove filler words that carry no meaning, while retaining repetition that expresses uncertainty, emphasis, or emotion.
- Correct obvious typos only when context is strong enough.
- Keep meaningful code-switching and proper nouns in their original language.
- Match the language used by the user.

## Entry format

Each newly written or appended fragment begins with a short, factual level-three heading:

```md
### {brief factual heading}

{Lightly organized journal prose in natural paragraphs. Use a list only when the original material is genuinely a list.}
```

Do not add summaries, lessons, tags, or execution notes to the journal file unless the user explicitly requests them.

## Storage and append behavior

```text
daily/journal/{YYYY}/{YYYYMM}/{YYYYMMDD}-{keywords}.md
```

Example:

```text
daily/journal/2026/202607/20260714-a-slower-walk.md
```

Date rules:

- Use the user's local date from `AGENTS.md`, not UTC.
- Resolve explicit dates and relative dates such as “yesterday” in that timezone.
- If the timezone is unknown and could change the target date, ask once before writing.

File rules:

1. Create the year and month directories if needed.
2. Search for an existing file beginning with the target `YYYYMMDD-` prefix.
3. If none exists, create one using brief keywords from the day's first fragment.
4. If one exists, read it fully and append only the newly supplied fragment, separated by a blank line.
5. Do not rename the file when later fragments introduce different topics.
6. If multiple files exist for the same date, do not guess or create a third. Use the file the user explicitly identifies; otherwise ask.
7. Never revise, merge, reorder, or delete earlier fragments while appending unless the user explicitly asks.

## Quality check

Before writing, confirm:

- meaningful uncertainty and repetition were preserved;
- the voice and emotional intensity still belong to the user;
- no motive, causal explanation, or lesson was added;
- paragraphs follow the natural movement of the account;
- only journal prose will be written to the file.

## Completion response

After writing, briefly state whether the entry was created or appended and give the relative file path. Mention any uncertain transcription that needs confirmation.

Do not repeat the full private entry unless the user asks for a preview.
