# Plato 快速开始

这是一条最短路径：从下载 Plato 到完成第一个可评估的任务计划。

## 1. 下载本地 beta 版本

当前 beta 下载版本：

- [Plato-1.1-beta-macos-arm64.dmg](https://github.com/zhanghao1903/plato-public/releases/download/v1.1-beta/Plato-1.1-beta-macos-arm64.dmg)

可选校验值：

```text
d8c71d1c1d06a99ca1598bd4dda09785efc4d4a6113f034a56b7803445a9bbdc  Plato-1.1-beta-macos-arm64.dmg
```

当前版本未签名、未公证。如果 macOS 拦截启动，请参考英文文档
[macOS local release usage](../../usage/macos-local-release.md)。
如果你需要 stable 基线版本，请查看 [公开版本](../product/versions.md)。

## 2. 打开 Plato

挂载 DMG 后打开 Plato。

第一次使用时建议：

- 先使用测试 workspace；
- 不要一开始就放入敏感文件；
- 在信任输出前，先查看任务状态、文件变化和 Audit Page。

## 3. 输入一个目标

创建或选择一个 Session，然后用自然语言描述你想完成的结果。

适合第一次尝试的输入：

- "帮我规划一个个人网站。"
- "把这个粗略想法拆成我可以检查的任务。"
- "在修改文件前，帮我先准备一组安全步骤。"
- "帮我规划一个七年级生物 HTML 课件。"

你不需要一开始就写出完美 prompt。Plato 的目标之一就是在需要时追问缺失上下文，而不是直接猜。

## 4. 检查计划

Plato 会把目标转成可见的任务计划。

发布前建议检查：

- 计划是否符合你的真实意图；
- 任务是否看得懂；
- 顺序是否合理；
- 哪些任务需要补充说明。

如果计划不对，先修改计划，不要急着执行。

![Plato Main Page](../../../assets/screenshots/plato-main-page.png)

## 5. 回答 ASK 问题

ASK 不是普通聊天。

ASK 出现时，表示 Plato 缺少应该由你提供的信息，而且不应该自己猜。

- Authoring ASK：计划生成前，Plato 需要补足目标或约束。
- Execution ASK：执行中，某个任务缺少信息，需要暂停等待你回答。

![Plato Authoring ASK](../../../assets/screenshots/plato-authoring-ask.svg)

## 6. 发布并检查

当计划看起来正确时，可以发布计划并观察任务进度。

执行后重点检查：

- 任务状态；
- 结果摘要；
- 文件变化；
- Audit Page 中的证据；
- workspace inspection 中的 Git 状态、文件查看和 diff。

![Plato Audit Page](../../../assets/screenshots/plato-audit-page.png)

## 7. 理解当前限制

`1.1-beta` 公开版本适合早期评估，但不是正式完整发行版。

当前限制：

- macOS 签名和公证还未完成；
- 暂时只提供 macOS Apple Silicon 版本；
- 部分截图展示的是产品方向或开发预览；
- public 仓库不是源码仓库。

下一步阅读：

- [常见问题](faq.md)
- [公开版本](../product/versions.md)
- [隐私与安全](../security/privacy-and-safety.md)
- [1.1-beta 发布说明](../releases/1.1-beta.md)
