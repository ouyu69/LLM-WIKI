---
type: "concept"
tags: ["java", "并发", "锁", "synchronized", "reentrantlock"]
summary: "Java 常见锁包括 synchronized、ReentrantLock 和 ReentrantReadWriteLock，分别在语法、能力和适用场景上有差异。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 锁体系

## synchronized
`synchronized` 是 JVM 层面的内置锁，可修饰实例方法、静态方法或代码块。它保证互斥、可见性和有序性，异常退出时会自动释放锁。

## ReentrantLock
`ReentrantLock` 是 `java.util.concurrent.locks` 中的显式可重入锁，基于 AQS 实现。它相比 `synchronized` 提供可中断获取、超时获取、公平锁选项和多个 `Condition` 条件队列。

## ReentrantReadWriteLock
读写锁将共享访问拆成读锁和写锁，适合读多写少场景。多个读线程可并发持有读锁，写锁独占。读锁通常不能升级为写锁，否则容易造成死锁；写锁可以降级为读锁。

## 锁优化
JDK 1.6 后 `synchronized` 做过锁优化，如轻量级锁、重量级锁等路径。偏向锁曾用于降低无竞争场景成本，但后续版本中逐步废弃。

## 选择建议
- 简单互斥优先用 `synchronized`，语义清楚且自动释放。
- 需要可中断、超时、公平性或多个条件队列时用 `ReentrantLock`。
- 读多写少且读操作耗时明显时考虑读写锁。
- 高频计数和无锁更新优先考虑原子类或并发容器。

## 关联
- [[concepts/概念_JMM与volatile]]
- [[concepts/概念_AQS同步器]]
- [[concepts/概念_死锁定义检测与规避]]
