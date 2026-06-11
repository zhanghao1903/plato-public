# Plato FAQ

## What Is Plato?

Plato is a task-first intelligent workbench. You describe a goal, Plato turns
it into a visible plan, you review or guide the tasks, and then you inspect
what happened afterward.

## How Is Plato Different From ChatGPT Or Claude?

Chat products make the conversation the main object. Plato makes the task plan
the main object.

The goal is not only to get an answer. The goal is to make work visible:

- what the system thinks the work is;
- which task is running;
- what needs your input;
- what changed;
- what evidence exists afterward.

## Is Plato Ready For Everyday Non-Technical Users?

Not yet as a polished public product. The current `1.1-beta` build is a local
beta release for early evaluation.

It is designed to show the product direction and working loop, but it still has
rough edges such as unsigned macOS packaging and evolving UI details.

## Why Does macOS Warn Me When Opening The App?

The `1.1-beta` release is unsigned and non-notarized. macOS Gatekeeper may
block a normal double-click launch.

See [macOS local release usage](macos-local-release.md) for the local opening
path.

## Does Plato Modify My Files?

Plato is designed around local workspaces and task-level control. Some
workflows may involve file changes, but the product direction is to show tasks,
ask for confirmation when needed, and make changes inspectable afterward.

For early testing, use a non-sensitive test workspace.

The `1.1-beta` release adds workspace inspection paths for git status,
structured diffs, and file viewing so file-related work is easier to review.

## What Is An ASK?

An ASK appears when Plato needs information that belongs to the user and should
not be guessed.

Examples:

- "Which audience should this content target?"
- "Should this task continue with the default option?"
- "Which file or scope should this task use?"

ASK is different from a confirmation. A confirmation means Plato knows the
action but needs approval. ASK means Plato needs missing information.

## What Is The Audit Page?

The Audit Page is a read-only trust surface. It helps you inspect evidence,
diagnostics, messages, and task facts after work happens.

It is not the main control surface. The Main Page is for controlling work; the
Audit Page is for understanding what happened.

## Where Is Data Stored?

The current public release is local-first. Runtime state, logs, and workspace
data are expected to live on the local machine, depending on the selected
workspace and app configuration.

Because this is an early release candidate, do not put secrets or private
customer data into test sessions unless you have reviewed the product behavior
and local files yourself.

## Does This Repository Contain Source Code?

No. This repository currently hosts public product docs, visual assets, release
metadata, and downloadable release assets. It is not a source-code mirror.

## What Should I Try First?

Start with a low-risk planning task:

- plan a personal website;
- draft a courseware outline;
- turn a research idea into tasks;
- ask Plato to break down a small local project cleanup.

See [Use cases](../product/use-cases.md).

## How Should I Report A Problem?

Use the GitHub issue templates:

- Bug report for reproducible product/runtime issues.
- Feedback for confusing UX or product direction.
- Question if you are unsure whether something is expected.

Avoid attaching private logs, secrets, or real workspace files unless you have
sanitized them first.
