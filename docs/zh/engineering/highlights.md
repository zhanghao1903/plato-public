# Plato 工程亮点

这份文档面向招聘方和技术评审者，解释 Plato 在 UI 之外体现出的工程判断。

public 仓库不是源码镜像，因此这里以公开安全的方式介绍系统设计。

## 1. Task-first 产品架构

Plato 把任务视为用户可见的工作契约。

这和普通聊天界面不同：

- 规划和执行分离；
- 用户问题绑定到 authoring 或具体任务；
- 进度投影为任务状态；
- 结果、文件变化和审计证据回连到任务结构。

这让普通用户更容易理解，也让工程上更容易测试和追踪。

## 2. 本地桌面 App 与 Sidecar Runtime

`1.1-beta` 公开版本将桌面 UI 和 Python sidecar runtime candidate 打包在一起。

这说明：

- UI 可以在本地 runtime 工作时保持响应；
- 用户无需 clone 源码仓即可评估产品；
- 发布资产可以做 checksum 校验；
- 本地优先的工作流可以在云端分发前先验证。

## 3. Main Page 是产品投影

Main Page 不是原始日志查看器，而是 session、plan、task、message 和状态事实的产品投影。

它要回答：

- 当前是否有计划；
- 选中了哪个任务；
- 什么需要用户注意；
- 用户现在能做什么；
- 证据在哪里查看。

这样可以把 runtime 复杂度挡在主要 UX 之外。

## 4. Audit Page 是 Trust Plane

Audit Page 故意设计为只读页面。它帮助用户理解发生了什么，而不是修改任务或会话。

工程含义：

- 审计证据和控制动作分离；
- 证据可以过滤和查看，但不改变状态；
- 敏感 payload 可以隐藏或部分披露；
- Trust Plane 可以逐步增强，不需要压垮 Main Page。

## 5. ASK 和确认是不同概念

Plato 区分 ASK 和 confirmation：

- ASK：系统缺少用户拥有的信息，不应该猜；
- confirmation：系统知道动作，但需要用户批准。

这个区别可以降低误操作，也让 UI 更容易理解。

## 6. 上下文治理

LLM 调用本身是无状态的，但 Plato 的工作会话是有状态的。系统需要在每次模型调用前，把任务、workspace、消息、事件、权限和结果事实组织成有边界的上下文。

公开架构中将这称为 context governance：

![Plato context governance](../../../assets/images/plato-context-governance.svg)

目标是避免隐藏的聊天记忆成为唯一事实来源。

## 7. 发布纪律

当前 public release 包含：

- GitHub Release 中的大体积 DMG；
- machine-readable manifest；
- SHA256 checksum；
- 明确的 unsigned / non-notarized 说明；
- 与机器元数据分离的人类可读发布说明。

DMG 不提交进 Git 仓库。

## 8. 这个项目展示了什么

Plato 当前公开仓展示了：

- Task-first AI UX 的产品判断；
- 本地桌面应用与 sidecar runtime 的打包方式；
- Control Plane 和 Trust Plane 的分离；
- 对发布边界的清晰说明；
- 重视审计和证据，而不是盲目自动化；
- 区分已发布、开发预览、路线图和概念声明的公开文档组织方式。
