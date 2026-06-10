# Task-First Workflow

Plato is task-first rather than chat-first.

The user still starts with natural language, but the product turns that input
into a structured path the user can inspect and control.

![Plato product flow](../../assets/images/plato-product-flow.svg)

The workflow crosses three product planes:

- Inspiration Plane: help the user discover what AI can do, shape a useful
  prompt/workflow, and clarify missing context.
- Control Plane: review, confirm, and run visible task work.
- Trust Plane: inspect the result and evidence after execution.

## 1. Express Intent

The user describes what they want in ordinary language.

Plato treats this as the beginning of a work session, not as permission to
immediately change the workspace.

The user may also be unsure what to ask for. The Inspiration Plane should make
AI use more approachable by showing possible work patterns and the kind of
context that will improve the result.

Plane: Inspiration.

## 2. Clarify And Shape

If the goal is ambiguous, incomplete, risky, or missing constraints, Plato
should ask focused questions before planning.

This step is the core of the Inspiration Plane. It is where Plato helps the
user understand how AI can help, learns what the user actually needs, and makes
assumptions visible early.

This planning question pattern is Authoring ASK. It appears before a TaskTree
exists and is answered in the main work area.

## 3. Draft The TaskTree

The system turns the clarified goal into a draft task structure.

The draft exists so the user can answer:

- What does Plato think I asked for?
- Which tasks will happen?
- Which tasks need more context?
- Which tasks may affect files or results?

Plane: Inspiration moving into Control.

## 4. Review And Confirm

The user can inspect task details before execution.

High-impact actions should be confirmed near the task they affect. This keeps
confirmation connected to the work instead of hiding it in a generic dialog.

Plane: Control.

## 5. Execute Locally

Reviewed tasks are published into executable work.

The early public release uses a local runtime and bundled Python sidecar
candidate. Execution remains local to the user's machine and release status
limits should be read from [Release status](release-status.md).

If a running task is missing user-owned information, Plato should create an
Execution ASK and pause that task instead of guessing. The user answers it from
the task detail panel while keeping the TaskTree in view.

Plane: Control.

## 6. Inspect Outcome

When work completes, Plato should make the outcome inspectable:

- user-readable result summary;
- changed-file summary when file work occurred;
- task status and failure/retry context;
- audit entry for trust and debugging.

Plane: Trust.

## 7. Continue Or Accept

The user can accept the result, inspect evidence, or continue with another
round of work.

This loop is the product center:

```text
intent -> clarification -> task structure -> review -> execution -> outcome -> next step
```

The next product emphasis is improving the beginning of this loop. A stronger
Inspiration Plane helps users learn how to work with AI and helps Plato
understand the user earlier, which makes the Control Plane less noisy and the
Trust Plane more meaningful.
