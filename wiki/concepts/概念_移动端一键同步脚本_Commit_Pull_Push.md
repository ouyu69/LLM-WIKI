---
type: "concept"
tags: ["termux", "脚本", "git", "同步", "鲁棒性"]
summary: "移动端一键同步脚本可把 add/commit/pull/push 串成受控流程，并加入防空提交、冲突熔断和权限自愈。"
sources: ["raw/已处理/Obsidian + GitHub + Termux 打造全平台丝滑同步工作流.md"]
updated: "2026-04-24"
---

# 概念：移动端一键同步脚本（Commit -> Pull -> Push）

## 标准流程
- `git add .` 收集本地变更。
- 仅在存在变更时 `git commit`，避免空提交报错。
- `git pull` 先同步远端，再决定是否继续推送。
- `git push` 将本地结果上送远端主分支。

## 保护机制
- 防空提交：通过 `git diff-index --quiet HEAD --` 判断是否需要提交。
- 冲突熔断：`pull` 失败时立刻退出，避免带冲突状态继续 push。
- 权限自愈：安卓环境可通过 `safe.directory` 减少 ownership 误报。

## 风险点
- token 明文写入命令或脚本存在泄露风险。
- 自动化脚本不能替代冲突理解；出现 `<<<<<<<` 仍需人工处理。

## 关联
- [[concepts/概念_Termux原生Git接管Obsidian移动端同步]]
- [[concepts/概念_Obsidian仓库Gitignore策略]]

