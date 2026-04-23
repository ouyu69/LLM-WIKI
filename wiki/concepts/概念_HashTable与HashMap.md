---
type: "concept"
tags: ["java", "集合", "map", "hashtable", "hashmap"]
summary: "Hashtable 通过同步方法保证线程安全但并发性能低，HashMap 非线程安全但允许 null 且单线程性能更好。"
sources: ["raw/已处理/未命名.md", "raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：HashTable 与 HashMap

## 核心区别
- 线程安全：`Hashtable` 的公开方法大多使用 `synchronized`，是线程安全但粗粒度锁的实现；`HashMap` 默认不保证线程安全。
- `null` 支持：`HashMap` 允许一个 `null` key 和多个 `null` value；`Hashtable` 不允许 `null` key 或 value。
- 性能：无并发需求时，`HashMap` 通常因为没有同步开销而更快。
- 继承体系：`Hashtable` 是较早期的遗留类；现代代码中非并发场景优先 `HashMap`，并发场景优先 `ConcurrentHashMap`。

## 与 ConcurrentHashMap 的关系
如果需要线程安全 Map，不建议简单使用 `Hashtable`。`ConcurrentHashMap` 通过更细粒度的并发控制降低锁竞争，在高并发场景下通常更合适。

## 关联
- [[sources/来源_未命名_Java基础要点]]
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_HashMap底层实现]]
- [[concepts/概念_ConcurrentHashMap]]
