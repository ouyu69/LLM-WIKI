---
type: "concept"
tags: ["java", "集合", "iterator", "fail-fast", "fail-safe"]
summary: "fail-fast 迭代器尽早暴露结构性并发修改，fail-safe 迭代通常基于副本或弱一致视图降低冲突。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 集合迭代 fail-fast 与 fail-safe

## fail-fast
`fail-fast` 是快速失败机制，常见于 `java.util` 包下的非线程安全集合迭代器。集合在结构性修改时维护 `modCount`，迭代器保存 `expectedModCount`；迭代过程中二者不一致时通常抛出 `ConcurrentModificationException`。

## fail-safe
`fail-safe` 更偏向“迭代期间不直接失败”的行为，常见实现会基于副本或弱一致视图进行迭代，例如并发集合中的某些迭代器不会因为遍历期间集合变化而立即抛出并发修改异常。

## 使用边界
- `fail-fast` 不是线程安全保证，只是尽早暴露错误使用方式。
- 遍历时需要删除元素，应使用迭代器自身的 `remove()`，不要直接调用集合的结构性修改方法。
- 并发读写场景应选择合适的并发集合或外部同步策略。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_ArrayList与LinkedList]]
- [[concepts/概念_ConcurrentHashMap]]
