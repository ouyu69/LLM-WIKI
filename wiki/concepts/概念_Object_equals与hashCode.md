---
type: "concept"
tags: ["java", "object", "equals", "hashcode", "集合"]
summary: "equals 定义对象逻辑相等，hashCode 为哈希容器提供分桶依据；重写 equals 时必须同步重写 hashCode。"
sources: ["raw/已处理/Java基础常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Object、equals 与 hashCode

## Object 常见方法
`Object` 是 Java 类体系的根类，常见方法包括 `equals()`、`hashCode()`、`toString()`、`getClass()`、`clone()`、`wait()`、`notify()`、`notifyAll()`。

## equals 与 ==
- `==`：对基本类型比较值，对引用类型比较对象地址。
- 默认 `equals()`：未重写时等价于引用比较。
- 重写 `equals()`：通常用于按业务字段判断两个对象是否逻辑相等。

## hashCode 约定
- 如果两个对象通过 `equals()` 判断相等，它们的 `hashCode()` 必须相同。
- 如果两个对象 `hashCode()` 相同，它们不一定 `equals()` 相等，可能只是哈希冲突。
- 哈希容器如 `HashMap`、`HashSet` 依赖 `hashCode()` 快速定位桶，再用 `equals()` 做精确比较。

## 实践建议
- 重写 `equals()` 时必须重写 `hashCode()`。
- 用作哈希集合 key 的字段应尽量不可变，避免放入集合后哈希值变化导致查找失败。

## 关联
- [[concepts/概念_HashTable与HashMap]]
- [[sources/来源_Java基础常见面试题总结]]
