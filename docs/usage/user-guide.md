# Plato User Guide

This guide explains Plato in user language.

Plato is for work where you know the outcome you want, but you may not know the
best way to ask AI, split the work, confirm risky steps, or check the result.

## 1. Start With The Outcome

Begin by describing what you want to accomplish.

Good starting points sound like:

- "Help me turn this rough idea into a concrete plan."
- "Review this workspace and tell me what should happen next."
- "Help me prepare a safe set of steps before changing files."
- "Summarize the result and show me what changed."

You do not need to start with a perfect prompt. One purpose of Plato's
Inspiration Plane is to help you discover what AI can help with and what extra
context will improve the work.

## 2. Let Plato Shape The Work

Plato should not treat your first sentence as permission to act immediately.

Before meaningful work starts, Plato should help turn the goal into a clearer
task structure. It may identify missing context, surface assumptions, or show a
draft plan.

Useful context can include:

- the goal or outcome you care about;
- files, project, or topic boundaries;
- what should not be changed;
- examples of a good result;
- timing, quality, or risk constraints.

When Plato needs this information before it can build a useful plan, it should
ask you directly. This is an Authoring ASK.

![Plato Authoring ASK](../../assets/screenshots/plato-authoring-ask.svg)

## 3. Review The Plan

The Main Page is the control surface.

Use it to check:

- what Plato thinks the task is;
- which steps are planned;
- what is waiting, running, done, or failed;
- which items need your input;
- what result or file changes are available.

If the plan does not match your intent, adjust the goal before work continues.

![Plato Main Page](../../assets/screenshots/plato-main-page.png)

## 4. Confirm Risky Steps

For high-impact work, Plato should ask before proceeding.

Confirmations should stay close to the task they affect, so you can judge the
decision in context instead of responding to a generic popup.

Use confirmations to pause on actions such as:

- changing files;
- running a risky command;
- using a sensitive input;
- continuing after an incomplete or uncertain result.

ASK is different from confirmation. A confirmation means Plato knows the action
but needs your approval. An ASK means Plato is missing information and should
not guess.

During execution, Plato may ask a task-scoped question before continuing. This
is an Execution ASK. Answer it from the task detail panel.

![Plato Execution ASK](../../assets/screenshots/plato-execution-ask.svg)

## 5. Inspect The Result

When work completes, do not judge only by the final answer.

Check:

- the result summary;
- file changes, when files were touched;
- task status and failure details;
- audit evidence when you need to know what happened and why.

The Audit Page is the trust surface. It is for reviewing evidence, not for
controlling tasks.

![Plato Audit Page](../../assets/screenshots/plato-audit-page.png)

## 6. Continue, Revise, Or Stop

After a result, choose the next move:

- accept the result if it matches your goal;
- continue with more guidance;
- revise the plan if the work moved in the wrong direction;
- inspect evidence before trusting the output;
- stop if the request is no longer useful or safe.

## Current Release Notes

The current public release is an unsigned and non-notarized macOS local release
candidate. Some screenshots may show product direction or public-safe sample
flows that should be checked against [Release status](../product/release-status.md)
before being treated as available in a specific release.
