---
type: "concept"
tags: ["openclaw", "模型", "claude", "gpt", "deepseek", "ollama"]
summary: "OpenClaw 支持多模型提供商，模型选择需要在能力、成本、隐私和稳定性之间折中。"
sources: ["raw/已处理/OpenClaw橙皮书_extracted.txt"]
updated: "2026-04-23"
---

# 概念：OpenClaw 模型配置

## 支持范围
OpenClaw 的模型层可接入国际模型、国产模型和本地模型。来源文档提到 Claude、GPT、DeepSeek、Gemini、GLM、Qwen、Kimi、Ollama 等。

## 选择维度
- Agent 能力：复杂多步骤任务更依赖强推理和工具调用稳定性。
- 成本：OpenClaw 多轮工具调用会放大 token 消耗，便宜模型或本地模型可显著降本。
- 隐私：本地模型更适合敏感数据，但能力和硬件成本需评估。
- 可用性：应配置 fallback，避免单一模型服务异常导致 Agent 不可用。

## 推荐思路
- 高价值复杂任务：强模型作为 primary。
- 高频低风险任务：低成本模型或国产模型。
- 隐私敏感任务：Ollama 本地模型或私有部署模型。
- 生产环境：开启预算限制、模型连通性探测和用量监控。

## 关联
- [[concepts/概念_OpenClaw安全与成本]]
- [[concepts/概念_OpenClaw部署与渠道接入]]
