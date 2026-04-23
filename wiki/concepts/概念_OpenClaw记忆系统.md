---
type: "concept"
tags: ["openclaw", "记忆", "session", "agent"]
summary: "OpenClaw 通过 SOUL、TOOLS、USER、Session 四层记忆和 Markdown 文件系统保持长期上下文。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw 记忆系统

## 四层记忆
- SOUL：永久身份内核，定义 Agent 的人格、价值观和核心身份。
- TOOLS：当前可用工具和 Skills，随安装和启用动态变化。
- USER：关于用户偏好、决策和长期事实的持久记忆，通常只在 main/private session 加载。
- Session：当前对话上下文，token 接近上限时会被压缩。

## 文件组织
典型工作区包含 `AGENTS.md`、`SOUL.md`、`USER.md`、`MEMORY.md`、`HEARTBEAT.md`、`memory/YYYY-MM-DD.md`、`skills/` 和 `sessions.json`。

## 关键机制
- Daily Logs：按日期 append-only 记录交互，Session 启动时读取今天和昨天日志。
- Long-term Memory：`MEMORY.md` 保存长期偏好、事实和决策。
- Pre-Compaction：上下文接近 token 限制时，系统静默保存重要记忆后压缩旧消息。
- Semantic Search：结合 embedding 向量检索和 BM25 关键词检索回忆历史。

## 隔离原则
私聊会进入共享 main session 并加载长期记忆；群组默认使用隔离 session，避免泄露私聊记忆。

## 关联
- [[concepts/概念_OpenClaw架构]]
- [[concepts/概念_OpenClaw安全与成本]]
