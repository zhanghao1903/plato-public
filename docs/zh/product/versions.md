# 公开版本

Plato 对外只维护两个公开发布通道：

| 通道 | 当前版本 | 适合谁 | 含义 |
|---|---:|---|---|
| Stable | `0.1.0` | 想评估保守公开基线的评审者。 | Task-first 基础循环、Main Page、ASK 基础、Audit Page 和公开安全文档。 |
| Beta | `1.1-beta` | 想评估最新 Product 1.1 inspection 基础能力的评审者。 | Stable 基线加上 token 使用分析、精确文件工具和 workspace inspection。 |

两个公开通道当前都是未签名、未公证的 macOS Apple Silicon 本地版本。
这里的 Stable 指更保守的公开基线，不等于应用商店级正式发行。

## 下载

| 通道 | 下载 | 发布说明 | 元数据 |
|---|---|---|---|
| Stable | [Plato-0.1.0-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v0.1.0/Plato-0.1.0-macos-arm64.dmg) | [0.1.0 notes](../../releases/0.1.0.md) | [manifest](../../../releases/0.1.0/manifest.json) |
| Beta | [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg) | [1.1-beta 发布说明](../releases/1.1-beta.md) | [manifest](../../../releases/1.1-beta/manifest.json) |

## 特性区别

| 能力 | Stable `0.1.0` | Beta `1.1-beta` | 公开文档 |
|---|---|---|---|
| Task-first 计划与检查 | 已包含 | 已包含 | [英文 Task-first workflow](../../product/task-first-workflow.md)、[英文 User guide](../../usage/user-guide.md) |
| Authoring ASK 与 Execution ASK | 作为核心交互方向包含 | 已包含 | [英文 Product overview](../../product/overview.md#ask-when-plato-needs-the-user)、[快速开始](../usage/quickstart.md) |
| Main Page 控制面 | 已包含 | 已包含 | [英文 Product overview](../../product/overview.md#control-plane)、[Main Page 截图](../../../assets/screenshots/plato-main-page.png) |
| Audit Page 信任面 | 已包含 | 已包含 | [英文 Trust and audit](../../architecture/trust-and-audit.md)、[Audit 截图](../../../assets/screenshots/plato-audit-page.png) |
| Token Usage Analytics | 不包含 | beta 基础能力 | [1.1-beta 发布说明](../releases/1.1-beta.md#token-usage-analytics)、[英文 User guide](../../usage/user-guide.md#5-inspect-the-result) |
| Precision File Tools | 不包含 | beta 基础能力 | [1.1-beta 发布说明](../releases/1.1-beta.md#precision-file-tools)、[隐私与安全](../security/privacy-and-safety.md) |
| Workspace Inspection: Git / Diff / File Viewer | 不包含 | beta 基础能力 | [英文 Trust and audit](../../architecture/trust-and-audit.md#workspace-inspection-direction)、[Workspace inspection 截图](../../../assets/screenshots/plato-workspace-inspection.png) |

## 如何选择

如果你想先理解 Plato 的任务计划、控制和审计基础模型，选择 Stable。

如果你想评估最新的 inspection 和 evidence 能力，选择 Beta。Beta 特性已经公开，
但 UI、覆盖范围和文档仍可能比 stable 通道变化更快。

发布限制请参考英文 [Release status](../../product/release-status.md)。
