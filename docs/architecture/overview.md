# Architecture Overview

This page describes Plato at a public architecture level.

Plato is the product surface. TaskWeavn is the local runtime behind it.

![Plato architecture overview](../../assets/images/plato-architecture-overview.svg)

## Architecture Shape

Plato separates intent, execution, and trust into distinct areas.

```text
User intent
  -> Authoring Domain
  -> Publishing boundary
  -> Execution Domain
  -> Main Page and Audit projections
```

## Authoring Domain

Authoring turns fuzzy user intent into a reviewable task structure.

Its job is to keep planning separate from execution:

- capture the user's goal;
- ask for clarification when needed;
- draft a TaskTree;
- let the user review and adjust tasks;
- publish only reviewed work into execution.

## Execution Domain

Execution starts after tasks are published.

The runtime executes task-scoped work, records progress, and produces result
and file-change facts that the UI can project back to the user.

For the early public release, Plato should be understood as a local task-first
workbench, not a broad multi-agent orchestration platform.

## UI Projection

The UI consumes product projections rather than raw runtime internals.

| Surface | Purpose |
|---|---|
| Main Page | Control plane for work, progress, confirmations, results, and file summaries. |
| Audit Page | Trust plane for evidence, traceability, and debugging. |

## Context Governance

LLM calls are stateless, but Plato work sessions are stateful.

![Plato context governance](../../assets/images/plato-context-governance.svg)

The runtime assembles task, workspace, event, permission, and recent result
facts into bounded context before model calls. This keeps execution tied to the
visible task and audit record instead of hidden chat memory.

## Release Boundary

Architecture docs may describe direction beyond the current release. Public
release claims should always be checked against [Release status](../product/release-status.md).
