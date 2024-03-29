---
title: C 语言的控制流
---

本文讲 C 程序最基本的常识。核心知识包括变量、控制流。

## 变量

语言是带有信息的，没有信息的语言就是废话。

C 语言也是如此，C 语言的信息就是`常量`和`变量`。

常量不会发生改变，如常数。

变量是会改变的值，我们会给这些变化的值一个统一的存储空间，并取一个名字。如：

```c
int name;
```

变量有特定的几种类型，包括`整数`、`浮点数`、`数组`、`枚举`、`结构体`等等。

信息之间会发生交互，我们将交互的类型称为`运算符`。包括：

- 算术运算符（加、减、乘、除）
- 逻辑运算符（与、或、非）
- 关系运算符（大于、小于、等于）
- 位运算（左移、右移、按位异或）

计算机处理的结果会呈现在屏幕上，至于以什么形式出现，C 语言提供了不同的格式，如：

```c
printf("%d", x);   // 十进制整数
printf("%c", ch);  // 字符
printf("%s", str); // 字符串
printf("%f", y);   // 浮点数
putchar(ch);       // 输出字符
```

计算机处理的信息可以通过键盘输入，相应代码如下：

```c
scanf("%d", &a);
a = getchar()
```

其中 `&a` 表示 a 的地址。从键盘输入一个字符，并将其存入 a 的地址中。

## 控制流

在 C 语言中，代码是逐条执行的，根据执行顺序的特点分为三种结构，分别是`顺序结构`、`条件结构`和`循环结构`。

在循环结构中，C 语言按顺序执行代码。

选择结构则根据条件判断来决定执行部分代码，如求绝对值：

```c
if (x >= 0) printf("%d", x);
else printf("%d", -x);
```

循环结构根据条件判断来重复执行一段代码，如输出小于 10 的自然数：

```c
int i = 0;
while (i < 10) {
    printf("%d ", i);
    i ++;
}
```

可以用 `break` 提前终止循环。

可以用 `continue` 提前结束本次循环，直接进入下次循环的判断。