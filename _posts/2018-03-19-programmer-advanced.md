---
layout: post
title: Programmer Advanced 程序员的素养
key: 2018031902
tags: advanced
---

每天学一点。先写中文的。

#### TensorFlow

这个最近提到的非常多, 有必要了解一下(即使我不是真的那么感兴趣)。

目前的了解是, TensorFlow是一个google po出来的machine learning开源library。因为很先进而且开源所以火起来了吧(大概)。

中文介绍/入门教学：
<http://www.tensorfly.cn/tfdoc/get_started/introduction.html>

我还没来得及读。

#### Apache

Web server, 一款软件。只支持html, 静态网页。

"Apache是以进程为基础的结构，进程要比线程消耗更多的系统开支，不太适合于多处理器环境，因此，在一个Apache Web站点扩容时，通常是增加服务器或扩充群集节点而不是增加处理器。"(百度百科)

#### Multiprocess vs. Multithread 多进程与多线程

在知乎上看到一个非常有趣的例子, 贴在这里。

1。单进程单线程：一个人在一个桌子上吃菜。2。单进程多线程：多个人在同一个桌子上一起吃菜。3。多进程单线程：多个人每个人在自己的桌子上吃菜。

多线程的问题是多个人同时吃一道菜的时候容易发生争抢，例如两个人同时夹一个菜，一个人刚伸出筷子，结果伸到的时候已经被夹走菜了。。。此时就必须等一个人夹一口之后，在还给另外一个人夹菜，也就是说资源共享就会发生冲突争抢。

1。对于 Windows 系统来说，【开桌子】的开销很大，因此 Windows 鼓励大家在一个桌子上吃菜。因此 Windows 多线程学习重点是要大量面对资源争抢与同步方面的问题。

2。对于 Linux 系统来说，【开桌子】的开销很小，因此 Linux 鼓励大家尽量每个人都开自己的桌子吃菜。这带来新的问题是：坐在两张不同的桌子上，说话不方便。因此，Linux 下的学习重点大家要学习进程间通讯的方法。

--补充：有人对这个开桌子的开销很有兴趣。我把这个问题推广说开一下。开桌子的意思是指创建进程。开销这里主要指的是时间开销。可以做个实验：创建一个进程，在进程中往内存写若干数据，然后读出该数据，然后退出。此过程重复 1000 次，相当于创建/销毁进程 1000 次。在我机器上的测试结果是：       

UbuntuLinux：耗时 0.8 秒       

Windows7：耗时 79.8 秒        

两者开销大约相差一百倍。

这意味着，在 Windows 中，进程创建的开销不容忽视。换句话说就是，Windows 编程中不建议你创建进程，如果你的程序架构需要大量创建进程，那么最好是切换到 Linux 系统。

大量创建进程的典型例子有两个，一个是 gnu autotools 工具链，用于编译很多开源代码的，他们在 Windows 下编译速度会很慢，因此软件开发人员最好是避免使用 Windows。另一个是服务器，某些服务器框架依靠大量创建进程来干活，甚至是对每个用户请求就创建一个进程，这些服务器在 Windows 下运行的效率就会很差。这"可能"也是放眼全世界范围，Linux  服务器远远多于 Windows 服务器的原因。(作者：pansz
<https://www.zhihu.com/question/19901763/answer/13299543>
)

#### Combinatorial optimization 组合优化问题

A topic in applied mathematics and theoretical computer science to find the optimal object from a finite set of objects.

Applications:
- TSP (Traveling Salesman Problem)
- MSP (Minimum Spanning Tree)
- Scheduling Problem
- Knapsack Problem
- Bin Packing Problem
- Graph Coloring Problem
- Vehicle Routing Problem
