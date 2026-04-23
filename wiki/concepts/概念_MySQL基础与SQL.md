---
type: "concept"
tags: ["mysql", "database", "sql", "面试"]
summary: "MySQL 是主流关系型数据库，围绕表模型与 SQL 进行数据定义、查询与事务处理。"
sources: ["raw/已处理/MySQL常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：MySQL基础与SQL

## 定义
关系型数据库基于表结构组织数据，通过主键、外键和约束表达实体关系。MySQL 是最常见的关系型数据库之一，默认端口为 `3306`。

## SQL 作用
- DDL：定义数据库对象，如库、表、索引。
- DML：增删改查业务数据。
- DCL/TCL：控制权限与事务行为。

## 工程特点
- 开源生态成熟，学习资料和工具链完善。
- 事务能力和扩展方案成熟，适合从中小型到较大规模业务演进。
- 与主流后端语言、ORM、中间件兼容性好。

## 关联
- [[sources/来源_MySQL常见面试题总结]]
- [[concepts/概念_MySQL存储引擎_InnoDB与MyISAM]]
- [[concepts/概念_MySQL事务隔离级别与MVCC]]
