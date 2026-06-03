# Expanded anonymized supervisor-skill package

This package is a portable, de-identified version of a doctoral supervision and project-memory skill.

It is designed for someone who wants Codex to support a long-term research project across conversations.

## Contents

- `supervisor-skill/`
  - A complete installable skill folder.
  - Includes `SKILL.md`, core routing rules, core protocols, and lightweight schemas.
- `memory-template/`
  - Empty starter memory files.
  - These should be copied into the recipient's own research workspace as `memory/`.
- `setup-guide.md`
  - A first-conversation guide for helping Codex initialize the recipient's project memory.
- `install-prompt-for-recipient.md`
  - A short message the recipient can paste into Codex after installing the skill.
- `anonymization-notes.md`
  - What was removed and what the recipient should personalize.

## What this is

This is a session-first research supervision skill. It helps Codex:

- distinguish explicit supervision sessions from ordinary help;
- read only the project memory needed for the current task;
- keep a compact project map and current-focus file;
- preserve session continuity without turning every chat into an archive;
- stage uncertain ideas before writing them into durable memory;
- support research-question, writing, article, meeting-preparation, and weekly-execution work.

## What this is not

It is not a copy of another person's doctoral project. It does not include:

- personal identifiers;
- local machine paths;
- supervisor names;
- real project title, questions, methods, data, field sites, or cases;
- real session logs;
- real weekly progress records.

## Basic installation

1. Copy `supervisor-skill/` into the local Codex skills directory.
2. Copy `memory-template/` into the recipient's chosen research workspace and rename it to `memory/`.
3. Open `setup-guide.md`.
4. Start a new Codex thread and paste the prompt from `install-prompt-for-recipient.md`.
5. Let Codex ask the minimal missing questions and fill the memory files with the recipient's own project information.

## Recommended first use

Do not fully populate memory in one pass. Start with:

1. project role and degree context;
2. working topic or title;
3. current main question or uncertainty;
4. current stage;
5. immediate priority;
6. any boundaries or risks Codex must respect.

Use `unknown`, `provisional`, and `to_confirm` rather than inventing details.
