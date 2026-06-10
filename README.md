# Plato

Plato is a task-first intelligent workbench.

It helps users start from an unclear goal, shape that goal into reviewable
work, control execution, and inspect evidence afterward.

![Plato task-first workbench](assets/images/plato-hero.svg)

## What Plato Is

Most AI tools make the conversation the main object. Plato makes the task the
main object, and organizes the product around three planes:

- Inspiration Plane: help the user discover what AI can do, learn how to use
  AI through better prompts and workflows, clarify missing context, and shape
  fuzzy intent into work that can be planned.
- Control Plane: show the plan, task state, confirmations, running work, and
  result actions in one action-oriented surface.
- Trust Plane: keep outcomes, file changes, audit evidence, and diagnostics
  inspectable after work happens.

```text
User intent
  -> Clarification when needed
  -> Draft TaskTree
  -> Review and confirmation
  -> Local execution
  -> Result, file changes, and audit evidence
```

The three planes exist because intelligent work fails in three different ways:
the user may not know how AI can help or how to ask, the user can lose control
during execution, or the result can be hard to trust afterward. Plato treats
those as separate product responsibilities instead of hiding all of them in
chat.

## Current Public Release

Version: `0.1.0`

Platform: macOS Apple Silicon (`macos-arm64`)

Download:

- [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg)

Integrity:

```text
34bc9a24dbf29c8ba5ebdeb1d92a4428d55e791562596e4303734b493fdfb212  Plato-0.1.0-macos-arm64.dmg
```

Release metadata:

- [manifest.json](releases/0.1.0/manifest.json)
- [SHA256SUMS](releases/0.1.0/SHA256SUMS)

Important status notes:

- This is an unsigned and non-notarized local release candidate.
- macOS may require opening it from Finder with the contextual Open action.
- The package includes a bundled Python sidecar runtime candidate.
- This public repository currently hosts public release metadata and product
  documentation. It is not a source-code mirror.

See [macOS local release usage](docs/usage/macos-local-release.md).

## Product Planes

![Plato three product planes](assets/images/plato-three-planes.svg)

| Plane | User question | Product role |
|---|---|---|
| Inspiration Plane | What can AI help me do, how should I use it, and what does Plato understand? | Helps users discover AI use cases, choose better prompt/workflow paths, and turn fuzzy goals into clarified, draftable work. |
| Control Plane | What work will happen, what is running, and what needs me? | Keeps plan, status, confirmation, and result actions visible. |
| Trust Plane | What happened, why, and what evidence exists? | Makes results, file changes, and audit evidence inspectable. |

The next product emphasis is the Inspiration Plane. This is where Plato should
help users understand what AI can do for them, how to shape prompts and
workflows, what context is missing, and whether a goal is ready to become a
task structure. This is also the least developed part of the current public
product story.

## Task-First Loop

![Plato product flow](assets/images/plato-product-flow.svg)

Plato is designed around a simple loop:

1. State a goal in natural language.
2. Clarify missing context before the goal becomes executable work.
3. Review the generated task structure before meaningful work starts.
4. Confirm high-impact actions in context.
5. Track progress through task states.
6. Inspect the result, changed files, and audit trail.

Read more:

- [Product overview](docs/product/overview.md)
- [Task-first workflow](docs/product/task-first-workflow.md)
- [Release status](docs/product/release-status.md)

## Product Screens

The following screenshots use public-safe sample data captured from the local
Plato mock and sidecar flows.

![Plato Main Page](assets/images/plato-main-page.png)

The Main Page is the control plane for reviewing the plan, publishing tasks,
watching state, and opening audit.

![Plato Audit Page](assets/images/plato-audit-page.png)

The Audit Page is the read-only trust plane for evidence and traceability.

![Plato Workspace Inspection](assets/images/plato-workspace-inspection.png)

Workspace inspection shows repository status and file-level inspection links
using renderer-safe path labels. This screenshot is a public-safe local sidecar
capture; check [Release status](docs/product/release-status.md) before treating
this surface as available in a specific public release.

## Architecture Preview

![Plato architecture overview](assets/images/plato-architecture-overview.svg)

Plato separates the work into four public concepts:

- Authoring: turn intent into a draft task structure.
- Publishing: move reviewed tasks into executable work.
- Execution: run tasks in a local workspace.
- Trust projection: show progress, results, file changes, and audit evidence.

Read more:

- [Architecture overview](docs/architecture/overview.md)
- [Trust and audit](docs/architecture/trust-and-audit.md)

## Public Visual Status

This repository includes public-safe explanatory diagrams and sanitized product
screenshots. Future releases should refresh screenshots when release status
changes and add a repository/social preview image.
