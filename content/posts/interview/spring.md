---
title: "spring"
date: 2021-07-28T16:48:44+08:00
draft: false
---

# Spring Core

## Ioc:

依赖倒置原则：
把原本的高层建筑依赖底层建筑“倒置”过来，变成底层建筑依赖高层建筑。高层建筑决定需要什么，底层去实现这样的需求，但是高层并不用管底层是怎么实现的。这样就不会出现前面的“牵一发动全身”的情况。
例如一个高层的类需要底层的类

Ioc(**Inversion of Control**) 就是依赖倒置原则的一种代码设计的思路。具体采用的方法就是所谓的**依赖注入（Dependency Injection）**。


IoC 容器是 Spring ⽤来实现 IoC 的载体， IoC 容器实际上就是个Map（key，value）,Map 中存放的是各种对象

