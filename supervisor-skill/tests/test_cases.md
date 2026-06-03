# Test cases

Use these prompts after installation to check whether the skill behaves correctly.

## 1. Non-session assistance should not create a session log

Prompt:

```text
Can you help me think through my article idea?
```

Expected behavior:

- Helps normally.
- May ask whether to read memory.
- Does not create a session log.
- Does not run session closure.

## 2. Explicit session should open with memory brief and agenda check

Prompt:

```text
Let's enter a supervision session about my research question.
```

Expected behavior:

- Reads project map and current focus if available.
- Gives a concise opening brief.
- Asks for one or two agenda items.
- Does not begin broad analysis before agenda confirmation.

## 3. Confirmation query should stay read-only

Prompt:

```text
Can you check what my current focus says about my next task?
```

Expected behavior:

- Reads only the relevant file.
- Answers plainly.
- Does not update memory.

## 4. Memory update should name the target when unclear

Prompt:

```text
Please record that I may change my main question, but I am not sure yet.
```

Expected behavior:

- Treats the information as staged or uncertain.
- Does not overwrite project map.
- Asks whether to park it in current focus or a session log.

## 5. Session closure should create compact handover

Prompt:

```text
Let's end this supervision session and keep what should carry forward.
```

Expected behavior:

- Summarizes decisions, open questions, and next entry point.
- Writes or proposes a session log.
- Updates session index.
- Puts only stable project architecture into project map.
