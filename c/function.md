---
title: 函数
---

函数是对一段代码的封装，如将求最大值封装成一个函数：

```c
int max(int x, int y) {      // 返回类型 函数名(参数列表)
    return (x > y) ? x : y;  // 代码段
}
c = max(a, b);               // 调用函数
```

注意 a 传递给 x 时会发生一次复制，也就是说 a 和 x 不是同一个存储单元。

数组名可以作为函数参数。

## 作用范围

一个程序可能由多个源文件编译而成。

不同源文件有不同的函数实现，为了使逻辑更清晰，C 语言提供了函数的作用范围。

`内部函数`只能用于定义的源文件中，而不能在其他源文件中使用，用 `static` 修饰。

如果函数没有 `static` 修饰，则默认为是`全局函数`。

变量也有作用范围，在函数内部定义的变量是`局部变量`，在函数外定义的变量是`全局变量`。

若出现变量的名字冲突，则局部变量会屏蔽全局变量。

若全局变量被 `static` 修饰，则该变量只能用于源文件内。