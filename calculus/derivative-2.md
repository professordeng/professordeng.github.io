---
title: 求导
mathjax: true
---

导数描述了某个点附近的最佳近似，因此微小变化量是导数的本质。

让我们先从幂函数的导数说起吧。

$$
\frac{dx^n}{dx}=nx^{n-1}
$$

## 面积增量

$A=x^2$ 表示边长为 $x$ 的面积。

$x$ 的微小增量 $dx$ 会引起 $A$ 的微小增量 $dA$。

$A$ 的几何意义是正方形，其面积增量为：

$$
dA = xdx + xdx + (dx)^2
$$

因此对应的导数为：

$$
\frac{dA}{dx} = 2x
$$

## 体积增量

$V=x^2$ 表示边长为 $x$ 的体积。

$V$ 的几何意义是正方体，其面积增量为：

$$
dV=3x^2dx + (\cdots)(dx)^2
$$

因此对应的导数为：

$$
\frac{dV}{dx}=3x^2
$$

对于大于 3 的自然数，其推理规则类似。

## 