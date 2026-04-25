# Wiki Index

## Sources
- [[sources/来源_未命名_Java基础要点]] - Java 基础速记，覆盖字符串、装箱拆箱、OOP、类型转换、抽象类与接口。
- [[sources/来源_Java基础常见面试题总结]] - JavaGuide Java 基础面试题综述，覆盖 JVM、语法、OOP、核心类库、异常、泛型、反射、代理、注解、SPI、序列化与 I/O。
- [[sources/来源_Java并发常见面试题总结]] - JavaGuide 并发面试题综述，覆盖线程、JMM、锁、线程池、AQS 与虚拟线程。
- [[sources/来源_Java集合常见面试题总结]] - JavaGuide Java 集合面试题综述，覆盖集合框架、List/Set/Queue/Map、HashMap 与 ConcurrentHashMap。
- [[sources/来源_JVM常见面试题总结]] - JavaGuide JVM 面试题综述，覆盖运行时数据区、GC、类加载与双亲委派、以及常用排查工具。
- [[sources/来源_MySQL常见面试题总结]] - JavaGuide MySQL 面试题综述，覆盖基础、字段类型、存储引擎、索引、日志、事务、锁与性能优化。
- [[sources/来源_OpenClaw橙皮书]] - OpenClaw 橙皮书摘要，覆盖产品定位、架构、部署、渠道、Skills、模型、安全成本与生态。
- [[sources/来源_Obsidian_GitHub_Termux全平台同步工作流]] - Obsidian 全平台同步实践摘要，覆盖方案选型、Termux 原生 Git、一键脚本与 gitignore 治理。
- [[sources/来源_冷门科技_DFS序求LCA]] - 树上 LCA 的 DFS 序方法摘要，覆盖性质证明、ST 表实现与和欧拉序/倍增/树剖的对比。

## Java Concepts
- [[concepts/概念_JVM_JDK_JRE与字节码]] - JVM/JDK/JRE 边界、字节码、解释执行、JIT 与 AOT。
- [[concepts/概念_JVM运行时数据区_内存区域]] - 运行时数据区的线程私有/共享划分，堆/栈/方法区与常见 OOM。
- [[concepts/概念_JVM对象创建与访问定位]] - 对象创建流程与句柄/直接指针两种访问定位方式。
- [[concepts/概念_JVM垃圾回收_存活判定_引用类型]] - 可达性分析（GC Roots）与强/软/弱/虚引用。
- [[concepts/概念_JVM垃圾回收算法与收集器_G1_ZGC]] - GC 算法与收集器演进要点，G1 与 ZGC 的取舍。
- [[concepts/概念_类加载机制与双亲委派模型]] - 双亲委派的工作方式、价值与容器场景的“打破”。
- [[concepts/概念_JVM问题排查与性能工具]] - jps/jstat/jstack/jcmd/Heap Dump 与 OOM/死锁/GC 排查路径。
- [[concepts/概念_Java基本数据类型与包装类型]] - 基本类型、包装类型、缓存机制、浮点精度与大数表示。
- [[concepts/概念_字符串类型_String_StringBuffer_StringBuilder]] - 对比三类字符串实现的可变性、线程安全与性能。
- [[concepts/概念_自动装箱与拆箱]] - 说明装箱拆箱机制及性能、空指针风险。
- [[concepts/概念_面向对象三大特征]] - 概述封装、继承、多态。
- [[concepts/概念_Java方法重载与重写]] - 区分编译期重载与运行时重写/多态。
- [[concepts/概念_类型转换_向上转型与向下转型]] - 区分向上转型与向下转型及其风险。
- [[concepts/概念_抽象类与接口]] - 比较抽象类与接口的能力边界与使用场景。
- [[concepts/概念_值传递与引用传递]] - 澄清 Java 参数传递语义。
- [[concepts/概念_Object_equals与hashCode]] - Object 常见方法、equals/hashCode 约定与哈希容器影响。
- [[concepts/概念_Java异常体系]] - Error、Exception、Checked/Unchecked Exception 与异常使用建议。
- [[concepts/概念_Java泛型]] - 泛型类、接口、方法、类型安全与类型擦除。
- [[concepts/概念_Java反射]] - 反射机制、入口 API、典型场景与风险。
- [[concepts/概念_Java动态代理]] - JDK/CGLIB 动态代理及 AOP 场景。
- [[concepts/概念_Java注解与SPI]] - 注解解析方式、SPI 与 API 的扩展关系。
- [[concepts/概念_Java序列化]] - 序列化/反序列化、transient、协议选择与安全风险。
- [[concepts/概念_Java_IO模型]] - 字节流/字符流、BIO/NIO/AIO 与 I/O 设计模式。
- [[concepts/概念_Java集合框架]] - Collection 与 Map 两条集合体系及 List/Set/Queue/Map 的核心语义。
- [[concepts/概念_ArrayList与LinkedList]] - 动态数组与双向链表实现的访问、增删、内存和选型差异。
- [[concepts/概念_Java集合迭代_fail-fast与fail-safe]] - fail-fast 与 fail-safe 迭代行为、并发修改检测和使用边界。
- [[concepts/概念_Comparable与Comparator]] - 自然排序与外部定制排序规则的职责边界。
- [[concepts/概念_Set实现_HashSet_LinkedHashSet_TreeSet]] - HashSet、LinkedHashSet、TreeSet 的去重、顺序和排序差异。
- [[concepts/概念_Queue与Deque]] - Queue、Deque、ArrayDeque、LinkedList、PriorityQueue 的队列语义和选型。
- [[concepts/概念_BlockingQueue]] - 阻塞队列的生产者-消费者语义和常见实现。
- [[concepts/概念_HashMap底层实现]] - HashMap 的数组、链表/红黑树、2 的幂容量和线程安全边界。
- [[concepts/概念_HashMap与HashSet]] - HashMap 存储映射，HashSet 基于哈希语义存储唯一元素。
- [[concepts/概念_HashTable与HashMap]] - HashTable/HashMap 的线程安全、空值、性能差异。
- [[concepts/概念_ConcurrentHashMap]] - ConcurrentHashMap 的 JDK 1.7/1.8 实现差异、null 限制和原子复合操作。
- [[concepts/概念_并发与并行_同步与异步]] - 区分并发/并行与同步/异步。
- [[concepts/概念_线程与进程]] - 从资源隔离与共享角度理解线程与进程。
- [[concepts/概念_Java线程生命周期与状态]] - 归纳 Java 线程六种状态与常见迁移。
- [[concepts/概念_线程上下文切换]] - 解释切换触发条件与性能代价。
- [[concepts/概念_sleep与wait对比]] - 对比 sleep 和 wait 的锁语义与唤醒机制。
- [[concepts/概念_start与run的区别]] - 说明真正启动线程必须调用 start。
- [[concepts/概念_多线程收益与适用边界]] - 总结多线程收益条件与常见误区。
- [[concepts/概念_死锁定义检测与规避]] - 死锁四条件、检测方法与规避策略。
- [[concepts/概念_JMM与volatile]] - Java 内存模型、可见性、有序性与 volatile 边界。
- [[concepts/概念_Java锁体系_synchronized_ReentrantLock_读写锁]] - synchronized、ReentrantLock、读写锁与锁优化。
- [[concepts/概念_ThreadLocal]] - ThreadLocal 原理、内存泄露与跨线程传递。
- [[concepts/概念_Java线程池]] - 线程池参数、拒绝策略、执行流程与调参。
- [[concepts/概念_Future与CompletableFuture]] - Future、Callable、CompletableFuture 编排与异常处理。
- [[concepts/概念_AQS同步器]] - AQS、Semaphore、CountDownLatch、CyclicBarrier 的基础原理。
- [[concepts/概念_Java虚拟线程]] - Java 21 虚拟线程定位、优缺点与适用边界。

