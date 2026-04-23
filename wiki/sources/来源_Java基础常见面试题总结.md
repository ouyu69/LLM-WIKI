---
type: "source"
tags: ["java", "基础", "面试", "javaguide"]
summary: "Java 基础高频面试题综述，覆盖 JVM/JDK/JRE、语法、基本类型、OOP、Object/String、异常、泛型、反射、代理、注解、SPI、序列化与 I/O。"
sources: ["raw/已处理/Java基础常见面试题总结.md"]
updated: "2026-04-23"
---

# 来源摘要：Java基础常见面试题总结

## 来源信息
- 文件：`raw/已处理/Java基础常见面试题总结.md`
- 来源站点：JavaGuide（Java 基础面试专题）
- 主题范围：Java 基础概念、语法、面向对象、核心类库与常见运行机制

## 核心要点
- JVM 是运行 Java 字节码的虚拟机，JRE 是运行环境，JDK 在 JRE 基础上提供开发工具。
- Java 通过字节码实现跨平台，并在运行时结合解释执行与 JIT 编译；AOT 可改善启动与内存占用，但通常牺牲部分峰值优化能力。
- 基本类型与包装类型在存储、默认值、泛型支持、比较方式和缓存机制上存在差异。
- 面向对象核心包括封装、继承、多态；重载发生在同一类方法签名层面，重写发生在子类覆盖父类方法层面。
- `Object` 的 `equals()` 与 `hashCode()` 共同影响对象相等性和哈希容器行为。
- `String` 不可变且依赖字符串常量池；拼接、`intern()`、`new String()` 的对象创建语义是高频考点。
- Java 异常体系分为 `Error` 与 `Exception`，`Exception` 又可分为受检查异常与不受检查异常。
- 泛型提升类型安全与复用性，但 Java 泛型主要通过类型擦除实现，运行期类型信息有限。
- 反射、动态代理、注解与 SPI 是 Java 框架能力的重要基础。
- 序列化用于对象存储和传输，但 JDK 原生序列化存在跨语言、性能和安全风险。
- Java I/O 涉及字节流/字符流、装饰器/适配器等设计模式，以及 BIO/NIO/AIO 三类模型差异。

## 关联概念页
- [[concepts/概念_JVM_JDK_JRE与字节码]]
- [[concepts/概念_Java基本数据类型与包装类型]]
- [[concepts/概念_自动装箱与拆箱]]
- [[concepts/概念_面向对象三大特征]]
- [[concepts/概念_Java方法重载与重写]]
- [[concepts/概念_抽象类与接口]]
- [[concepts/概念_Object_equals与hashCode]]
- [[concepts/概念_字符串类型_String_StringBuffer_StringBuilder]]
- [[concepts/概念_Java异常体系]]
- [[concepts/概念_Java泛型]]
- [[concepts/概念_Java反射]]
- [[concepts/概念_Java动态代理]]
- [[concepts/概念_Java注解与SPI]]
- [[concepts/概念_Java序列化]]
- [[concepts/概念_Java_IO模型]]

## Ingest 状态
- 已按主题粒度完成 ingest；未逐题拆页，避免产生过碎页面。
