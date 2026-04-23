---
type: "concept"
tags: ["java", "集合", "map", "hashmap"]
summary: "HashMap 基于哈希桶组织键值对，JDK 1.8 后使用数组、链表和红黑树处理哈希冲突。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：HashMap 底层实现

## 数据结构
- JDK 1.8 之前：数组 + 链表。
- JDK 1.8 之后：数组 + 链表/红黑树；当冲突链表达到阈值且容量满足条件时，链表会树化以降低查找成本。

## 定位桶
`HashMap` 通过 key 的 hash 值计算桶下标。容量使用 2 的幂次方，可以用 `(n - 1) & hash` 代替取模，降低计算成本，并让扩容后的元素迁移更高效。

## 线程安全边界
`HashMap` 不是线程安全容器，多线程并发写入可能导致数据覆盖、size 不准确等问题。JDK 1.7 及之前还常被提到扩容转移链表导致死循环的风险；JDK 1.8 结构变化后，线程不安全问题仍然存在。

## 遍历方式
常见遍历方式包括 `entrySet`、`keySet`、`forEach`、迭代器和流式遍历。通常需要同时访问 key 和 value 时，`entrySet` 更直接。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_HashTable与HashMap]]
- [[concepts/概念_HashMap与HashSet]]
- [[concepts/概念_ConcurrentHashMap]]
- [[concepts/概念_Object_equals与hashCode]]
