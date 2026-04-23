---
type: "concept"
tags: ["java", "异常", "error", "exception"]
summary: "Java 异常体系分为 Error 与 Exception；Exception 又分为受检查异常和不受检查异常，应按可恢复性和业务语义选择。"
sources: ["raw/已处理/Java基础常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 异常体系

## 分类
- `Error`：通常表示 JVM 或系统级严重问题，程序一般不建议捕获处理，例如 `OutOfMemoryError`。
- `Exception`：程序可处理的异常。
- Checked Exception：受检查异常，编译期要求显式 `catch` 或 `throws`。
- Unchecked Exception：不受检查异常，通常继承 `RuntimeException`，编译期不强制处理。

## try-catch-finally
- `try` 放置可能抛出异常的代码。
- `catch` 捕获并处理指定类型异常。
- `finally` 通常用于释放资源，多数情况下会执行，但 JVM 退出、线程被强制终止等极端场景除外。

## 使用建议
- 异常不应用于普通流程控制。
- 捕获异常时尽量保留上下文，避免吞掉异常。
- 业务可恢复且调用方必须处理的情况，可考虑 Checked Exception。
- 编程错误、参数非法、状态非法等场景更适合 Unchecked Exception。

## 关联
- [[sources/来源_Java基础常见面试题总结]]
