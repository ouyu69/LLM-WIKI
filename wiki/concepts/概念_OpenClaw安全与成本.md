---
type: "concept"
tags: ["openclaw", "安全", "成本", "认证", "供应链"]
summary: "OpenClaw 的主要风险来自公网暴露、第三方 Skill、模型密钥、工具执行权限和失控 token 成本。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw 安全与成本

## 主要安全风险
- Gateway 暴露：如果端口直接暴露公网且认证不足，攻击者可能控制 Agent 或触发工具执行。
- RCE 漏洞：来源文档提到 CVE-2026-25253 曾导致大量暴露实例存在远程代码执行风险。
- Skill 供应链：第三方 Skill 可能包含恶意代码、凭证窃取逻辑或隐藏网络请求。
- 渠道滥用：未授权用户或群聊噪声可能消耗 API 额度并泄露上下文。
- 本地权限：Agent 可执行 Shell、读写文件、操作浏览器时，权限边界必须清楚。

## 成本风险
OpenClaw 的多轮思考、工具调用、记忆检索和跨渠道常驻运行会显著放大 token 消耗。来源文档多次强调“一觉醒来收到高额 API 账单”的风险。

## 防护清单
- Gateway 默认只绑定 localhost，远程访问使用安全隧道和强认证。
- 保持 OpenClaw 和插件更新，关注安全公告。
- 安装 Skill 前审查源码和权限。
- 设置模型 API 消费限额、告警和 fallback。
- 群聊使用 requireMention，私聊使用配对码、白名单和会话隔离。
- 对系统命令、文件写入、浏览器自动化等高危能力使用最小权限。

## 关联
- [[concepts/概念_OpenClaw架构]]
- [[concepts/概念_OpenClaw_Skills系统]]
- [[concepts/概念_OpenClaw模型配置]]
