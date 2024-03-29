---
title: 什么是操作系统
---

计算机是由多个硬件组成的，最流行的计算机模型是[冯·诺伊曼模型](https://en.wikipedia.org/wiki/Von_Neumann_architecture)。为了更高效地利用计算机硬件，人们开发专门的软件来管理硬件，该软件就是操作系统。当应用软件需要调用硬件资源的时候，需要向操作系统申请。

硬件的调用是通过一条条指令来执行的，操作系统将这些指令封装起来，提供统一且简洁的调用接口，应用软件可以直接通过调用接口来获取服务，而不需要涉及调用硬件的底层指令。

## 发展

随着人类的需求发展，操作系统也相应发展。为了让计算机自动执行多个程序，人们设计出了`批处理操作系统`。批处理操作系统分为单道批处理和多道批处理，其中单道批处理的特点是内存中仅有一道程序。

批处理操作系统可对用户作业成批处理，但期间用户不能和计算机交互。为了实现交互功能，人们设计出了`分时操作系统`，分时是指把处理机的运行时间分成很短的时间片，按时间片轮流把处理机分配给各联机作业使用。

一些行业对时间特别敏感，例如汽车。当发生车祸的时候，汽车必须在规定时间内启动安全气囊，这需要操作系统快速响应，于是人们设计出了`实时操作系统`。实时操作系统的特点是在规定的时间内完成响应。

## 内核

随着操作系统复杂度的提升，操作系统的设计难度也跟着提升，人们就提出了微内核的概念。内核是操作系统的一部分代码，这部分代码对硬件有绝对的掌控权，如进程管理、文件系统。除了内核，其他代码称为服务模块。

微内核使得操作系统的代码更加清晰，容易拓展和调试。