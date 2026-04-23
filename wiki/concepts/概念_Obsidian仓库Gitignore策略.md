---
type: "concept"
tags: ["obsidian", "git", "gitignore", "同步", "冲突治理"]
summary: "Obsidian 仓库应通过 gitignore 过滤大文件、缓存和设备状态文件，以降低同步冲突与仓库膨胀风险。"
sources: ["raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md"]
updated: "2026-04-24"
---

# 概念：Obsidian 仓库 Gitignore 策略

## 目标
- 降低无效文件进入版本库的概率。
- 避免设备状态文件在多端来回覆盖造成冲突。
- 控制仓库体积，减少 Push/Pull 时间与失败概率。

## 常见忽略对象
- 大文件：`*.pdf`、`*.mp4`、`*.zip` 等。
- 系统文件：`.DS_Store`、`Thumbs.db`。
- Obsidian 缓存和设备状态：`.obsidian/cache/`、`workspace*.json`。
- 插件缓存/临时数据与垃圾箱目录：`.trash/` 等。

## 实践建议
- 先定义“必须版本化”的 Obsidian 配置，再把设备状态与缓存排除。
- 团队协作时统一 `.gitignore`，避免每人本地差异导致重复噪声提交。

## 关联
- [[concepts/概念_Obsidian多端同步方案选型]]
- [[concepts/概念_移动端一键同步脚本_Commit_Pull_Push]]

