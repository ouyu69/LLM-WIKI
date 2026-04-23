---
type: "concept"
tags: ["java", "jvm", "jdk", "jre", "字节码"]
summary: "JDK 提供开发工具，JRE 提供运行环境，JVM 执行字节码；字节码是 Java 跨平台和运行期优化的基础。"
sources: ["raw/已处理/Java基础常见面试题总结.md", "raw/已处理/JVM常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：JVM、JDK、JRE 与字节码

## 定义
- `JVM`：Java 虚拟机，负责加载、验证、解释或编译执行 `.class` 字节码。
- `JRE`：Java 运行环境，包含 JVM、基础类库与运行 Java 程序所需组件。
- `JDK`：Java 开发工具包，在 JRE 基础上提供 `javac`、`javadoc`、调试和打包等开发工具。
- 字节码：Java 源码经编译后生成的中间代码，不绑定具体 CPU 或操作系统。

## 关键理解
- Java 的跨平台能力主要来自“源代码编译成字节码，字节码交给不同平台的 JVM 执行”。
- Java 通常被描述为“编译与解释并存”：源码先编译为字节码，运行时再由解释器和 JIT 编译器协作执行。
- JIT 适合根据运行时热点做深度优化；AOT 可改善启动时间、内存占用和部署体积，但通常难以完全替代 JIT 的运行期优化。
- Oracle JDK 与 OpenJDK 的核心差异主要在发行、授权、商业支持和部分工具链上，具体选择应结合项目合规与运维要求。

## 关联
- [[sources/来源_Java基础常见面试题总结]]
- [[sources/来源_JVM常见面试题总结]]
