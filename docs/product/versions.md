# Public Versions

Plato keeps two public release channels visible:

| Channel | Current version | Who should use it | What it means |
|---|---:|---|---|
| Stable | `0.1.0` | Reviewers who want the conservative public baseline. | The task-first loop, Main Page, ASK basics, Audit Page, and public-safe docs. |
| Beta | `1.1-beta` | Reviewers who want the newest Product 1.1 inspection foundations. | Stable baseline plus token usage analytics, precision file tools, and workspace inspection. |

Both public channels are currently unsigned and non-notarized macOS Apple
Silicon local releases. Stable means the more conservative public baseline; it
does not mean app-store distribution quality.

## Downloads

| Channel | Download | Release notes | Metadata |
|---|---|---|---|
| Stable | [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg) | [0.1.0 notes](../releases/0.1.0.md) | [manifest](../../releases/0.1.0/manifest.json) |
| Beta | [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg) | [1.1-beta notes](../releases/1.1-beta.md) | [manifest](../../releases/1.1-beta/manifest.json) |

## Feature Difference

| Capability | Stable `0.1.0` | Beta `1.1-beta` | Public docs |
|---|---|---|---|
| Task-first planning and review | Included | Included | [Task-first workflow](task-first-workflow.md), [User guide](../usage/user-guide.md) |
| Authoring ASK and Execution ASK | Included as core interaction direction | Included | [Product overview](overview.md#ask-when-plato-needs-the-user), [User guide](../usage/user-guide.md#2-let-plato-shape-the-work) |
| Main Page control surface | Included | Included | [Product overview](overview.md#control-plane), [Main Page screenshot](../../assets/screenshots/plato-main-page.png) |
| Audit Page trust surface | Included | Included | [Trust and audit](../architecture/trust-and-audit.md), [Audit screenshot](../../assets/screenshots/plato-audit-page.png) |
| Token Usage Analytics | Not included | Included as beta foundation | [1.1-beta release notes](../releases/1.1-beta.md#token-usage-analytics), [User guide](../usage/user-guide.md#5-inspect-the-result) |
| Precision File Tools | Not included | Included as beta foundation | [1.1-beta release notes](../releases/1.1-beta.md#precision-file-tools), [Privacy and safety](../security/privacy-and-safety.md#files-and-workspaces) |
| Workspace Inspection: Git, Diff, File Viewer | Not included | Included as beta foundation | [Trust and audit](../architecture/trust-and-audit.md#workspace-inspection-direction), [Workspace inspection screenshot](../../assets/screenshots/plato-workspace-inspection.png) |

## How To Choose

Choose Stable when you want the simplest public baseline for understanding the
task-first product model.

Choose Beta when you want to evaluate the latest inspection and evidence
surfaces. Beta features are public, but their UI, coverage, and docs may still
change faster than the stable channel.

For release caveats, see [Release status](release-status.md).
