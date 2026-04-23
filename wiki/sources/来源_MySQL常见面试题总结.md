---
type: "source"
tags: ["mysql", "database", "面试", "javaguide"]
summary: "JavaGuide MySQL 面试题综述，覆盖基础、字段类型、存储引擎、索引、日志、事务、锁与性能优化。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 来源摘要：MySQL常见面试题总结

## 来源信息
- 文件：`raw/已处理/MySQL常见面试题总结.md`
- 来源站点：JavaGuide（MySQL 面试专题）
- 原始链接：`https://interview.javaguide.cn/database/mysql.html`
- 主题范围：MySQL 基础概念、类型设计、索引与执行、事务隔离、锁机制与性能优化

## 核心要点
- MySQL 作为主流关系型数据库，兼顾开源成本、生态成熟度与工程可用性，常用于业务系统持久化。
- 字段类型设计直接影响空间、索引效率和可维护性，应关注 `UNSIGNED`、`CHAR/VARCHAR`、`DATETIME/TIMESTAMP`、`NULL` 语义与约束。
- InnoDB 是默认存储引擎，支持事务、MVCC、行级锁与崩溃恢复；MyISAM 更偏向简单读场景但缺少事务能力。
- 索引核心围绕 B+ 树、最左前缀、覆盖索引与避免索引失效展开，目标是减少回表和全表扫描。
- MySQL 关键日志包括 `binlog`、`redo log`、`undo log`，分别支撑复制恢复、崩溃恢复与事务回滚/MVCC。
- 事务关注 ACID、隔离级别和并发异常；InnoDB 在 `REPEATABLE READ` 下结合 MVCC 与锁机制平衡一致性和吞吐。
- 锁体系包含表锁、行锁、意向锁、记录锁、间隙锁与临键锁，需要结合 SQL 条件与索引命中分析锁范围。
- 性能优化应从慢 SQL 定位与 `EXPLAIN` 入手，逐步推进索引/SQL/表结构，再评估读写分离、分库分表和缓存。

## 关联概念页
- [[concepts/概念_MySQL基础与SQL]]
- [[concepts/概念_MySQL字段类型设计]]
- [[concepts/概念_MySQL存储引擎_InnoDB与MyISAM]]
- [[concepts/概念_MySQL索引与最左前缀匹配]]
- [[concepts/概念_MySQL日志_binlog_redo_undo]]
- [[concepts/概念_MySQL事务隔离级别与MVCC]]
- [[concepts/概念_MySQL锁机制_表锁行锁意向锁]]
- [[concepts/概念_MySQL执行流程与EXPLAIN]]
- [[concepts/概念_MySQL性能优化路径]]

## Ingest 状态
- 已按主题粒度完成 ingest；未逐题拆页，避免产生过碎页面。
