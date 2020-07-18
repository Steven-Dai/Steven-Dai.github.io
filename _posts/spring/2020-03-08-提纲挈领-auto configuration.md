---
layout: blog
title: spring boot auto configuration
background-image:
date: 2020-03-08 22:00:00
category: spring boot
tags:
  - spring boot
  - 提纲挈领
  - configuration
---

_提纲挈领(4) 自动配置 auto configuration_

# 是什么

Spring 应用启动时，auto configuration 可以根据 jar 的依赖关系自动创建对象并添加到 spring 容器中。

# 核心点

@EnableAutoConfiguration 启用 auto-configuration。

@Import(EnableAutoConfigurationImportSelector.class) auto-configuration 机制的启动入口。

EnableAutoConfigurationImportSelector 实现了接口 DeferredImportSelector，其内部调用了

SpringFactoriesLoader.loadFactoryNames()方法，该方法会从 META-INF/spring.factories 中加载配置类。

# 特点

1、取代原则：自定义配置 取代 默认配置。比如 datasource。

2、禁用一些配置方式

方法一：@SpringBootApplication(exclude={DataSourceAutoConfiguration.class})

方法二：spring.autoconfigure.exclude=XXX

# 我的示例

待补充……
