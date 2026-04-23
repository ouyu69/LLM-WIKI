---
type: "source"
tags: ["java", "并发", "面试", "javaguide"]
summary: "Java 并发高频面试题综述，覆盖线程/进程、线程状态、JMM、锁、ThreadLocal、线程池、Future、AQS 与虚拟线程。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 来源摘要：Java并发常见面试题总结

## 来源信息
- 文件：`raw/已处理/Java并发常见面试题总结.md`
- 来源站点：JavaGuide（面试突击版并发专题）
- 主题范围：并发基础、线程模型、调度、JMM、锁、ThreadLocal、线程池、Future、AQS、虚拟线程

## 核心要点
- Java 线程本质上是操作系统内核线程，主流系统采用一对一模型。
- 线程是轻量级执行单元，同进程线程共享堆与方法区，但拥有独立程序计数器与栈。
- 线程生命周期含 NEW、RUNNABLE、BLOCKED、WAITING、TIMED_WAITING、TERMINATED 六态。
- `start()` 才会真正启动并发执行，直接调用 `run()` 只是普通方法调用。
- `sleep()` 不释放锁，`wait()` 释放锁并需配合 `notify/notifyAll`。
- 多线程收益取决于任务类型：IO 密集型更易受益，单核下 CPU 密集型线程过多会降低效率。
- 死锁由互斥、请求保持、不剥夺、循环等待四条件共同触发；可通过资源有序申请等方式规避。
- 死锁排查可借助 `jstack`、`jmap`、JConsole、VisualVM 等工具。
- JMM 用 happens-before 约束跨线程可见性与有序性；`volatile` 能保证可见性和禁止特定重排序，但不能保证复合操作原子性。
- Java 锁体系包括 `synchronized`、`ReentrantLock`、读写锁以及 AQS 上层同步器；选择时需关注可中断、公平性、条件队列与读多写少场景。
- `ThreadLocal` 适合保存线程上下文，但在线程池中必须及时 `remove()`，否则可能因弱引用 key 与强引用 value 组合产生内存泄露。
- 线程池复用线程以降低创建销毁成本，但必须显式配置参数、队列、拒绝策略与线程名，避免无界队列和不可控资源耗尽。
- `CompletableFuture` 支持任务依赖、组合和异常处理；生产环境应提供自定义线程池，避免占用公共 ForkJoinPool。
- AQS 以 `state` 和 CLH 变体队列为核心，支撑 `ReentrantLock`、`Semaphore`、`CountDownLatch` 等同步器。
- Java 21 虚拟线程适合高并发 IO 阻塞任务，但不等于提升 CPU 密集型任务吞吐。

## 关联概念页
- [[concepts/概念_并发与并行_同步与异步]]
- [[concepts/概念_线程与进程]]
- [[concepts/概念_Java线程生命周期与状态]]
- [[concepts/概念_线程上下文切换]]
- [[concepts/概念_sleep与wait对比]]
- [[concepts/概念_start与run的区别]]
- [[concepts/概念_多线程收益与适用边界]]
- [[concepts/概念_死锁定义检测与规避]]
- [[concepts/概念_JMM与volatile]]
- [[concepts/概念_Java锁体系_synchronized_ReentrantLock_读写锁]]
- [[concepts/概念_ThreadLocal]]
- [[concepts/概念_Java线程池]]
- [[concepts/概念_Future与CompletableFuture]]
- [[concepts/概念_AQS同步器]]
- [[concepts/概念_Java虚拟线程]]

## Ingest 状态
- 已按主题粒度完成重新 ingest；未逐题拆页，避免产生过碎的低价值知识页。
