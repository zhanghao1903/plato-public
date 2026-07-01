# Public Versions

Plato keeps two public release channels visible:

| Channel | Current version | Who should use it | What it means |
|---|---:|---|---|
| Stable | `1.1` | Reviewers who want the current formal public release. | Product 1.1 Router-first Conversation, Activity, Audit, workspace inspection, token usage, and precision file evidence foundations. |
| Beta | `1.1-beta` | Reviewers comparing the earlier Product 1.1 preview. | Older preview of the Product 1.1 inspection foundations, superseded by Stable `1.1` for new users. |

The previous Product 1.0 public baseline was `0.1.0`. It remains available in
GitHub releases for historical comparison, but the recommended stable download
is now `1.1`.

Both public channels are currently unsigned and non-notarized macOS Apple
Silicon local releases. Stable means the recommended public channel; it does not
mean app-store distribution quality.

## Downloads

| Channel | Download | Release notes | Metadata |
|---|---|---|---|
| Stable | [Plato-1.1-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1/Plato-1.1-macos-arm64.dmg) | [1.1 notes](../releases/1.1.md) | [manifest](../../releases/1.1/manifest.json) |
| Beta | [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg) | [1.1-beta notes](../releases/1.1-beta.md) | [manifest](../../releases/1.1-beta/manifest.json) |
| Product 1.0 baseline | [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg) | [0.1.0 notes](../releases/0.1.0.md) | [manifest](../../releases/0.1.0/manifest.json) |

## Feature Difference

| Capability | Product 1.0 baseline `0.1.0` | Stable `1.1` | Beta `1.1-beta` | Public docs |
|---|---|---|---|---|
| Task-first planning and review | Included | Included | Included | [Task-first workflow](task-first-workflow.md), [User guide](../usage/user-guide.md) |
| Authoring ASK and Execution ASK | Included as core interaction direction | Routed through Conversation and Runtime Input Router | Included as beta direction | [Product overview](overview.md#ask-when-plato-needs-the-user), [User guide](../usage/user-guide.md#2-let-plato-shape-the-work) |
| Runtime Input Router | Not included | Included | Included as beta foundation | [1.1 notes](../releases/1.1.md#runtime-input-router) |
| Durable Conversation / Activity | Partial task activity only | Included as primary history surface | Included as beta foundation | [1.1 notes](../releases/1.1.md#durable-conversation-and-activity) |
| Read-only inquiry | Not included | Included | Included as beta foundation | [1.1 notes](../releases/1.1.md#read-only-inquiry) |
| Contract revision commands | Not included | Included | Included as beta foundation | [1.1 notes](../releases/1.1.md#contract-revision-commands) |
| Token Usage Analytics | Not included | Included | Included as beta foundation | [User guide](../usage/user-guide.md#5-inspect-the-result) |
| Precision File Tools | Not included | Included | Included as beta foundation | [Privacy and safety](../security/privacy-and-safety.md#files-and-workspaces) |
| Workspace Inspection: Git, Diff, File Viewer | Not included | Included | Included as beta foundation | [Trust and audit](../architecture/trust-and-audit.md#workspace-inspection-direction), [Workspace inspection screenshot](../../assets/screenshots/plato-workspace-inspection.png) |
| Archived Plan access | Not included | Included | Partial | [1.1 notes](../releases/1.1.md#archived-plan-access) |
| Submit/focus/scroll runtime polish | Not included | Included and installer-smoke verified | Older beta behavior | [1.1 notes](../releases/1.1.md#frontend-interaction-runtime) |

## How To Choose

Choose Stable `1.1` for current evaluation.

Use Beta `1.1-beta` only when you need to compare the earlier Product 1.1
preview. Use `0.1.0` only when you need the older Product 1.0 baseline.

For release caveats, see [Release status](release-status.md).
