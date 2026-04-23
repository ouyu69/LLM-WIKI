---
type: "concept"
tags: ["java", "集合", "queue", "deque"]
summary: "Queue 表达队列语义，Deque 支持双端插入和删除，ArrayDeque 通常是栈/队列场景的优先实现。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Queue 与 Deque

## 定义
- `Queue`：队列接口，通常按特定排队规则处理元素。
- `Deque`：双端队列接口，允许在队头和队尾进行插入、删除和查看。

## 常见实现
- `ArrayDeque`：基于可扩容数组，内存局部性好，通常比 `LinkedList` 更适合作为普通栈或队列。
- `LinkedList`：同时实现 `List` 和 `Deque`，但节点对象带来额外内存开销。
- `PriorityQueue`：优先级队列，按自然顺序或比较器确定出队顺序，不保证普通 FIFO。

## 选型建议
- 栈或普通双端队列：优先 `ArrayDeque`。
- 优先级调度：选择 `PriorityQueue`。
- 生产者-消费者阻塞模型：选择 `BlockingQueue` 体系。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_ArrayList与LinkedList]]
- [[concepts/概念_BlockingQueue]]
