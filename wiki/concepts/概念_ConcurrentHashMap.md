---
type: "concept"
tags: ["java", "集合", "并发", "map", "concurrenthashmap"]
summary: "ConcurrentHashMap 是高并发场景下的线程安全哈希表，JDK 1.8 后主要依赖 CAS 与 synchronized 控制桶级并发。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：ConcurrentHashMap

## 定位
`ConcurrentHashMap` 是线程安全的哈希表实现，适合多线程共享读写 Map 的场景。它避免了 `Hashtable` 粗粒度同步带来的严重竞争。

## JDK 1.7 与 JDK 1.8 差异
- JDK 1.7：使用 `Segment` 分段锁，最大并发度受 Segment 数量影响。
- JDK 1.8：取消分段锁主体设计，使用 `Node` 数组 + 链表/红黑树，并通过 CAS 与 `synchronized` 控制并发。
- JDK 1.8 锁粒度更细，通常只锁定当前桶的链表或树结构首节点。

## null 限制
`ConcurrentHashMap` 不允许 key 或 value 为 `null`，核心原因是避免并发环境下 `get()` 返回 `null` 时无法区分“不存在 key”与“存在 key 但 value 为 null”的二义性。

## 复合操作原子性
`ConcurrentHashMap` 保证单个基本操作的线程安全，但不自动保证“先判断再写入”等复合逻辑的原子性。需要使用：
- `putIfAbsent`
- `compute`
- `computeIfAbsent`
- `computeIfPresent`
- `merge`

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_HashMap底层实现]]
- [[concepts/概念_HashTable与HashMap]]
- [[concepts/概念_Java集合迭代_fail-fast与fail-safe]]