## Database Concepts
- [[concepts/概念_MySQL基础与SQL]] - MySQL 关系型模型、SQL 职责与工程定位。
- [[concepts/概念_MySQL字段类型设计]] - 字段类型选型原则与常见陷阱。
- [[concepts/概念_MySQL存储引擎_InnoDB与MyISAM]] - InnoDB 与 MyISAM 的能力差异与选型建议。
- [[concepts/概念_MySQL索引与最左前缀匹配]] - B+ 树索引、联合索引与失效场景。
- [[concepts/概念_MySQL日志_binlog_redo_undo]] - 三类日志分工与一致性保障。
- [[concepts/概念_MySQL事务隔离级别与MVCC]] - ACID、隔离级别、并发异常与 MVCC。
- [[concepts/概念_MySQL锁机制_表锁行锁意向锁]] - 表锁、行锁、意向锁与锁冲突分析。
- [[concepts/概念_MySQL执行流程与EXPLAIN]] - 执行计划解读与调优入口。
- [[concepts/概念_MySQL性能优化路径]] - 从慢 SQL 到架构扩展的优化路线。

## Algorithm Concepts
- [[concepts/概念_树上LCA_DFS序方法]] - 用 DFS 序把 LCA 转为 RMQ，并通过 ST 表实现 O(1) 查询。

## OpenClaw Pages
- [[overview/主题_OpenClaw总览]] - OpenClaw 作为自托管多渠道 AI Agent 系统的整体认知。
- [[concepts/概念_OpenClaw架构]] - Gateway-Node-Channel 三层架构与 Loopback-First 安全设计。
- [[concepts/概念_OpenClaw记忆系统]] - SOUL、TOOLS、USER、Session 四层记忆与持久化机制。
- [[concepts/概念_OpenClaw部署与渠道接入]] - 本地、Docker、云厂商部署与国内外消息渠道接入。
- [[concepts/概念_OpenClaw_Skills系统]] - Skills 工作原理、ClawHub、安全审查与自建 Skill。
- [[concepts/概念_OpenClaw模型配置]] - 国际、国产、本地模型与推荐组合。
- [[concepts/概念_OpenClaw安全与成本]] - RCE、供应链攻击、认证、权限与 API 费用控制。
- [[concepts/概念_OpenClaw生态与国内产品]] - 养虾文化、Moltbook、国内生态与国产 Claw 产品。
- [[comparisons/OpenClaw_vs_Claude_Code]] - OpenClaw 与 Claude Code 的定位、能力和组合方式。

## Obsidian & Sync Concepts
- [[concepts/概念_Obsidian多端同步方案选型]] - 官方 Sync、网盘与 Git 路线的取舍，以及大仓库场景的实践建议。
- [[concepts/概念_Termux原生Git接管Obsidian移动端同步]] - Android 端用 Termux 原生 Git 接管同步的流程与边界。
- [[concepts/概念_Obsidian仓库Gitignore策略]] - Obsidian 仓库的忽略规则设计与冲突治理要点。
- [[concepts/概念_移动端一键同步脚本_Commit_Pull_Push]] - 一键同步脚本的标准流程、保护机制与风险点。
