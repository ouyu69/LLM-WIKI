---
type: "concept"
tags: ["java", "集合", "set", "hashset", "treeset"]
summary: "HashSet、LinkedHashSet、TreeSet 都保证元素唯一，但分别强调哈希性能、顺序保留和排序能力。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Set 实现：HashSet、LinkedHashSet、TreeSet

## 共同点
三者都实现 `Set` 语义，核心特征是元素不可重复，适合去重和成员存在性判断。

## 主要区别
- `HashSet`：底层依赖哈希结构，通常查询、添加、删除效率较高，但不保证迭代顺序。
- `LinkedHashSet`：在哈希结构基础上维护链表，能够保留插入顺序，成本略高于 `HashSet`。
- `TreeSet`：基于排序结构，元素按自然排序或比较器排序，操作复杂度通常为 O(log n)。

## HashSet 如何判重
`HashSet` 通常依赖 `HashMap` 实现，插入元素时先使用 `hashCode()` 定位桶，再使用 `equals()` 判断是否已有逻辑相等元素。

## 选型建议
- 只需要去重和快速查询：优先 `HashSet`。
- 需要稳定迭代顺序：选择 `LinkedHashSet`。
- 需要有序集合或范围相关能力：选择 `TreeSet`。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_Object_equals与hashCode]]
- [[concepts/概念_Comparable与Comparator]]
- [[concepts/概念_HashMap与HashSet]]
