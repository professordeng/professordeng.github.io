---
title: 面积
mathjax: true
---

假设你已知矩形的面积等于底乘高。

给你一个函数 $f(x)=2x$。

在只用矩形面积公式的情况下，求 f 和 x 轴在 [0, 1] 围成的面积 A。

## 微元与积分

把 A 近似成矩形，高取 f(1)，得到面积为 `2`，和正确答案 `1` 相距有点远。

把 A 分成两段 [0, 0.5] 和 [0.5, 1]，分别求两部分的面积，然后求和：

$$
A = 0.5\times f(0.5) + 0.5\times f(1)=1.5
$$

我们发现离正确答案更近了。

如果把 [0, 1] 平均分成很多段，然后求和，就可以求出 A 的面积。

这里的计算涉及到了两个步骤：

- 微元：每个时间段对应的路程
- 积分：将各时间段的路程相加

我们可以用数学符号表示求面积的过程：

$$
A = \int_{0}^1 f(x)dx
$$