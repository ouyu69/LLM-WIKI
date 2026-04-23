---
type: "concept"
tags: ["java", "集合", "排序", "comparable", "comparator"]
summary: "Comparable 定义类的自然排序，Comparator 在类外提供可替换的定制排序规则。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Comparable 与 Comparator

## 定义
- `Comparable<T>`：由被排序对象自身实现，通过 `compareTo()` 定义自然排序。
- `Comparator<T>`：由外部比较器实现，通过 `compare()` 定义定制排序。

## 使用场景
- 当类只有一种稳定、通用的默认排序规则时，可以实现 `Comparable`。
- 当排序规则依赖业务场景，或无法修改目标类源码时，使用 `Comparator` 更灵活。
- `TreeSet`、`TreeMap`、`Collections.sort()`、`List.sort()` 等排序能力都与比较规则密切相关。

## 注意点
- 比较逻辑应满足自反性、传递性和一致性，否则排序集合可能表现异常。
- 对排序集合而言，“相等”通常由比较结果是否为 0 决定，需要避免与 `equals()` 语义严重冲突。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]]
