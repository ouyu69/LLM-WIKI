---
type: "concept"
tags: ["java", "string", "并发"]
summary: "对比 String、StringBuffer、StringBuilder 在可变性、线程安全与性能上的差异。"
sources: ["raw/已处理/未命名.md", "raw/已处理/Java基础常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：String / StringBuffer / StringBuilder

## 定义
- `String`：不可变字符串。
- `StringBuffer`：可变字符串容器，方法通常带同步。
- `StringBuilder`：可变字符串容器，不保证线程安全。

## 对比
| 类型 | 是否可变 | 线程安全 | 性能特征 |
|---|---|---|---|
| String | 否 | 是（不可变对象天然安全） | 频繁拼接性能较差 |
| StringBuffer | 是 | 是 | 中等 |
| StringBuilder | 是 | 否 | 通常最好 |

## 使用建议
- 单线程且频繁拼接：优先 `StringBuilder`。
- 多线程共享可变字符串：考虑 `StringBuffer` 或外部同步。
- 常量与只读文本：使用 `String`。

## 关联
- [[sources/来源_未命名_Java基础要点]]
- [[sources/来源_Java基础常见面试题总结]]
