# Project Memory Protocol

Use this protocol when project memory may matter.

## Purpose

Maintain a long-term project memory system without forcing every detail into one file.

Core files:

```text
memory/project_map.yaml
memory/current_focus.yaml
memory/current_week.yaml
memory/session_index.yaml
memory/sessions/*.yaml
memory/log_index.yaml
memory/logs/*.yaml
memory/articles/*.card.yaml
memory/user_profile.yaml
memory/session_feedback_log.yaml
memory/skill_boundary_candidates.yaml
```

## Memory roles

- `project_map.yaml`: stable project orientation, research problem, question architecture, methods, materials, stage, durable risks.
- `current_focus.yaml`: current active work, live assumptions, immediate decisions, next files or tasks.
- `current_week.yaml`: weekly commitments, completed work, blockers, carry-forward, next candidates.
- `session_index.yaml`: where the latest supervision session lives.
- `sessions/*.yaml`: compact handover logs for explicit sessions.
- `log_index.yaml`: routes topical streams to logs.
- `logs/*.yaml`: stream-specific continuity.
- `articles/*.card.yaml`: article-specific claim, scope, relation to larger project, and next writing task.
- `user_profile.yaml`: stable collaboration preferences.
- `session_feedback_log.yaml`: interaction-level feedback and candidate protocol improvements.

## Reading sequence

For explicit sessions:

1. Read `project_map.yaml`.
2. Read `current_focus.yaml`.
3. Read `current_week.yaml` if progress, timing, or priority matters.
4. Read `session_index.yaml`.
5. Read the latest session log if available.
6. Give a concise opening brief.
7. Ask for one or two agenda items.
8. Read topical logs only after the agenda shows they are needed.

For non-session assistance:

- read only the smallest file set needed;
- do not create session logs;
- do not run session feedback.

For confirmation queries:

- answer from the smallest file set;
- do not write.

For memory updates:

- read enough to choose the target;
- preserve prior history;
- write only the confirmed information;
- record a short `update_history` entry when the file supports it.

## Write timing

Write factual, low-risk progress immediately only when continuity benefits from it and the user has clearly accepted the fact.

Stage evolving conceptual material when it concerns:

- research questions;
- theoretical framing;
- methodology fit;
- chapter function;
- article claim;
- material placement;
- project architecture.

Move staged material into durable memory only after user confirmation or session closure.

## Stability split

Use this split for research-question and architecture work:

- `project_map.yaml`: stable architecture.
- `current_focus.yaml`: current question work and live assumptions.
- `sessions/*.yaml`: provisional or unresolved session movement.
- `logs/*.yaml`: stream-specific detail.

## What counts as project-level information

- topic or working title;
- research question or problem;
- theory or methodology;
- materials, data, cases, archive, or field;
- chapter or article architecture;
- supervisor or collaborator feedback;
- milestone, deadline, priority, or risk;
- publication plan;
- active topical stream;
- live assumptions, superseded ideas, and parked directions.

## Do not

- fill missing fields from examples;
- overwrite stable fields without preserving history;
- treat every chat as a session;
- create a second memory system without the user's consent;
- store private names unless the user wants them stored.
