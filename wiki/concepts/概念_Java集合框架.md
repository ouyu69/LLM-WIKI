---
type: "concept"
tags: ["java", "集合", "collection", "map"]
summary: "Java 集合框架以 Collection 和 Map 为核心，分别承载单元素容器与键值对容器。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 集合框架

## 定义
Java 集合也叫容器，主要分为两条体系：
- `Collection`：存放单个元素，常见子接口包括 `List`、`Set`、`Queue`。
- `Map`：存放 key-value 键值对，通过 key 定位 value。

## 常见接口语义
- `List`：元素有序、可重复，适合按位置访问和保留插入顺序的场景。
- `Set`：元素不可重复，适合去重和成员存在性判断。
- `Queue`：按队列规则确定元素先后，适合排队、缓冲和任务调度。
- `Map`：key 无序且不可重复，value 可重复，适合通过 key 快速查找对象。

## 面试关注点
- 先按语义选择接口，再按性能和并发需求选择具体实现。
- `Collection` 与 `Map` 不是继承关系，二者解决的问题不同。
- 集合实现通常需要同时考虑顺序、重复性、查询性能、插入删除成本和线程安全。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_ArrayList与LinkedList]]
- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]]
- [[concepts/概念_Queue与Deque]]
- [[concepts/概念_HashMap底层实现]]
