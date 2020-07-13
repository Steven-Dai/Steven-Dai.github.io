---
layout: blog
title: spring boot auto configuration
background-image: 
date:  2020-03-08 23:45:56
category: git
tags:
- spring boot
- 提纲挈领
- configuration

---

*提纲挈领(4)	自动配置 auto configuration*

# 是什么

Spring应用启动时，auto configuration可以根据jar的依赖关系自动创建对象并添加到spring容器中。

# 核心点

@EnableAutoConfiguration 启用auto-configuration。

@Import(EnableAutoConfigurationImportSelector.class)  auto-configuration机制的启动入口。

EnableAutoConfigurationImportSelector实现了接口DeferredImportSelector，其内部调用了

SpringFactoriesLoader.loadFactoryNames()方法，该方法会从META-INF/spring.factories中加载配置类。

# 特点

1、取代原则：自定义配置 取代 默认配置。比如datasource。

2、禁用一些配置方式

方法一：@SpringBootApplication(exclude={DataSourceAutoConfiguration.class})

方法二：spring.autoconfigure.exclude=XXX

# 我的示例

待补充……



