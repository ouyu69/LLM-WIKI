---
type: "concept"
tags: ["mysql", "database", "transaction", "isolation", "mvcc"]
summary: "MySQL 事务围绕 ACID 与隔离级别展开，InnoDB 通过 MVCC 与锁机制处理并发一致性。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：MySQL事务隔离级别与MVCC

## 定义
事务是一组要么全部成功、要么全部失败的数据库操作。数据库事务通常强调 ACID 特性。

## 并发异常
- 脏读：读到未提交数据。
- 不可重复读：同一事务两次读取结果不同。
- 幻读：同一条件查询出现“新行”。

## 隔离级别
- `READ UNCOMMITTED`
- `READ COMMITTED`
- `REPEATABLE READ`（MySQL 默认）
- `SERIALIZABLE`

## MVCC 作用
InnoDB 在 RC/RR 下通过多版本并发控制提供一致性读，降低读写互斥；配合间隙锁/临键锁处理特定幻读风险。

## 关联
- [[sources/来源_MySQL常见面试题总结]]
- [[concepts/概念_MySQL日志_binlog_redo_undo]]
- [[concepts/概念_MySQL锁机制_表锁行锁意向锁]]
