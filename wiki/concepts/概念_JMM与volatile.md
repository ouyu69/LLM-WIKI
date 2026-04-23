---
type: "concept"
tags: ["java", "并发", "jmm", "volatile", "面试"]
summary: "JMM 定义跨线程可见性和有序性规则，volatile 保证可见性和禁止特定重排序，但不保证复合操作原子性。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：JMM 与 volatile

## 定义
JMM（Java Memory Model，Java 内存模型）定义线程如何通过主内存和工作内存交互，以及一个线程的写入何时对另一个线程可见。

## 核心问题
- 可见性：一个线程修改共享变量后，其他线程能否及时看到。
- 有序性：编译器、处理器可能进行指令重排序，JMM 通过 happens-before 等规则约束重排序结果。
- 原子性：单个读写可视为原子，但 `i++` 这类复合操作不是原子操作。

## volatile 的作用
- 保证可见性：写入 volatile 变量会刷新到主内存，读取 volatile 变量会从主内存获取最新值。
- 禁止特定指令重排序：通过内存屏障约束 volatile 读写前后的执行顺序。
- 不保证复合操作原子性：`volatile int count; count++` 仍然可能发生竞态。

## 使用边界
适合状态标记、一次性发布、双重检查锁定中的实例引用等场景；不适合需要复合读改写一致性的计数器，后者应使用锁或原子类。

## 关联
- [[sources/来源_Java并发常见面试题总结]]
- [[concepts/概念_Java锁体系_synchronized_ReentrantLock_读写锁]]
- [[concepts/概念_AQS同步器]]
