# First-conversation setup guide

Use this guide before the recipient begins using `supervisor-skill` for real supervision sessions.

## Goal

Create a small, accurate project memory folder that Codex can use later. The first setup should not pretend to know the whole project.

## Suggested first message

Paste this into Codex after installing the skill:

```text
I have installed a portable supervisor-skill and copied its memory-template folder into my research workspace as memory/.

Please help me initialize the memory files for my own project.

Do not invent missing details. Ask only the minimum questions needed to create project_map.yaml and current_focus.yaml. Use unknown, provisional, or to_confirm where needed. Show me the proposed memory content before writing it.
```

## Minimum questions Codex should ask

Codex should ask no more than these questions at first:

1. What is your role, degree or project type, and current stage?
2. What is the working topic or title?
3. What is the current main question, problem, or research uncertainty?
4. What materials, methods, field, archive, data, or cases matter most right now?
5. What is your current priority for the next 1 to 2 weeks?
6. Are there any boundaries Codex must respect, such as not writing memory without confirmation or not treating ordinary help as a supervision session?

## First files to create or update

Start with only:

- `memory/project_map.yaml`
- `memory/current_focus.yaml`
- `memory/session_index.yaml`
- `memory/log_index.yaml`

Use `memory/current_week.yaml` only if the user wants weekly execution tracking.

## Setup principles

- Ask first, then propose memory content.
- Keep the first memory minimal.
- Mark uncertain fields clearly.
- Do not add private names unless the recipient explicitly wants them in their own memory.
- Do not create a session log during setup unless the recipient explicitly says the setup is also a supervision session.
- Do not import another person's examples as project facts.

## Good first memory shape

`project_map.yaml` should answer:

- What is this project?
- What is the current research question or uncertainty?
- What theories, methods, materials, or cases define the project?
- What stage is it in?
- What should Codex preserve across conversations?

`current_focus.yaml` should answer:

- What is live right now?
- What decision, draft, reading, meeting, or task is next?
- What assumptions are provisional?
- What should be checked before planning?

## After setup

Once the project map and current focus exist, start using the skill in two different ways:

- Ordinary help: "Can you help me think through this paragraph?"
- Explicit session: "Let's enter a supervision session about my research question."

The skill should only use the richer session workflow when the session frame is explicit.
