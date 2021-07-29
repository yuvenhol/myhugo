---
title: "Jvm"
date: 2021-07-29T18:31:14+08:00
draft: false
---

## TLAB
由于堆内存是线程共有的，多线程创建对象时可能会出现对象指针的碰撞。为每个线程在eden分配少量的线程独占的内存分配区，那么会极大的改善这个问题。
https://www.cnblogs.com/zhxdick/p/14371562.html
