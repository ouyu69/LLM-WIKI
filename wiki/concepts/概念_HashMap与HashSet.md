---
type: "concept"
tags: ["java", "集合", "hashmap", "hashset"]
summary: "HashSet 通常基于 HashMap 实现，只存储元素本身；HashMap 存储 key-value 映射。"
sources: ["raw/已处理/Java集合常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：HashMap 与 HashSet

## 核心区别
- `HashMap` 实现 `Map`，存储 key-value 映射。
- `HashSet` 实现 `Set`，存储不可重复元素。
- `HashSet` 底层通常借助 `HashMap`，元素作为 key，value 使用固定占位对象。

## 判重机制
二者都依赖哈希语义：
- 先通过 `hashCode()` 定位哈希桶。
- 再通过 `equals()` 判断 key 或元素是否逻辑相等。

## 使用建议
- 需要通过 key 查找 value：使用 `HashMap`。
- 只关心元素是否存在或需要去重：使用 `HashSet`。
- 作为 key 或 set 元素的对象，应保持参与 `equals()` / `hashCode()` 的字段稳定。

## 关联
- [[sources/来源_Java集合常见面试题总结]]
- [[concepts/概念_HashMap底层实现]]
- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]]
- [[concepts/概念_Object_equals与hashCode]]
