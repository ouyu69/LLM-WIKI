---
type: "concept"
tags: ["openclaw", "部署", "渠道", "docker", "飞书", "钉钉"]
summary: "OpenClaw 支持本地、Docker、云服务器和面板部署，并通过国际与国内消息平台接入用户。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw 部署与渠道接入

## 部署方式
- 本地安装：适合开发者和单机实验，通常通过 npm 全局安装并初始化 daemon。
- Docker 部署：适合服务器长期运行，便于升级和隔离。
- 国内云一键部署：适合非深度技术用户，文档中提到阿里云、腾讯云等方案。
- 1Panel/Umbrel 等面板：适合同时管理多个自托管服务。

## 初始配置
首次使用通常需要完成模型认证、Gateway 启动、设备配对、渠道授权和基础安全策略设置。

## 渠道接入
- 国际渠道：WhatsApp、Telegram、Discord、Slack 等。
- 国内渠道：飞书、钉钉、QQ Bot、企业微信等，文档重点提到 openclaw-china 插件。
- 群组策略：默认应要求 mention 才响应，避免群聊噪声造成 token 浪费。

## 远程访问建议
不要直接把 Gateway 端口暴露到公网。更稳妥的方式是 localhost 绑定 + Tailscale/反向代理 + 强认证 + 最小权限。

## 关联
- [[concepts/概念_OpenClaw架构]]
- [[concepts/概念_OpenClaw安全与成本]]
- [[concepts/概念_OpenClaw模型配置]]
