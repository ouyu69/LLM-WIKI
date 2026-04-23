---
type: "concept"
tags: ["java", "集合", "并发", "queue", "blockingqueue"]
summary: "BlockingQueue 为生产者-消费者模型提供阻塞式入队和出队能力，是线程池和并发协作的重要基础。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：BlockingQueue

## 定义
`BlockingQueue` 是阻塞队列接口：队列为空时，获取元素的线程可以阻塞等待；队列满时，插入元素的线程可以阻塞等待。

## 常见实现
- `ArrayBlockingQueue`：基于数组的有界阻塞队列，创建时通常需要指定容量。
- `LinkedBlockingQueue`：基于链表的阻塞队列，可有界也可近似无界，吞吐和内存风险需要结合容量配置判断。
- `PriorityBlockingQueue`：支持优先级排序的无界阻塞队列。
- `DelayQueue`：延迟队列，元素到期后才能被取出。
- `SynchronousQueue`：不存储元素，生产和消费直接交接。

## ArrayBlockingQueue 与 LinkedBlockingQueue
- `ArrayBlockingQueue` 容量固定，内存更可控，通常使用一把锁配合两个条件队列。
- `LinkedBlockingQueue` 链表节点分配成本更高，但生产和消费锁分离，某些场景吞吐更好。
- 使用 `LinkedBlockingQueue` 时应显式设置容量，避免无界队列导致内存堆积。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_Queue与Deque]]
- [[concepts/概念_Java线程池]]
