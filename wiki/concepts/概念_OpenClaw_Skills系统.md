---
type: "concept"
tags: ["openclaw", "skills", "插件", "安全"]
summary: "OpenClaw Skills 是扩展 Agent 能力的插件机制，但第三方 Skill 必须经过安全审查。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw Skills 系统

## 定义
Skills 是 OpenClaw 的能力扩展单元，可为 Agent 添加具体工具、流程、领域知识或第三方集成。工作区本地 `skills/` 的优先级高于全局和内置技能。

## 生态来源
- 内置 Skills：随系统提供，基础可信度较高。
- ClawHub：社区技能市场，数量大但质量差异明显。
- 自建 Skill：适合私有业务流程、公司内部工具和个人自动化。

## 安全风险
文档强调 ClawHub 中存在垃圾、重复、低质量甚至恶意 Skill。恶意 Skill 可能窃取凭证、滥用 API、执行危险命令或植入供应链攻击。

## 使用准则
- 优先安装官方、知名作者或精选列表中的 Skill。
- 安装前阅读源码、权限和外部网络调用。
- 对涉及 Shell、文件系统、浏览器、凭证读取的 Skill 提高审查等级。
- 使用最小权限、沙箱、预算限制和日志审计。

## 关联
- [[concepts/概念_OpenClaw安全与成本]]
- [[concepts/概念_OpenClaw生态与国内产品]]
