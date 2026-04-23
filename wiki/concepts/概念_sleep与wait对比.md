---
type: "concept"
tags: ["java", "线程", "锁", "wait-notify"]
summary: "sleep 与 wait 都能暂停线程，但是否释放锁、归属类与唤醒机制完全不同。"
sources: ["raw/已处理/Java并发常见面试题总结.md"]
updated: "2026-04-21"
---

# 概念：sleep 与 wait 对比

## 共同点
- 都可让当前线程暂停执行。

## 差异
- `sleep()` 不释放锁，`wait()` 释放当前对象锁。
- `sleep()` 属于 `Thread`，`wait()` 属于 `Object`。
- `wait()` 依赖 `notify/notifyAll` 或超时恢复，`sleep()` 到时自动恢复可运行态。

## 设计原因
- `wait()` 本质是对象监视器协作机制。
- `sleep()` 本质是当前线程调度行为。

## 关联
- [[sources/来源_Java并发常见面试题总结]]
