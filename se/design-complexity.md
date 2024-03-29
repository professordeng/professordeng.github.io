---
title: 软件设计的复杂性
---

软件设计的最大目标，就是降低复杂性（complexity）。

复杂度指任何使得软件难以理解和修改的因素。

复杂度的来源有两个：代码的含义模糊和互相依赖。

模糊指的是，代码里面的重要信息，看不出来。

依赖指的是，某个模块的代码，不结合其他模块，就会无法理解。

## 复杂性的危害

复杂性的危害在于，它会递增。

你做错了一个决定，导致后面的代码都基于前面的错误实现，整个软件变得越来越复杂。

## 降低复杂性的方法

把复杂性隔离在一个模块，不与其他模块互动。

模块分成接口和实现。接口要简单，实现可以复杂。

除了那些必须告诉用户的错误，其他错误尽量在软件内部处理掉，不要抛出。

## 参考资料

- [如何降低软件的复杂性](https://www.ruanyifeng.com/blog/2018/09/complexity.html)