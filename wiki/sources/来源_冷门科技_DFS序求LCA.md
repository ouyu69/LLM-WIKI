---
type: "source"
tags: ["algorithm", "tree", "lca", "dfs", "rmq"]
summary: "介绍用 DFS 序 + ST 表求树上 LCA 的方法，并与欧拉序、倍增、树剖做常数与实现复杂度对比。"
sources: ["raw/已处理/冷门科技 —— DFS 序求 LCA.md"]
updated: "2026-04-24"
---

# 来源摘要：冷门科技 —— DFS 序求 LCA

## 来源信息
- 文件：`raw/已处理/冷门科技 —— DFS 序求 LCA.md`
- 来源站点：洛谷专栏
- 原始链接：`https://www.luogu.com.cn/article/pu52m9ue`
- 作者：Alex_Wei
- 主题范围：树上最近公共祖先（LCA）、DFS 序性质、ST 表区间最值建模

## 核心要点
- 文章主张使用 DFS 序而非欧拉序来做 LCA，认为其时间/空间常数更低，代码更简洁。
- 关键性质是祖先先于后代被 DFS 访问：若 x 是 y 的祖先，则 dfn(x) <= dfn(y)。
- 对查询点 u、v（设 dfn(u) < dfn(v)），当 u != v 时，可在区间 (dfn(u), dfn(v)] 上取深度最小结点，其父亲即为 LCA。
- 实现上可在 ST 表底层直接存“父亲结点”，比较函数按 DFS 序或深度规则选优，从而减少额外数组与常数开销。
- 与常见方案对比：相对欧拉序更省空间、预处理常数更小；相对倍增查询复杂度更优；相对树剖实现更轻量。

## 关联概念页
- [[concepts/概念_树上LCA_DFS序方法]]

## Ingest 状态
- 已按主题粒度完成 ingest；当前先建立核心方法页，后续可按需要拆分欧拉序/倍增/树剖对比专题。
