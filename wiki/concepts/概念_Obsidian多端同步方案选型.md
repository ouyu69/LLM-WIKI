---
type: "concept"
tags: ["obsidian", "同步", "选型", "github", "termux"]
summary: "Obsidian 多端同步常见有官方 Sync、网盘同步和 Git 同步；大仓库场景下可优先考虑原生 Git 路线。"
sources: ["raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md"]
updated: "2026-04-24"
---

# 概念：Obsidian 多端同步方案选型

## 常见路线
- 官方 Sync：体验稳定，开箱即用，但存在长期订阅成本。
- 网盘同步：部署简单，但双端并发修改时更容易出现冲突或覆盖风险。
- Git 同步：可审计、可回滚、可跨平台；在大仓库场景应优先使用原生 Git 实现。

## 选型维度
- 成本：预算是否允许持续订阅。
- 稳定性：是否能接受移动端插件在大仓库下的性能波动。
- 可控性：是否需要版本历史、分支能力和冲突可追踪性。
- 使用门槛：是否愿意维护 token、.gitignore 和脚本。

## 实践结论
在“PC 常规写作 + Android 高频查看/修改 + 仓库规模较大”场景下，`PC 原生 Git + Termux 原生 Git` 通常比“移动端 Git 插件”更稳定。

## 关联
- [[concepts/概念_Termux原生Git接管Obsidian移动端同步]]
- [[concepts/概念_Obsidian仓库Gitignore策略]]
- [[concepts/概念_移动端一键同步脚本_Commit_Pull_Push]]

