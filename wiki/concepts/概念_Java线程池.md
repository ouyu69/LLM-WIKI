---
type: "concept"
tags: ["java", "并发", "线程池", "executor"]
summary: "线程池通过复用线程降低开销，但需要明确核心参数、队列、拒绝策略、线程命名和动态调参方案。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 线程池

## 定义
线程池复用已创建线程执行任务，避免频繁创建和销毁线程，同时通过队列、线程数和拒绝策略控制并发压力。

## 核心参数
- `corePoolSize`：核心线程数。
- `maximumPoolSize`：最大线程数。
- `keepAliveTime`：非核心线程空闲存活时间，也可配置核心线程超时回收。
- `workQueue`：任务阻塞队列。
- `threadFactory`：线程创建工厂，生产环境应命名线程并设置异常处理。
- `handler`：拒绝策略。

## 执行流程
当任务提交后，线程池优先创建核心线程；核心线程满后进入队列；队列满后创建非核心线程；达到最大线程数后触发拒绝策略。

## 为什么不推荐内置线程池
`Executors` 的部分工厂方法会使用无界队列或过大的最大线程数，可能隐藏资源耗尽风险。生产环境更推荐显式创建 `ThreadPoolExecutor`。

## 拒绝策略
常见策略包括 AbortPolicy、CallerRunsPolicy、DiscardPolicy、DiscardOldestPolicy。若不允许丢任务，需要结合持久化队列、降级、限流或调用方回退策略设计，而不是简单依赖内置策略。

## 关联
- [[concepts/概念_ThreadLocal]]
- [[concepts/概念_Future与CompletableFuture]]
- [[concepts/概念_多线程收益与适用边界]]
