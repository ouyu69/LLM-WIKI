---
type: "overview"
tags: ["openclaw", "agent", "自托管", "总览"]
summary: "OpenClaw 是一个自托管、多渠道、可扩展的 AI Agent 平台，核心价值是长期在线执行任务并保留用户数据控制权。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 主题：OpenClaw 总览

## 一句话结论
OpenClaw 的定位不是更强的聊天机器人，而是一个自托管的“个人 AI 操作系统”：通过消息渠道唤醒 Agent，让它长期在线、调用工具、执行任务并维护记忆。

## 核心定位
- 与 ChatGPT 相比，OpenClaw 强调自主执行任务，而不是单轮问答。
- 与 Claude Code 相比，OpenClaw 强调消息渠道、生活/办公自动化和长期记忆，而不是代码库内的专业编程。
- 与传统自动化脚本相比，OpenClaw 的优势在于自然语言入口、模型推理、工具调用和可扩展 Skills。

## 关键能力
- 多渠道接入：WhatsApp、Telegram、Discord、Slack、飞书、钉钉、QQ、企业微信等。
- 自托管：默认数据在用户自己的服务器或本地机器上。
- 工具执行：可调用 Shell、浏览器、文件系统、设备能力和第三方插件。
- 长期记忆：通过 Markdown 文件、Daily Logs、向量检索与 session 压缩保存上下文。
- 生态扩展：ClawHub Skills 与国内 openclaw-china 插件扩展任务能力和渠道接入。

## 主要约束
- 成本不可忽视：多轮推理与工具调用可能消耗远高于普通聊天的 token。
- 安全责任转移给自托管者：暴露端口、第三方 Skill、模型密钥和本地命令执行都需要防护。
- 生态质量参差：热门不等于安全，第三方插件需要代码审查和权限隔离。

## 关联
- [[sources/来源_OpenClaw橙皮书]]
- [[concepts/概念_OpenClaw架构]]
- [[concepts/概念_OpenClaw安全与成本]]
- [[comparisons/OpenClaw_vs_Claude_Code]]
