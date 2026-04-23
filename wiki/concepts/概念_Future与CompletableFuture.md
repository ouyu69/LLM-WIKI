---
type: "concept"
tags: ["java", "并发", "future", "completablefuture"]
summary: "Future 表示异步任务结果，CompletableFuture 进一步支持任务编排、组合、回调和异常处理。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Future 与 CompletableFuture

## Future
`Future` 表示异步计算结果，常与 `Callable` 配合使用。`Callable` 负责返回结果或抛出异常，提交到线程池后得到 `Future`，再通过 `get()` 获取结果。

## CompletableFuture
`CompletableFuture` 在 Future 基础上支持异步任务编排，例如串行依赖、并行合并、任一完成、异常恢复和回调处理。

## 典型场景
- 一个任务依赖两个任务完成后再执行：可使用 `thenCombine`、`allOf` 等组合。
- 多个文件或接口并行处理后汇总：可收集多个 `CompletableFuture` 并用 `allOf` 等待。
- 任务失败处理：可使用 `exceptionally`、`handle`、`whenComplete` 等方法。

## 自定义线程池
生产环境使用 `CompletableFuture` 时应提供自定义线程池，避免大量业务任务占用公共 ForkJoinPool，导致隔离性差、资源不可控和异常难定位。

## 关联
- [[concepts/概念_Java线程池]]
- [[concepts/概念_AQS同步器]]
