---
type: "concept"
tags: ["java", "jvm", "排查", "性能", "dump"]
summary: "JVM 排查常用 jps/jstat/jinfo/jstack/jmap/jcmd 与可视化工具（VisualVM、MAT），围绕 OOM、死锁与 GC 异常定位根因。"
sources: ["raw/已处理/JVM常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：JVM 问题排查与性能工具

## 常用命令（速记）
- `jps`：查看 Java 进程列表（`jps -l` / `jps -v` 常用于确认启动参数与主类）。
- `jstat`：采集 JVM 运行数据（如 GC 相关统计）。
- `jinfo`：查看/修改（部分）JVM 配置信息。
- `jstack`：打印线程栈，定位死锁、阻塞与热点线程。
- `jmap`：生成堆转储（高版本 JDK 中更推荐用 `jcmd` 替代直接 `jmap`）。
- `jcmd`：多功能命令入口，可生成 heap dump、触发诊断命令等。

## Heap Dump（堆转储）
Heap Dump 是某一时刻堆内存快照，常用于定位内存泄漏、异常对象占用与 OOM 根因。生成方式通常包括：
- OOM 自动生成：通过 JVM 参数在发生 `OutOfMemoryError` 时落盘 dump。
- 手动生成：通过 `jcmd <pid> GC.heap_dump <path>` 等方式生成。
- 图形化工具：VisualVM、YourKit、JProfiler 等。

## 排查路径（实践化）
- OOM：先确认堆/元空间/直接内存的预算与参数，再结合 GC 日志与 Heap Dump 分析“泄漏 vs 膨胀”。
- 死锁：用 `jstack` 或相关工具检测，关注输出中的死锁提示与线程持锁关系。
- GC 异常：用 `jstat` + GC 日志判断频率、停顿与晋升失败等问题，必要时结合采样/剖析工具定位分配热点。

## 关联
- [[sources/来源_JVM常见面试题总结]]
- [[concepts/概念_JVM运行时数据区_内存区域]]
- [[concepts/概念_JVM垃圾回收算法与收集器_G1_ZGC]]

