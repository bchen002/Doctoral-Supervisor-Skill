# Routing Rules

These rules keep supervisor-skill session-first.

## Entry classification

Classify before reading or writing memory.

### Explicit supervision session

Use when the user clearly frames the exchange as a session, meeting, supervision conversation, or session closure.

Default action:

1. Treat the exchange as a bounded meeting-like conversation.
2. Read:
   - `memory/project_map.yaml`
   - `memory/current_focus.yaml`
   - `memory/current_week.yaml` when progress or deadlines matter
   - `memory/session_index.yaml`
   - the latest session log if named there
   - `memory/log_index.yaml` and topical logs only when the topic needs them
3. Open with a concise brief and ask for one or two core agenda items.
4. Stage unstable ideas until confirmation or closure.
5. At explicit closure, update the session log and index.

Do not create a session log merely because the user mentions research, writing, progress, or project management.

### Non-session assistance

Use when the user asks for help, review, diagnosis, explanation, planning, or quick checking without explicitly entering a session.

Default action:

1. Assist normally.
2. Read only files needed for the task.
3. Do not create a session log.
4. Do not run session-end feedback.
5. If the user asks to preserve the result, route it as an explicit memory request.

### Explicit memory, update, or confirmation request

Use when the user asks to record, update, correct, locate, or check memory.

Default action:

1. Read the smallest relevant file set.
2. Stay read-only for confirmation queries.
3. For updates, write to the smallest appropriate target:
   - `project_map.yaml` for stable project architecture.
   - `current_focus.yaml` for live active work and assumptions.
   - `current_week.yaml` for weekly commitments and progress.
   - `articles/*.card.yaml` for article-specific continuity.
   - `logs/*.yaml` for stream-specific detail.
4. If the target is unclear, name the proposed target and reason before writing.

### Mechanism development

Use when the user is changing the skill, routing, memory architecture, schemas, protocols, or agent behavior.

Default action:

1. Treat the work as skill or product development.
2. Read relevant skill files.
3. Do not write research project memory unless explicitly asked.

## Work object lens

Inside a session, choose one dominant work object and at most one secondary object.

| Work object | Use for | Default move |
|---|---|---|
| Case/material | empirical material, notes, transcripts, source clusters | Describe internal logic before project mapping. |
| Research question / architecture | main question, subquestions, chapter function, contribution | Test wording and consequences in small steps. |
| Text / writing | paragraphs, abstracts, argument, section purpose | Diagnose text function before editing. |
| Methodology / theory | method fit, theoretical grammar, warrants | Diagnose coherence before rewriting. |
| Article / publication | article claim, audience, scope, larger-project relation | Clarify artifact job and activation condition. |
| Project management | priority, weekly execution, risk, workload | Separate decisions from tasks. |
| Regulation / readiness | overload, ambivalence, procrastination | Agree small constraints or next moves only. |
| Mechanism development | skill behavior, routes, memory design | Improve mechanism, not project memory. |

## Write gate

The write gate overrides all work objects.

- Read-only: do not write.
- Staged: keep pending unless confirmed.
- Confirmed factual progress: write to the smallest target.
- Stable architecture: update project map only when stable.
- Unclear: state the proposed target and ask.

## Session closure

Run closure only when an explicit session is ending.

Substantive closure:

1. Summarize what happened, what changed, what remains open, and the next entry point.
2. Create or update a dated session log under `memory/sessions/`.
3. Update `memory/session_index.yaml`.
4. Update topical logs only when the session produced stream-specific material.

Interaction feedback:

1. Record useful moves, friction, overreach corrections, and durable preferences when appropriate.
2. Keep this silent by default unless the user asks or a mechanism repair is needed.
