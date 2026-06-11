# Privacy And Safety

This page explains the current public safety posture in plain language.

Plato `1.1-beta` is an early local beta release. It is useful for evaluation,
but it is not a formally audited or app-store-distributed product.

## Local-First Evaluation

The current public release runs as a local desktop app with a bundled sidecar
runtime candidate.

Practical guidance:

- test with non-sensitive workspaces first;
- avoid secrets, credentials, private customer data, and production files until
  you have reviewed local behavior yourself;
- inspect task state, file-change surfaces, and audit evidence before trusting
  output.

## User Control

Plato's product direction is to keep the user in control:

- goals become visible task plans;
- tasks can be reviewed before meaningful execution;
- ASK appears when user-owned context is missing;
- confirmations should stay close to the task they affect;
- Audit Page evidence remains read-only.

This does not mean every risk is solved in the current release. It means the
product is designed around visible control rather than hidden automation.

## Files And Workspaces

Some Plato workflows may inspect or change files in a local workspace.

Before using a real project:

1. use version control;
2. use a disposable branch or copy if the work is risky;
3. inspect proposed tasks before publishing;
4. review changed files and audit evidence afterward.

## Logs And Audit

Plato uses logs, messages, task state, and audit projections to help explain
what happened.

Do not share raw logs publicly unless you have checked and sanitized them.
Logs can contain local paths, prompts, file names, or other private context.

## Network And Providers

The public documentation describes Plato's product and local release posture.
Actual model/provider behavior depends on the runtime configuration used by the
app environment.

Do not put provider secrets or API keys into public issues, screenshots, or
logs.

## Current Distribution Caveats

The `1.1-beta` release is:

- unsigned;
- non-notarized;
- intended for local evaluation;
- not a formal security release;
- not a promise that every public screenshot is available as a stable feature.

It adds token usage analytics, precision file tool foundations, and workspace
inspection, but those features should still be evaluated in non-sensitive test
workspaces first.

See [Release status](../product/release-status.md).

## Reporting Concerns

Use GitHub issues for public-safe reports. If a report requires sensitive
details, describe the issue at a high level first and avoid attaching private
logs or workspaces.

Helpful reports include:

- release version;
- operating system and architecture;
- what you expected;
- what happened;
- whether files changed;
- safe screenshots or redacted logs.
