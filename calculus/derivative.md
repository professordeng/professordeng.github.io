---
title: 导数的悖论
mathjax: true
---

假设车的路程 s 随时间 t 的关系如下：

$$
S(t) = t^3
$$

每辆车上都有车速表，则车速表的数字 v 和时间 t 的关系如下：

$$
V(t) = 3t^2
$$

理解 V(1) = 3 的含义：

- 错误：时刻 1 的瞬时速度
- 正确：时刻 1 附近的速度近似值

## 导数

如何求每个时间点附近的速度近似值呢，采用速度定义：

$$
v = \frac{s}{t}
$$

那么附近的近似值就可以表示为：

$$
V(t) = \frac{ds}{dt}(t)=3t^2
$$

几何意义就是 S(t) 的切线斜率。

## 悖论

把速度曲线 V(t) 的点认为是瞬间速度，是一件很矛盾的事。

V(0) = 0 代表车在时刻 0 时的瞬间速度为零，即不发生运动。但实际上时刻 0 是车的启动时刻。

所以请把`导数`认为是曲线的`某个点附近的变化率的最佳近似`。 