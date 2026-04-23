---
type: "concept"
tags: ["java", "jvm", "内存", "运行时数据区"]
summary: "运行时数据区可按线程私有与线程共享理解，核心关注堆、栈、方法区/元空间、常量池与直接内存的边界与常见 OOM。"
sources: ["raw/已处理/JVM常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：JVM 运行时数据区（内存区域）

## 组成（按线程共享性）
- 线程私有：程序计数器、虚拟机栈、本地方法栈
- 线程共享：堆、方法区
- 相关但不属于运行时数据区：直接内存（常与 NIO 相关）

## 常见错误与边界
- 程序计数器：规范意义上唯一不会出现 `OutOfMemoryError` 的区域。
- 虚拟机栈：
  - 栈深度超限常见 `StackOverflowError`
  - 可扩展栈在扩展失败时可能 `OutOfMemoryError`
- 堆：常见 `OutOfMemoryError: Java heap space`、`GC Overhead Limit Exceeded` 等。
- 方法区 / 元空间：
  - JDK 8 起用 Metaspace（本地内存）替代 PermGen
  - 典型错误：`OutOfMemoryError: Metaspace`

## 常量池与直接内存
- 字符串常量池用于复用字符串对象与降低内存占用；JDK 7 起字符串常量池迁移到堆。
- 直接内存用于减少堆内存拷贝开销（如 NIO），但占用不可忽视，排查时需要纳入整体内存预算。

## 关联
- [[sources/来源_JVM常见面试题总结]]
- [[concepts/概念_JVM对象创建与访问定位]]

