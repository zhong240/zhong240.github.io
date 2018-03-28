---
layout: post
title: Programming Basics 编程的一些基本常识
key: 2018031901
tags: basics
---

每天学一点。先写中文的。

#### IDE: Integrated Development Environment 集成开发环境

IDE是应用程序。代码编辑器。可以有额外的编译功能、设计UI功能。

如: Visual Studio, Android Studio, NetBeans(Oracle, Java), Eclipse, Xcode.

Sorce code editor is a part of IDE.

Example: Sublime text, Atom

#### API: Application Programming Interface 应用程序编程接口

可以理解为定义的函数将会被如何使用。接口是一个媒介, 连接两端的内容。

Interface的一个较好翻译是"交互"。比如User Interace, 一般的翻译为用户操作界面, 实际上是人与软件的交互过程——人输入数据, 程序输出结果。

还有一种理解, API是产品经理为客户提供的产品。产品怎么做的客户并不知道, 但是客户知道有哪些产品可用以及如何使用就好。

#### SDK: Software Development Kit 软件开发工具组

意如其名, 写软件的开发工具。

SDK跟IDE容易混淆, 简单来说SDK更底层, 是基本平台; IDE是加了一堆插件的SDK。

"A set of software development tools that allows the creation of applications for a certain software package, software framework, hardware platform, computer system, video game console, operating system, or similar development platform."(Wikipedia)

#### DDL: Dynamic Link Library 动态链接库
“在Windows中，许多应用程序并不是一个完整的可执行文件，它们被分割成一些相对独立的动态链接库，即DLL文件，放置于系统中。当我们执行某一个程序时，相应的DLL文件就会被调用。一个应用程序可有多个DLL文件，一个DLL文件也可能被几个应用程序所共用。” (百度百科) 

相当于代码被模块化。因此一个好处是代码可以分开编译, 提高debug效率。另一个好处是在程序运行时候占用的内存变小, 因为只有需要的时候才调用某些模块。

#### Junit

Unit testing framework for Java. 这个是要学的。
