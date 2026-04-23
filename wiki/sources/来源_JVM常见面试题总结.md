---
type: "source"
tags: ["java", "jvm", "面试", "javaguide"]
summary: "JavaGuide JVM 面试题综述，覆盖运行时数据区、对象创建、GC、类加载与双亲委派、以及常用排查工具。"
sources: ["raw/已处理/JVM常见面试题总结.md"]
updated: "2026-04-23"
---

# 来源摘要：JVM常见面试题总结

## 来源信息
- 文件：`raw/已处理/JVM常见面试题总结.md`
- 来源站点：JavaGuide（JVM 面试专题）
- 原始链接：https://interview.javaguide.cn/java/java-jvm.html
- 主题范围：运行时数据区、对象创建与访问定位、垃圾回收、类加载与双亲委派、问题排查与性能工具。

## 核心要点
- 运行时数据区可按线程私有（程序计数器、虚拟机栈、本地方法栈）与线程共享（堆、方法区）理解；直接内存不属于运行时数据区，但与 NIO/内存占用密切相关。
- 程序计数器是规范意义上唯一不会出现 `OutOfMemoryError` 的区域；栈常见异常为 `StackOverflowError` 与（可扩展栈下的）`OutOfMemoryError`。
- 堆是对象实例主要分配区域（“几乎所有对象”），分代思想用于提高回收效率；PermGen 在 JDK 8 被 Metaspace（元空间，本地内存）替代。
- 对象创建涉及类加载检查、内存分配（指针碰撞/空闲列表）、初始化等过程；对象访问定位常见为句柄与直接指针两类。
- 存活判定常用可达性分析（GC Roots）与引用类型（强/软/弱/虚）理解；`finalize` 相关机制应尽量避免依赖。
- 常见 GC 算法包括标记-清除、复制、标记-整理、分代收集；收集器演进关注吞吐与停顿权衡，G1 以 Region + 价值优先回收为核心；ZGC 以更短暂停顿为目标。
- 双亲委派模型强调“先委托父加载器再自我加载”，用于避免核心类被篡改与重复加载；在容器与框架场景会借助线程上下文类加载器等机制实现“打破”。
- 问题排查常用 `jps/jstat/jinfo/jmap/jstack/jcmd` 与可视化工具（如 VisualVM、MAT）定位 OOM、死锁与 GC 异常，并结合 JVM 参数与 Heap Dump 分析。

## 关联概念页
- [[concepts/概念_JVM运行时数据区_内存区域]]
- [[concepts/概念_JVM对象创建与访问定位]]
- [[concepts/概念_JVM垃圾回收_存活判定_引用类型]]
- [[concepts/概念_JVM垃圾回收算法与收集器_G1_ZGC]]
- [[concepts/概念_类加载机制与双亲委派模型]]
- [[concepts/概念_JVM问题排查与性能工具]]
- [[concepts/概念_JVM_JDK_JRE与字节码]]

## Ingest 状态
- 已按 JVM 核心主题完成 ingest；未逐题拆页，避免产生过碎页面。

