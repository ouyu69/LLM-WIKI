---
type: "concept"
tags: ["mysql", "database", "explain", "执行计划", "sql优化"]
summary: "使用 EXPLAIN 分析 SQL 执行计划，是 MySQL 调优定位瓶颈的基础能力。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：MySQL执行流程与EXPLAIN

## 定义
执行计划描述 SQL 经优化器处理后的访问路径和执行策略。`EXPLAIN` 用于查看计划而非直接执行查询。

## 关注字段
- `type`：访问方式，是否全表扫描。
- `key` / `possible_keys`：候选索引与实际命中索引。
- `rows`：预计扫描行数。
- `Extra`：附加信息，如 `Using filesort`、`Using temporary`。

## 调优步骤
1. 先定位慢 SQL（日志或监控）。
2. 用 `EXPLAIN` 看扫描与索引使用。
3. 调整索引、SQL 写法或表结构。
4. 回归验证执行计划与耗时变化。

## 关联
- [[sources/来源_MySQL常见面试题总结]]
- [[concepts/概念_MySQL索引与最左前缀匹配]]
- [[concepts/概念_MySQL性能优化路径]]
