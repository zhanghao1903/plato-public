# 公开版本

Plato 对外保留两个公开发布通道：

| 通道 | 当前版本 | 适合谁 | 含义 |
|---|---:|---|---|
| Stable | `1.1` | 想评估当前正式公开版本的用户和评审者。 | Product 1.1 Router-first Conversation、Activity、Audit、workspace inspection、token 使用和 precision file evidence 基础能力。 |
| Beta | `1.1-beta` | 想对比早期 Product 1.1 preview 的评审者。 | Product 1.1 inspection 基础能力的旧 preview；新用户应优先使用 Stable `1.1`。 |

之前的 Product 1.0 公开基线是 `0.1.0`。它仍保留在 GitHub releases 中用于历史对比，但推荐 stable 下载已经是 `1.1`。

两个公开通道当前都是未签名、未公证的 macOS Apple Silicon 本地版本。这里的 Stable 指推荐公开通道，不等于应用商店级正式分发。

## 下载

| 通道 | 下载 | 发布说明 | 元数据 |
|---|---|---|---|
| Stable | [Plato-1.1-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1/Plato-1.1-macos-arm64.dmg) | [1.1 发布说明](../releases/1.1.md) | [manifest](../../../releases/1.1/manifest.json) |
| Beta | [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg) | [1.1-beta 发布说明](../releases/1.1-beta.md) | [manifest](../../../releases/1.1-beta/manifest.json) |
| Product 1.0 基线 | [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg) | [0.1.0 notes](../../releases/0.1.0.md) | [manifest](../../../releases/0.1.0/manifest.json) |

## 特性区别

| 能力 | Product 1.0 基线 `0.1.0` | Stable `1.1` | Beta `1.1-beta` | 公开文档 |
|---|---|---|---|---|
| Task-first 计划与检查 | 已包含 | 已包含 | 已包含 | [英文 Task-first workflow](../../product/task-first-workflow.md)、[英文 User guide](../../usage/user-guide.md) |
| Authoring ASK 与 Execution ASK | 作为核心交互方向包含 | 通过 Conversation 和 Runtime Input Router 路由 | beta 方向已包含 | [英文 Product overview](../../product/overview.md#ask-when-plato-needs-the-user)、[快速开始](../usage/quickstart.md) |
| Runtime Input Router | 不包含 | 已包含 | beta 基础能力 | [1.1 发布说明](../releases/1.1.md#runtime-input-router) |
| Durable Conversation / Activity | 只有部分任务活动 | 作为主要历史界面包含 | beta 基础能力 | [1.1 发布说明](../releases/1.1.md#durable-conversation-and-activity) |
| Read-only inquiry | 不包含 | 已包含 | beta 基础能力 | [1.1 发布说明](../releases/1.1.md#read-only-inquiry) |
| Contract revision commands | 不包含 | 已包含 | beta 基础能力 | [1.1 发布说明](../releases/1.1.md#contract-revision-commands) |
| Token Usage Analytics | 不包含 | 已包含 | beta 基础能力 | [英文 User guide](../../usage/user-guide.md#5-inspect-the-result) |
| Precision File Tools | 不包含 | 已包含 | beta 基础能力 | [隐私与安全](../security/privacy-and-safety.md) |
| Workspace Inspection: Git / Diff / File Viewer | 不包含 | 已包含 | beta 基础能力 | [英文 Trust and audit](../../architecture/trust-and-audit.md#workspace-inspection-direction)、[Workspace inspection 截图](../../../assets/screenshots/plato-workspace-inspection.png) |
| Archived Plan access | 不包含 | 已包含 | 部分包含 | [1.1 发布说明](../releases/1.1.md#archived-plan-access) |
| 提交、焦点、滚动 runtime polish | 不包含 | 已包含并通过 installer smoke | 旧 beta 行为 | [1.1 发布说明](../releases/1.1.md#frontend-interaction-runtime) |

## 如何选择

当前评估请选择 Stable `1.1`。

只有需要对比早期 Product 1.1 preview 时才使用 Beta `1.1-beta`；只有需要 Product 1.0 旧基线时才使用 `0.1.0`。

发布限制请参考英文 [Release status](../../product/release-status.md)。
