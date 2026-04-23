---
type: "concept"
tags: ["java", "并发", "aqs", "semaphore", "countdownlatch", "cyclicbarrier"]
summary: "AQS 通过 state 和 CLH 变体队列抽象同步器实现，是 ReentrantLock、Semaphore、CountDownLatch 等组件的基础。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：AQS 同步器

## 定义
AQS（`AbstractQueuedSynchronizer`）是 Java 并发包中的同步器基础框架，通过一个 `volatile int state` 表示同步状态，并用 CLH 变体队列管理等待线程。

## 核心机制
当共享资源空闲时，线程通过 CAS 修改 `state` 获取资源；如果资源不可用，线程会进入等待队列并被阻塞，待前驱释放资源后再被唤醒竞争。

## 常见同步器
- `ReentrantLock`：独占锁，`state` 表示重入次数。
- `Semaphore`：共享锁，`state` 表示可用许可证数量。
- `CountDownLatch`：一次性倒计时门闩，`state` 递减到 0 后释放等待线程。
- `CyclicBarrier`：循环屏障，基于 `ReentrantLock` 和 `Condition` 实现线程汇合。

## 理解重点
AQS 不直接定义业务锁语义，而是抽象出排队、阻塞、唤醒、状态变更的通用流程；具体同步器通过重写模板方法定义“如何获取/释放资源”。

## 关联
- [[concepts/概念_Java锁体系_synchronized_ReentrantLock_读写锁]]
- [[concepts/概念_Future与CompletableFuture]]
