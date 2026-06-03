# Supervisor Skill

A Codex skill for turning LLM conversations into structured research supervision sessions and durable project memory.

`supervisor-skill` is designed for PhD research, long-term academic projects, and research-based writing where ideas develop across many conversations rather than in one sitting.

## Why This Exists

We now talk to LLMs constantly.

These conversations can be genuinely useful: they help us think through research questions, reframe problems, notice tensions, plan writing, prepare meetings, and make decisions. But many of those useful moments remain trapped inside one-off chats.

A conversation ends.
The insight is not recorded.
The decision is not carried forward.
The next conversation starts by rebuilding context again.

This becomes especially costly in doctoral research and long-term research projects. A PhD is not a single task. It is a changing intellectual process: research questions shift, theoretical commitments move, materials become clearer, writing plans branch, supervisor feedback accumulates, and temporary ideas sometimes become durable commitments.

Ordinary chat is often too loose for this kind of continuity.

That is why this skill is built around the idea of a `supervision session`.

## What Is a Supervision Session?

A `supervision session` is a bounded research conversation with memory.

It is different from ordinary chat.

Ordinary chat can stay lightweight, exploratory, and informal. You can ask a quick question, test an idea, or get help with a paragraph without turning it into project memory.

A supervision session is more intentional. It works more like a small research meeting:

1. Codex reads the relevant project memory.
2. It gives a brief sense of the current project state.
3. You confirm one or two core agenda items.
4. You work through the issue together.
5. Important decisions, tensions, next steps, and unresolved questions can be written back into memory.

The point is not to make every conversation formal. The point is to create a clear mode for the conversations that should matter later.

## Core Principle

The skill follows one simple rule:

> classify first, read minimally, write only through the write gate.

Before doing memory work, Codex should classify the conversation:

- Is this ordinary help?
- Is this an explicit supervision session?
- Is this a memory check?
- Is this a memory update?
- Is this work on the skill or memory system itself?

Only after that should it decide what to read, what to ignore, and whether anything should be written.

## What It Helps With

`supervisor-skill` can support:

- research question development;
- thesis or dissertation planning;
- article and publication planning;
- supervision meeting preparation;
- writing-as-research feedback;
- weekly execution review;
- project continuity across conversations;
- memory checks and memory updates;
- session handover between research conversations.

## Project Memory

The skill works with a plain-file memory system, usually stored in a `memory/` folder.

A typical memory folder can include:

```text
memory/
  project_map.yaml
  current_focus.yaml
  current_week.yaml
  session_index.yaml
  log_index.yaml
  user_profile.yaml
  session_feedback_log.yaml
  skill_boundary_candidates.yaml

  sessions/
  logs/
  articles/
```

The main files are:

- `project_map.yaml`
  Stable overview of the research project: topic, questions, theory, methods, materials, stage, risks, and durable decisions.

- `current_focus.yaml`
  What is active right now: current problem, live assumptions, next decisions, immediate priorities.

- `current_week.yaml`
  Weekly execution: commitments, completed work, blockers, carry-forward items, and next-week candidates.

- `sessions/`
  Handover notes from explicit supervision sessions.

- `logs/`
  Topical or stream-specific research notes.

- `articles/`
  Article cards for publication projects connected to the larger research.

## Write Gate

Not every thought should become durable memory.

The skill separates:

- **Read-only checks**
  Codex answers from memory but does not write.

- **Staged ideas**
  Provisional thoughts, possible framings, and unfinished interpretations stay temporary.

- **Confirmed factual progress**
  Completed tasks, meeting outcomes, accepted commitments, and concrete next actions can be written to the smallest relevant file.

- **Stable architecture**
  Major changes to research questions, project direction, methodology, or article-thesis relationship should only update the project map when the user treats them as stable.

- **Unclear updates**
  Codex should name the proposed target file and ask before writing.

This matters because research thinking is often unstable before it becomes useful. The skill should preserve that instability instead of prematurely flattening it into "final" memory.

## Example Prompts

Ordinary help:

```text
Can you help me think through this paragraph?
```

Start a supervision session:

```text
Let's enter a supervision session about my research question.
```

Prepare a meeting:

```text
Help me prepare for my supervision meeting tomorrow.
```

Check memory:

```text
Can you check what my current focus says about my next task?
```

Update memory:

```text
Please record this meeting outcome in the smallest appropriate memory file.
```

Weekly review:

```text
Can you review what I completed this week and help me carry forward only what still matters?
```

Close a session:

```text
Let's end this supervision session and keep what should carry forward.
```

## Design Principles

### 1. Not every chat is a session

The skill should not over-formalize ordinary conversations. A supervision session begins only when the user explicitly asks for one.

### 2. Memory should be useful, not maximal

The goal is not to remember everything. The goal is to preserve what helps the project continue.

### 3. Research ideas need staging

Early ideas should not be treated as final decisions. The memory system needs room for uncertainty, parked ideas, reversals, and open questions.

### 4. The user owns the project

Codex can suggest, organize, diagnose, and remember. It should not silently replace the user's judgement or turn its own suggestions into project facts.

### 5. Project continuity should be inspectable

Memory lives in ordinary YAML and Markdown files so the user can read, edit, version, move, or delete it.

## Who This Is For

This skill may be useful for:

- PhD students;
- thesis and dissertation writers;
- independent researchers;
- academic writers managing several papers;
- people using LLMs as long-term thinking partners;
- anyone who needs a clearer boundary between chat, notes, decisions, and project memory.
