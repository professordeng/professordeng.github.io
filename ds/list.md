---
title: 链表
---

链表是一种常见的线性结构，它由一系列节点组成，每个节点包含两个部分：数据和指向下一个节点的指针。

节点的指针指向下一个节点，从而将所有节点按顺序连接起来。

链表的首节点称为头结点，尾节点称为尾结点。

链表可以分为单向链表、双向链表和循环链表等不同类型。

## 数据操作

链表相对于[数组](/ds/list)的主要优势是插入和删除节点的效率较高，因为只需要修改相邻节点的指针即可，而不需要像数组那样进行大量的数据移动。

但是链表的缺点是访问节点的效率较低，因为需要从头结点开始遍历链表才能找到目标节点。

链表还需要额外的存储空间来存储指针，因此相对于数组，链表需要更多的内存空间。

## 应用

在实际的程序设计中，链表常常用于实现栈、队列和哈希表等数据结构。

链表还常常与递归算法一起使用，例如反转链表、合并链表和判断链表是否存在环等问题。

在编写程序时，需要注意链表的空指针和头指针，以及链表的插入和删除操作等问题。

需要注意链表的复杂度分析，以便选择合适的算法来解决问题。
