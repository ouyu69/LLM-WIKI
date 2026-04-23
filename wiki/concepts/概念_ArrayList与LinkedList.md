---
type: "concept"
tags: ["java", "集合", "list", "arraylist", "linkedlist"]
summary: "ArrayList 基于动态数组，适合随机访问；LinkedList 基于双向链表，头尾操作成本低但随机访问慢。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：ArrayList 与 LinkedList

## 核心区别
- `ArrayList` 底层是动态数组，支持 O(1) 随机访问，但中间插入/删除通常需要移动元素。
- `LinkedList` 底层是双向链表，头尾插入/删除为 O(1)，但按索引访问或在指定位置操作需要先遍历。
- 二者默认都不是线程安全集合。

## ArrayList 特点
- 可以存储 `null`，但实际业务中通常不建议放入无语义的 `null`。
- 尾部追加在未扩容时近似 O(1)，扩容时需要复制数组，单次为 O(n)。
- 相比原生数组，`ArrayList` 支持泛型和动态扩容，但只能存储对象，基本类型需要使用包装类型。
- 实现了 `RandomAccess` 标记接口，适合基于索引高频读取。

## LinkedList 特点
- 不实现 `RandomAccess`，按索引访问需要从头或尾遍历。
- 每个节点需要额外保存前驱、后继指针，内存占用通常高于数组结构。
- 不应简单认为链表一定更适合增删；只有头尾操作优势明显，指定位置增删仍需遍历。

## 选型建议
- 大多数业务列表优先选择 `ArrayList`。
- 需要频繁头尾入队/出队时，优先考虑 `ArrayDeque`，而不是默认选择 `LinkedList`。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_Java集合框架]]
- [[concepts/概念_Queue与Deque]]
