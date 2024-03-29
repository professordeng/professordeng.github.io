---
title: 数据类型
---

C++ 数据类型包括以下几种：

- 基本数据类型，如 int 等
- 枚举类型
- 数组类型
- 指针类型
- 引用类型
- 结构体
- 共用体

上述类型很多在 [C 语言]中有讲过，本文介绍 C 语言之外的新特性。

## 引用类型


在 C++ 中，引用是一个已定义变量的别名，用于简化指针的使用和函数参数的传递。引用使用 `&` 符号来声明。

```c
void swap(int& x, int& y) {
    int temp = x;
    x = y;
    y = temp;
}

int a = 10, b = 20;
swap(a, b);
cout << a << " " << b << endl; // 输出 20 10
```

引用类型不占用内存空间，仅仅是一个变量的别名。

## 类型推断

我很喜欢 C++ 的 `auto` 关键字。`auto` 可以用来让编译器自动推导变量的类型，使代码更加简洁和易读。

```c
auto i = 42;      // i 的类型被推导为 int
auto d = 3.14;    // d 的类型被推导为 double
auto s = "hello"; // s 的类型被推导为 const char*
```