# Plato Product Overview

Plato is a task-first intelligent workbench for local AI-assisted work.

The product is built around one belief: users should see what the system thinks
the work is before the system acts.

## Product Thesis

Plato turns unclear intent into structured, reviewable work:

```text
Natural language goal
  -> TaskTree
  -> TaskNode review
  -> Confirmed execution
  -> Result and evidence
```

The main object is not a chat transcript, an agent, or a file tree. The main
object is the task.

A task is a visible work contract:

- before execution, it is a plan the user can inspect;
- during execution, it is delegated work under user supervision;
- after execution, it anchors the result, file changes, and audit trail.

## Product Layers

| Layer | Meaning |
|---|---|
| Plato | User-facing product and release identity. |
| TaskWeavn | Local task-agent runtime behind Plato. |
| Workflow | User-facing mode for a session of work. |
| Session | Collaboration boundary for one active work context. |
| TaskTree | Structured representation of the user's goal. |
| TaskNode | Smallest unit of review, confirmation, execution, and evidence. |
| Result | User-readable output of completed work. |
| Audit | Trust surface for tracing what happened and why. |

## What Plato Prioritizes

Plato prioritizes:

- legibility before automation;
- review before consequential execution;
- task-scoped confirmation instead of context-free popups;
- visible result and file-change summaries;
- audit evidence for trust and debugging;
- local-first execution for early releases.

Plato does not position the `0.1.0` release as a broad autonomous worker, a
multi-agent marketplace, or a source-code distribution.

## Current Release Status

The current public release is `0.1.0`, an unsigned and non-notarized macOS
Apple Silicon local release candidate.

For exact release metadata, see [Release status](release-status.md).

## Public Screenshots

Current public-safe screenshots:

- [Main Page](../../assets/images/plato-main-page.png)
- [Audit Page](../../assets/images/plato-audit-page.png)
- [Workspace Inspection](../../assets/images/plato-workspace-inspection.png)
