# Plato Quickstart

This is the shortest path from download to a first useful Plato session.

## 1. Download The Local Release Candidate

Download the current macOS Apple Silicon asset:

- [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg)

Optional checksum:

```text
34bc9a24dbf29c8ba5ebdeb1d92a4428d55e791562596e4303734b493fdfb212  Plato-0.1.0-macos-arm64.dmg
```

The release is unsigned and non-notarized. If macOS blocks the first launch,
see [macOS local release usage](macos-local-release.md).

## 2. Open Plato

Mount the DMG and open Plato.

On first use, treat the app as a local release candidate:

- use a test workspace first;
- avoid sensitive files until you understand the flow;
- inspect audit and file-change surfaces before trusting output.

## 3. Start With A Goal

Create or select a session, then describe the outcome you want.

Good first prompts:

- "Help me plan a small personal website."
- "Turn this rough idea into tasks I can review."
- "Help me prepare a safe set of steps before changing files."
- "Draft a plan for creating a short courseware page."

You do not need a perfect prompt. Plato is designed to ask for missing context
when it should not guess.

## 4. Review The Plan

Plato should turn the goal into a visible task plan.

Before publishing, check:

- whether the plan matches your intent;
- whether the tasks are understandable;
- whether the order makes sense;
- whether any task needs extra guidance.

If the plan is wrong, refine it before running work.

![Plato Main Page](../../assets/screenshots/plato-main-page.png)

## 5. Answer ASK Questions

ASK is different from normal chat.

Plato uses ASK when it needs information that belongs to you and should not be
guessed.

- Authoring ASK appears before a plan is ready.
- Execution ASK appears when a task is blocked during work.

![Plato Authoring ASK](../../assets/screenshots/plato-authoring-ask.svg)

## 6. Publish And Inspect

When the plan looks right, publish it and watch task progress.

After work happens, inspect:

- task status;
- result summary;
- changed files, when available;
- Audit Page evidence.

![Plato Audit Page](../../assets/screenshots/plato-audit-page.png)

## 7. Know The Current Limits

The `0.1.0` public release is useful for early evaluation, but it is not a
fully polished public distribution.

Current caveats:

- macOS signing and notarization are not complete;
- broad platform support is not available;
- some screenshots show development previews;
- the repository hosts public docs and release assets, not source code.

Read next:

- [User guide](user-guide.md)
- [FAQ](faq.md)
- [Release status](../product/release-status.md)
- [Privacy and safety](../security/privacy-and-safety.md)
