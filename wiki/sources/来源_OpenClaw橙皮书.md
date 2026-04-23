---
type: "source"
tags: ["openclaw", "agent", "部署", "skills", "安全", "模型"]
summary: "OpenClaw 橙皮书的结构化摘要，覆盖产品定位、架构、记忆、部署、渠道、Skills、模型、安全成本与生态。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 来源摘要：OpenClaw 橙皮书

## 来源信息
- 文件：`raw/已处理/OpenClaw橙皮书_extracted.txt`
- 文档版本：v1.1.0
- 适用版本：v2026.3.8
- 发布时间：2026-03-11
- 作者/整理：花叔，基于 OpenClaw 官方文档、GitHub 仓库与社区资料整理

## 核心要点
- OpenClaw 被定义为开源、自托管的 AI Agent 系统，强调让 AI 从问答工具变成可长期在线执行任务的“数字员工”。
- 系统采用 Gateway-Node-Channel 三层架构，通过 WebSocket 总线连接控制平面、本地执行节点与 20+ 消息渠道。
- 记忆系统由 SOUL、TOOLS、USER、Session 四层组成，并通过 Daily Logs、`MEMORY.md`、向量检索与压缩前保存机制保持上下文连续性。
- 部署方式覆盖本地 npm、Docker、国内云厂商一键部署与 1Panel 等面板方案；默认建议 Gateway 仅绑定 localhost。
- 渠道接入覆盖 WhatsApp、Telegram、Discord、Slack、飞书、钉钉、QQ、企业微信等，国内生态重点依赖 openclaw-china 插件。
- Skills 系统通过 ClawHub 市场和本地技能目录扩展能力，但第三方 Skill 存在质量与供应链风险，安装前必须审查。
- 模型配置支持 Claude、GPT、DeepSeek、Gemini、GLM、Qwen、Kimi、Ollama 等，建议用 fallback 与预算限制控制稳定性和成本。
- 安全与成本是使用 OpenClaw 的核心约束：文档提到 RCE 漏洞、恶意 Skills、账号封禁、API 账单失控等风险案例。
- OpenClaw 与 Claude Code 的关系是互补：前者管多渠道生活/工作自动化，后者管代码库内的编程任务。
- 中文社区形成“养虾”文化，并出现 QClaw、MaxClaw、AutoClaw、ArkClaw、KimiClaw、WorkBuddy、LobsterAI、CoPaw、miclaw 等产品。

## 关联页面
- [[overview/主题_OpenClaw总览]]
- [[concepts/概念_OpenClaw架构]]
- [[concepts/概念_OpenClaw记忆系统]]
- [[concepts/概念_OpenClaw部署与渠道接入]]
- [[concepts/概念_OpenClaw_Skills系统]]
- [[concepts/概念_OpenClaw模型配置]]
- [[concepts/概念_OpenClaw安全与成本]]
- [[concepts/概念_OpenClaw生态与国内产品]]
- [[comparisons/OpenClaw_vs_Claude_Code]]

## 使用提醒
- 本页仅归纳 raw 文档内容；涉及版本、Stars、产品价格、漏洞状态等时效信息，查询时应优先以最新官方来源复核。
