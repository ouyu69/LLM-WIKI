## [2026-04-21] ingest | raw/已处理/未命名.md -> wiki/sources/来源_未命名_Java基础要点.md (+ concepts)

- 新建来源页：[[sources/来源_未命名_Java基础要点]]
- 新建概念页：
	- [[concepts/概念_字符串类型_String_StringBuffer_StringBuilder]]
	- [[concepts/概念_自动装箱与拆箱]]
	- [[concepts/概念_面向对象三大特征]]
	- [[concepts/概念_类型转换_向上转型与向下转型]]
	- [[concepts/概念_抽象类与接口]]
	- [[concepts/概念_值传递与引用传递]]
	- [[concepts/概念_Java反射]]
	- [[concepts/概念_HashTable与HashMap]]

## [2026-04-21] ingest | raw/已处理/Java并发常见面试题总结.md -> wiki/sources/来源_Java并发常见面试题总结.md (+ concepts)

- 新建来源页：[[sources/来源_Java并发常见面试题总结]]
- 新建概念页：
	- [[concepts/概念_并发与并行_同步与异步]]
	- [[concepts/概念_线程与进程]]
	- [[concepts/概念_Java线程生命周期与状态]]
	- [[concepts/概念_线程上下文切换]]
	- [[concepts/概念_sleep与wait对比]]
	- [[concepts/概念_start与run的区别]]
	- [[concepts/概念_多线程收益与适用边界]]
	- [[concepts/概念_死锁定义检测与规避]]

- 说明：当次 ingest 覆盖到原文的并发基础与死锁部分；JMM 及后续章节已在 2026-04-23 重新 ingest 中补齐。

## [2026-04-23] ingest | raw/* -> wiki/sources/* (+ concepts, overview, comparisons)

- 重新 ingest `raw/已处理/未命名.md`：保留并索引 Java 基础来源页与概念页。
- 重新 ingest `raw/已处理/Java并发常见面试题总结.md`：补齐 JMM/volatile、锁体系、ThreadLocal、线程池、Future/CompletableFuture、AQS、虚拟线程等后续主题页。
- 首次 ingest `raw/已处理/OpenClaw橙皮书_extracted.txt`：
	- [[sources/来源_OpenClaw橙皮书]]
	- [[overview/主题_OpenClaw总览]]
	- [[concepts/概念_OpenClaw架构]]
	- [[concepts/概念_OpenClaw记忆系统]]
	- [[concepts/概念_OpenClaw部署与渠道接入]]
	- [[concepts/概念_OpenClaw_Skills系统]]
	- [[concepts/概念_OpenClaw模型配置]]
	- [[concepts/概念_OpenClaw安全与成本]]
	- [[concepts/概念_OpenClaw生态与国内产品]]
	- [[comparisons/OpenClaw_vs_Claude_Code]]
- 更新 [[index]]，修正死锁概念页的旧错误链接。

## [2026-04-23] ingest | raw/已处理/Java基础常见面试题总结.md -> wiki/sources/来源_Java基础常见面试题总结.md (+ concepts)

- 新建来源页：[[sources/来源_Java基础常见面试题总结]]
- 新建概念页：
	- [[concepts/概念_JVM_JDK_JRE与字节码]]
	- [[concepts/概念_Java基本数据类型与包装类型]]
	- [[concepts/概念_Java方法重载与重写]]
	- [[concepts/概念_Object_equals与hashCode]]
	- [[concepts/概念_Java异常体系]]
	- [[concepts/概念_Java泛型]]
	- [[concepts/概念_Java动态代理]]
	- [[concepts/概念_Java注解与SPI]]
	- [[concepts/概念_Java序列化]]
	- [[concepts/概念_Java_IO模型]]
- 更新已有基础概念页，补充 `Java基础常见面试题总结` 作为更完整来源。
- 整理 `raw/`：按已处理/未处理文件夹归类原始资料，未修改原文内容。

## [2026-04-23] ingest | raw/未处理/Java集合常见面试题总结.md -> wiki/sources/来源_Java集合常见面试题总结.md (+ concepts)

- 新建来源页：[[sources/来源_Java集合常见面试题总结]]
- 新建概念页：
	- [[concepts/概念_Java集合框架]]
	- [[concepts/概念_ArrayList与LinkedList]]
	- [[concepts/概念_Java集合迭代_fail-fast与fail-safe]]
	- [[concepts/概念_Comparable与Comparator]]
	- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]]
	- [[concepts/概念_Queue与Deque]]
	- [[concepts/概念_BlockingQueue]]
	- [[concepts/概念_HashMap底层实现]]
	- [[concepts/概念_HashMap与HashSet]]
	- [[concepts/概念_ConcurrentHashMap]]
- 更新已有概念页：[[concepts/概念_HashTable与HashMap]]
- 更新 [[index]]，补充 Java 集合相关索引项。
- 整理 `raw/`：将 `raw/未处理/Java集合常见面试题总结.md` 归入 `raw/已处理/`，未修改原文内容。

## [2026-04-23] ingest | raw/未处理/JVM常见面试题总结.md -> wiki/sources/来源_JVM常见面试题总结.md (+ concepts)

- 新建来源页：[[sources/来源_JVM常见面试题总结]]
- 新建概念页：
	- [[concepts/概念_JVM运行时数据区_内存区域]]
	- [[concepts/概念_JVM对象创建与访问定位]]
	- [[concepts/概念_JVM垃圾回收_存活判定_引用类型]]
	- [[concepts/概念_JVM垃圾回收算法与收集器_G1_ZGC]]
	- [[concepts/概念_类加载机制与双亲委派模型]]
	- [[concepts/概念_JVM问题排查与性能工具]]
- 更新已有概念页：[[concepts/概念_JVM_JDK_JRE与字节码]]
- 更新 [[index]]，补充 JVM 相关索引项。
- 整理 `raw/`：将 `raw/未处理/JVM常见面试题总结.md` 归入 `raw/已处理/`，未修改原文内容。

## [2026-04-23] ingest | raw/未处理/MySQL常见面试题总结.md -> wiki/sources/来源_MySQL常见面试题总结.md (+ concepts)

- 新建来源页：[[sources/来源_MySQL常见面试题总结]]
- 新建概念页：
	- [[concepts/概念_MySQL基础与SQL]]
	- [[concepts/概念_MySQL字段类型设计]]
	- [[concepts/概念_MySQL存储引擎_InnoDB与MyISAM]]
	- [[concepts/概念_MySQL索引与最左前缀匹配]]
	- [[concepts/概念_MySQL日志_binlog_redo_undo]]
	- [[concepts/概念_MySQL事务隔离级别与MVCC]]
	- [[concepts/概念_MySQL锁机制_表锁行锁意向锁]]
	- [[concepts/概念_MySQL执行流程与EXPLAIN]]
	- [[concepts/概念_MySQL性能优化路径]]
- 更新 [[index]]，补充 MySQL 来源与 Database Concepts 索引项。
- 整理 `raw/`：已复制 `raw/未处理/MySQL常见面试题总结.md` 到 `raw/已处理/`，原文件因系统占用暂未删除，未修改原文内容。
