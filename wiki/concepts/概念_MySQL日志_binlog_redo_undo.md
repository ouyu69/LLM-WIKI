---
type: "concept"
tags: ["mysql", "database", "binlog", "redo-log", "undo-log"]
summary: "binlog、redo log、undo log 分工不同，分别支持复制恢复、崩溃恢复与回滚/MVCC。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：MySQL日志 binlog redo undo

## 三类日志分工
- `binlog`：Server 层逻辑日志，记录已提交事务变更，用于主从复制与时间点恢复。
- `redo log`：InnoDB 物理日志，保证崩溃后已提交数据可恢复（WAL）。
- `undo log`：记录修改前镜像，用于事务回滚与 MVCC 历史版本读取。

## 常见面试关注点
- 为什么需要 redo：减少随机写，先顺序写日志再落盘数据页。
- 为什么需要 undo：支持回滚和一致性读。
- 为什么还要 binlog：跨实例复制和逻辑恢复依赖 binlog。

## 关联
- [[sources/来源_MySQL常见面试题总结]]
- [[concepts/概念_MySQL事务隔离级别与MVCC]]
