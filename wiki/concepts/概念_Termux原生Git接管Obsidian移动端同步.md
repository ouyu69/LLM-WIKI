---
type: "concept"
tags: ["termux", "git", "obsidian", "android", "同步"]
summary: "在 Android 端用 Termux 的原生 Git 接管同步，可绕开部分移动端插件在大仓库下的性能瓶颈。"
sources: ["raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md"]
updated: "2026-04-24"
---

# 概念：Termux 原生 Git 接管 Obsidian 移动端同步

## 核心思路
- 电脑端继续使用标准 Git 客户端工作流。
- Android 端不依赖 Obsidian Git 插件，而是在 Termux 中执行原生 `git pull / commit / push`。
- 通过 `Termux:Widget` 将同步脚本暴露为桌面快捷操作。

## 关键前置
- Termux 与 Termux:Widget 需来自同一分发渠道并保持签名一致。
- 必须授权存储访问（`termux-setup-storage`）并将仓库放在可访问目录。
- 远程鉴权需使用 token（GitHub 已不支持密码推送）。

## 优势与边界
- 优势：速度更稳定、行为更接近桌面 Git、便于排障。
- 边界：仍需处理网络失败、冲突合并和凭据安全问题。

## 关联
- [[concepts/概念_Obsidian多端同步方案选型]]
- [[concepts/概念_移动端一键同步脚本_Commit_Pull_Push]]

