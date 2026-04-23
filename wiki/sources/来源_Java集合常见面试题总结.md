---
type: "source"
tags: ["java", "集合", "面试", "javaguide"]
summary: "JavaGuide Java 集合面试题综述，覆盖集合框架、List/Set/Queue/Map、HashMap 与 ConcurrentHashMap。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 来源摘要：Java集合常见面试题总结

## 来源信息
- 文件：`raw/已处理/Java集合常见面试题总结.md`
- 来源站点：JavaGuide（Java 集合面试专题）
- 原始链接：https://interview.javaguide.cn/java/java-collection.html
- 主题范围：Java 集合框架、常见容器实现、哈希容器、并发容器与集合迭代行为。

## 核心要点
- Java 集合主要由 `Collection` 与 `Map` 两大接口派生，`Collection` 下包含 `List`、`Set`、`Queue` 等常见子接口。
- `List` 强调有序和可重复，`Set` 强调唯一性，`Queue` 强调排队语义，`Map` 使用 key-value 存储并通过 key 定位 value。
- `ArrayList` 底层基于动态数组，随机访问快但中间插入/删除需要移动元素；`LinkedList` 基于双向链表，头尾操作成本低，但随机访问需要遍历。
- `RandomAccess` 是标记接口，用于提示集合支持高效随机访问；`ArrayList` 支持，`LinkedList` 不支持。
- `fail-fast` 通过 `modCount` 与迭代器期望修改次数检测并发结构性修改；`fail-safe` 通常基于副本或弱一致视图避免直接抛出并发修改异常。
- `Comparable` 定义对象的自然排序，`Comparator` 用于外部定制排序。
- `HashSet`、`LinkedHashSet`、`TreeSet` 都保证元素唯一，但分别强调哈希性能、插入顺序/访问顺序、排序能力。
- `Queue` 与 `Deque` 分别表达单端队列和双端队列语义；`ArrayDeque` 通常比 `LinkedList` 更适合作为栈或队列。
- `BlockingQueue` 为生产者-消费者模型提供阻塞式入队/出队能力，常见实现包括 `ArrayBlockingQueue`、`LinkedBlockingQueue`、`PriorityBlockingQueue` 等。
- `HashMap` 在 JDK 1.8 后采用数组 + 链表/红黑树结构，容量使用 2 的幂便于通过位运算定位桶。
- `HashMap` 不是线程安全容器，多线程写入可能出现数据覆盖、size 失真等问题。
- `ConcurrentHashMap` 在 JDK 1.7 使用 Segment 分段锁，在 JDK 1.8 使用 Node 数组、CAS 与 `synchronized` 降低锁粒度。
- `ConcurrentHashMap` 的单个基本操作线程安全，但复合操作应优先使用 `putIfAbsent`、`computeIfAbsent`、`merge` 等原子复合方法。

## 关联概念页
- [[concepts/概念_Java集合框架]]
- [[concepts/概念_ArrayList与LinkedList]]
- [[concepts/概念_Java集合迭代_fail-fast与fail-safe]]
- [[concepts/概念_Comparable与Comparator]]
- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]]
- [[concepts/概念_Queue与Deque]]
- [[concepts/概念_BlockingQueue]]
- [[concepts/概念_HashMap底层实现]]
- [[concepts/概念_HashMap与HashSet]]
- [[concepts/概念_HashTable与HashMap]]
- [[concepts/概念_ConcurrentHashMap]]

## Ingest 状态
- 已按集合核心主题完成 ingest；未逐题拆页，避免产生过碎页面。
