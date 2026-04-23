---
type: "source"
tags: ["java", "基础", "面试", "笔记"]
summary: "一份 Java 基础知识速记，覆盖字符串、装箱拆箱、OOP、类型转换、抽象类与接口等主题。"
sources: ["raw/已处理/未命名.md"]
updated: "2026-04-23"
---

# 来源摘要：未命名（Java 基础要点）

## 来源信息
- 文件：`raw/已处理/未命名.md`
- 形态：结构化学习笔记（含对比表与概念清单）
- 主题：Java 基础语法与面向对象核心概念

## 核心要点
- `String` 不可变，线程安全；`StringBuffer` 可变且线程安全；`StringBuilder` 可变但非线程安全。
- 自动装箱/拆箱是语法糖，频繁装箱会带来对象分配和 GC 压力，拆箱 `null` 会抛 `NullPointerException`。
- 面向对象三大特征：封装、继承、多态。
- 强制类型转换包含向上转型（隐式）与向下转型（显式）。
- 抽象类与接口在继承方式、构造器、字段与方法能力上有明确差异。
- 值传递与引用传递的区分在笔记中给出直观定义（注意 Java 语义需在概念页进一步澄清）。
- 反射与 `HashTable`/`HashMap` 在原笔记中仅作为占位主题出现，现已由后续 Java 基础与集合来源补齐。

## 关联概念页
- [[concepts/概念_字符串类型_String_StringBuffer_StringBuilder]]
- [[concepts/概念_自动装箱与拆箱]]
- [[concepts/概念_面向对象三大特征]]
- [[concepts/概念_类型转换_向上转型与向下转型]]
- [[concepts/概念_抽象类与接口]]
- [[concepts/概念_值传递与引用传递]]
- [[concepts/概念_Java反射]]
- [[concepts/概念_HashTable与HashMap]]

## 后续补齐状态
- 反射核心机制与典型使用场景已整理至 [[concepts/概念_Java反射]]。
- `HashTable` 与 `HashMap` 的差异维度已整理至 [[concepts/概念_HashTable与HashMap]]。
