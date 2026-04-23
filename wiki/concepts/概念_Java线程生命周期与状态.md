---
type: "concept"
tags: ["java", "线程", "生命周期"]
summary: "Java 线程具备六种官方状态，状态迁移受锁、等待、超时与调度影响。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-21"
---

# 概念：Java 线程生命周期与状态

## 六种状态
- NEW
- RUNNABLE
- BLOCKED
- WAITING
- TIMED_WAITING
- TERMINATED

## 关键理解
- JVM 视角中 RUNNABLE 覆盖了操作系统层的 ready/running。
- 进入 `synchronized` 竞争失败会进入 BLOCKED。
- `wait()` 进入 WAITING，`sleep(timeout)`/`wait(timeout)` 进入 TIMED_WAITING。

## 关联
- [[sources/来源_Java并发常见面试题总结]]
