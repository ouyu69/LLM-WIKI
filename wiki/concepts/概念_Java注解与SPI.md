---
type: "concept"
tags: ["java", "注解", "spi", "框架"]
summary: "注解为代码添加元数据，可在编译期或运行期解析；SPI 通过服务发现机制实现可插拔扩展。"
sources: ["raw/已处理/Java基础常见面试题总结.md"]
updated: "2026-04-23"
---

# 概念：Java 注解与 SPI

## 注解
注解是附加在类、方法、字段、参数等程序元素上的元数据，本身不直接改变业务逻辑，需要由编译器、框架或运行时代码解析。

## 注解解析
- 编译期扫描：例如 `@Override` 由编译器检查。
- 运行期反射处理：例如 Spring 中的组件扫描、依赖注入、配置绑定等。

## SPI
SPI 是 Service Provider Interface，用于让框架定义接口，由第三方提供具体实现，再通过约定配置完成服务发现和加载。

## SPI 与 API
- API 面向使用者，强调调用已有能力。
- SPI 面向扩展者，强调按约定提供实现让框架调用。

## 关联
- [[concepts/概念_Java反射]]
- [[concepts/概念_Java动态代理]]
- [[sources/来源_Java基础常见面试题总结]]
