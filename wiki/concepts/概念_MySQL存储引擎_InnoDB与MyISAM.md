---
type: "concept"
tags: ["mysql", "database", "innodb", "myisam", "存储引擎"]
summary: "InnoDB 是 MySQL 默认存储引擎，提供事务、行锁与崩溃恢复；MyISAM 更轻量但不支持事务。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：MySQL存储引擎 InnoDB与MyISAM

## 定义
存储引擎决定数据在磁盘上的组织方式、索引实现、锁粒度与事务能力。MySQL 支持多引擎，默认使用 InnoDB。

## InnoDB 特点
- 支持事务与 ACID。
- 支持行级锁与 MVCC。
- 支持崩溃恢复（redo/undo 机制）。
- 聚簇索引按主键组织数据，适合 OLTP 场景。

## MyISAM 特点
- 不支持事务与行级锁。
- 读性能在部分简单场景可接受。
- 更适合历史只读或低并发写入场景。

## 选型建议
- 默认优先 InnoDB。
- 只有在明确无事务需求且读多写少时，才评估 MyISAM 或其他替代引擎。

## 关联
- [[sources/来源_MySQL常见面试题总结]]
- [[concepts/概念_MySQL事务隔离级别与MVCC]]
- [[concepts/概念_MySQL锁机制_表锁行锁意向锁]]
