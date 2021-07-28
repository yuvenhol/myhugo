---
title: "Java基础"
date: 2021-07-28T11:48:44+08:00
draft: false
---

## 集合框架
主要是对三个接口的实现，Set、Map、List。其中Set、List又实现了Collection
### HashMap
#### 结构
数组+链表or红黑树
#### 负载因子0.75f的原因
空间和查询效率的平衡
#### 树化阈值8的原因
和泊松分布，连续8次hash冲突的概率极低百万分之一，空间和速度的取舍，为啥还要转为树？防止hash冲突
### ConcurrentHashMap

## GC
GCRoot：被栈区、native栈、方法区
### GC算法
1标记-清理（CMS）：缺点内存碎片
2标记-整理：缺点全部数据移动，耗时长
3复制算法（parNew、youngGC使用算法）：缺点内存消耗大
4：
一个对象在6次gc后会转移到old区中，old区里也有大对象。

### GC清理器
#### G1
1：初步标记 找出root对象和对应的rootRegion
2：根据rootRegion的RSet找出CSet
3：对Cset并发标记
4：补充标记
5：并发清理，使用标记复制算法