---
type: "concept"
tags: ["openclaw", "架构", "gateway", "websocket"]
summary: "OpenClaw 采用 Gateway-Node-Channel 三层架构，用 WebSocket 将控制、执行和消息渠道解耦。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw 架构

## 定义
OpenClaw 的核心架构是 Gateway-Node-Channel 三层模型：Gateway 作为中央控制平面，Node 负责设备端执行，Channel 负责连接外部消息平台。

## 三层职责
- Gateway：维护 WebSocket 服务、管理 session、调度 Agent，默认监听 `127.0.0.1:18789`。
- Node：执行本地能力，例如摄像头、录屏、系统命令、文件和浏览器操作。
- Channel：对接 WhatsApp、Telegram、Discord、Slack、飞书、钉钉等消息渠道。

## 安全默认值
Loopback-First 是架构中的关键安全设计：Gateway 默认只绑定 localhost，不直接暴露公网端口。远程访问应通过 Tailscale Serve/Funnel 等方式转发，并叠加认证。

## 消息流
用户消息进入 Channel 后，由 Gateway 路由给 Agent；Agent 推理后调用 Node 执行工具，再将结果返回给用户所在渠道。

## 设计取舍
- 优点：控制面、执行面、渠道面解耦，便于扩展渠道和设备能力。
- 风险：一旦 Gateway 暴露或认证不足，攻击者可能间接触发本地工具执行。

## 关联
- [[overview/主题_OpenClaw总览]]
- [[concepts/概念_OpenClaw部署与渠道接入]]
- [[concepts/概念_OpenClaw安全与成本]]
