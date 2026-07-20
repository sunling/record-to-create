# Record to Create

**Capture what enters your life. Notice what keeps returning. Turn it into something real.**

Most ideas do not arrive as polished thoughts. They begin as a sentence from a book, a moment in a conversation, a question on a walk, or something you notice about your own day.

Record to Create is a small, AI-assisted recording system that helps you keep those moments without demanding that you immediately organize, explain, or publish them.

```text
daily inputs + daily journal
            ↓
       regular review
            ↓
 writing, conversation, projects, experiments, or action
```

This repository is an English, reusable version of the core daily loop in [Sunling OS](https://github.com/sunling/sunling-os). It intentionally includes only three skills:

- [`capture-daily-inputs`](.agents/skills/capture-daily-inputs/SKILL.md) — save ideas and observations from books, podcasts, conversations, and everyday life.
- [`capture-daily-journal`](.agents/skills/capture-daily-journal/SKILL.md) — turn rough notes or voice transcripts into a readable, faithful journal entry.
- [`review-daily-entries`](.agents/skills/review-daily-entries/SKILL.md) — revisit a period of daily records, notice recurring questions, and choose a small next direction.

## Why this exists

Recording is not the same as collecting information.

A useful record keeps three things close together:

1. What entered your attention.
2. Why it mattered to you at that moment.
3. What it may change in how you understand, express, or act.

Not every note needs to become an output. But when you return to your records, the ideas that keep showing up become easier to recognize—and easier to turn into a piece of writing, a meaningful conversation, a project, an experiment, or a decision.

## Quick start

1. Fork or copy this repository into a **private repository** for your personal records.
2. Open it in an AI coding workspace or editor that can read and write repository files.
3. Tell the assistant your timezone, or replace `YOUR_TIMEZONE` in [`AGENTS.md`](AGENTS.md).
4. Start with one of these prompts:

```text
Capture this daily input: [paste a thought, quote, observation, or transcript]

Add this to today's journal: [paste rough notes or a voice transcript]

Review my daily entries from the last 7 days. What keeps returning, and what may be worth creating or doing next?
```

If your assistant does not automatically discover repository skills, ask it to follow the relevant `SKILL.md` file in `.agents/skills/`.

## Repository structure

```text
.
├── .agents/skills/
│   ├── capture-daily-inputs/
│   ├── capture-daily-journal/
│   └── review-daily-entries/
├── daily/
│   ├── inputs/
│   └── journal/
├── examples/
├── AGENTS.md
└── README.md
```

### Daily inputs

`daily/inputs/` holds material that entered your attention: reading, podcasts, videos, conversations, observations, questions, and sudden thoughts.

```text
daily/inputs/YYYY/YYYYMM/YYYYMMDD-source-keywords.md
```

### Daily journal

`daily/journal/` holds what happened in your life: scenes, choices, feelings, body states, relationships, work, and ordinary details.

```text
daily/journal/YYYY/YYYYMM/YYYYMMDD-keywords.md
```

The distinction does not need to be perfect. If you are unsure, choose the folder that makes it easier to record the moment now.

## The review loop

A review is not a productivity report and does not need to summarize everything. It should help you notice:

- questions, words, feelings, or situations that recur;
- connections between what you consume and how you are living;
- changes in your judgment or behavior;
- ideas that have enough energy to become an output;
- moments when the best next step is action, not another note.

The default review period is seven days. End with no more than one to three directions. Small, honest continuations are more useful than a long list of ambitions.

## Privacy first

The starter repository is public, but your personal records probably should not be.

This repository's `.gitignore` excludes Markdown files created under `daily/inputs/` and `daily/journal/` by default. For actual use, we recommend a private repository. If you intentionally want to version your daily records in that private repository, remove the corresponding rules from `.gitignore`.

Before publishing anything derived from a journal, review names, health information, workplace details, relationship details, and stories involving other people.

## Principles

- Capture before categorizing.
- Preserve your actual words and uncertainty.
- Never invent missing facts, feelings, or conclusions.
- Review for patterns, not for a perfect summary.
- Let output take many forms—not only polished writing.
- Keep private material private.

## License

[MIT](LICENSE)
