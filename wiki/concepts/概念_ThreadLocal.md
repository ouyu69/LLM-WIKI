---
type: "concept"
tags: ["java", "并发", "threadlocal", "内存泄露"]
summary: "ThreadLocal 为每个线程保存独立变量副本，适合线程上下文传递，但在线程池中必须及时清理。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：ThreadLocal

## 定义
`ThreadLocal` 让每个线程访问同一个变量名时拿到自己的独立副本，常用于保存用户上下文、请求 ID、数据库连接上下文等线程内状态。

## 原理
每个线程内部维护 `ThreadLocalMap`，key 是 `ThreadLocal` 弱引用，value 是线程局部变量值。调用 `get/set/remove` 时，实际操作的是当前线程自己的 map。

## 内存泄露风险
`ThreadLocalMap` 的 key 是弱引用，但 value 是强引用。在线程池中线程长期存活，如果 `ThreadLocal` key 被回收而 value 未清理，就可能形成残留 value，导致内存泄露或上下文串扰。

## 实践建议
- 在线程池任务结束时在 `finally` 中调用 `remove()`。
- 不要把大对象或敏感凭证长期放入 ThreadLocal。
- 跨线程传递上下文时不要假设 ThreadLocal 自动传播，可使用显式参数、任务包装器或专门的传递型 ThreadLocal 工具。

## 关联
- [[concepts/概念_Java线程池]]
- [[concepts/概念_线程与进程]]
