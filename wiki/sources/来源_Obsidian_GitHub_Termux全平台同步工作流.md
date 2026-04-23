---
type: "source"
tags: ["obsidian", "github", "termux", "同步", "android", "git"]
summary: "基于 Obsidian 论坛实践的全平台同步方案，核心是 PC 端原生 Git + Android 端 Termux 原生 Git + Widget 一键同步。"
sources: ["raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md"]
updated: "2026-04-24"
---

# 来源摘要：Obsidian + GitHub + Termux 全平台同步工作流

## 来源信息
- 文件：`raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md`
- 原帖地址：https://forum-zh.obsidian.md/t/topic/60487
- 作者：`[[AuroRa1]]`
- 发布时间：2026-04-13
- 适用场景：PC（Win11）+ Android 的 Obsidian 多端同步

## 核心要点
- 传统方案痛点：官方 Sync 成本高，网盘同步容易冲突，移动端 Obsidian Git 插件在大仓库场景可能出现状态扫描卡死。
- 方案核心：PC 保持标准 Git 工作流；Android 使用 Termux 中的原生 Git（非 isomorphic-git）进行拉取、提交、推送。
- 认证方式：GitHub 已不支持密码推送，需要使用 Personal Access Token（文中推荐 classic token + `repo` 权限）。
- 仓库治理：通过 `.gitignore` 过滤大文件、缓存文件和设备工作区状态，减少冲突与无效提交。
- 移动端落地：利用 `Termux:Widget` 绑定同步脚本，实现桌面一键执行 `add -> commit -> pull -> push`。
- 鲁棒性设计：脚本包含空提交跳过、Pull 失败熔断、`safe.directory` 自愈等保护逻辑。
- 国内网络备选：可将远程从 GitHub 切换到 Gitee，但需注意更严格的容量限制和 URL/token 格式差异。

## 关联页面
- [[concepts/概念_Obsidian多端同步方案选型]]
- [[concepts/概念_Termux原生Git接管Obsidian移动端同步]]
- [[concepts/概念_Obsidian仓库Gitignore策略]]
- [[concepts/概念_移动端一键同步脚本_Commit_Pull_Push]]

## 使用提醒
- 原文包含 token 直接拼接 URL 的示例；生产实践中应优先使用更安全的凭据管理方式，避免明文泄露。
