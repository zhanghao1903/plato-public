# Task-First Workflow

Plato is task-first rather than chat-first.

The user still starts with natural language, but the product turns that input
into a structured path the user can inspect and control.

![Plato product flow](../../assets/images/plato-product-flow.svg)

## 1. Express Intent

The user describes what they want in ordinary language.

Plato treats this as the beginning of a work session, not as permission to
immediately change the workspace.

## 2. Draft The TaskTree

The system turns the user's goal into a draft task structure.

The draft exists so the user can answer:

- What does Plato think I asked for?
- Which tasks will happen?
- Which tasks need more context?
- Which tasks may affect files or results?

## 3. Review And Confirm

The user can inspect task details before execution.

High-impact actions should be confirmed near the task they affect. This keeps
confirmation connected to the work instead of hiding it in a generic dialog.

## 4. Execute Locally

Reviewed tasks are published into executable work.

The early public release uses a local runtime and bundled Python sidecar
candidate. Execution remains local to the user's machine and release status
limits should be read from [Release status](release-status.md).

## 5. Inspect Outcome

When work completes, Plato should make the outcome inspectable:

- user-readable result summary;
- changed-file summary when file work occurred;
- task status and failure/retry context;
- audit entry for trust and debugging.

## 6. Continue Or Accept

The user can accept the result, inspect evidence, or continue with another
round of work.

This loop is the product center:

```text
intent -> task structure -> review -> execution -> outcome -> next step
```
