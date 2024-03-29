---
title: 关系运算的连接操作
mathjax: true
---

连接（join）：从两个关系的笛卡儿积中选取属性间满足一定条件的元组。

用 $\mathop{R\bowtie S}\limits_{A\theta B}$ 表示，其中 A 和 B 分别为 R 和 S 上列数相等且可比的属性组，$\theta$ 为比较运算符。

假设关系 R 如下：

| A  | B  | C |
|----|----|---|
| a1 | b1 | 5 |
| a2 | b2 | 6 |

关系 S 如下：

| B  | E |
|----|---|
| b1 | 2 |
| b1 | 7 |
| b3 | 4 |

## 非等值连接

则非等值连接 $\mathop{R\bowtie S}\limits_{C < E}$ 的结果为：

| A  | R.B | C | S.B | E |
|----|-----|---|-----|---|
| a1 | b1  | 5 | b1  | 7 |
| a2 | b2  | 6 | b1  | 7 |

## 等值连接

等值连接 $\mathop{R\bowtie S}\limits_{R.B= S.B}$ 的结果为：

| A  | R.B | C | S.B | E |
|----|-----|---|-----|---|
| a1 | b1  | 5 | b1  | 2 |
| a1 | b1  | 5 | b1  | 7 |

自然连接是一种特殊的连接。它要求两个关系中进行比较的份量必须是同名的属性组，并且在结果中把重复的属性列去掉。上述等值连接对应的自然连接如下：

| A  | B  | C | E |
|----|----|---|---|
| a1 | b1 | 5 | 2 |
| a1 | b1 | 5 | 7 |

## 悬浮元组

在等值连接操作中，R 和 S 中某些元组被舍弃了，这些被舍弃的元组称为悬浮元组（dangling tuple）。

如果把悬浮元组也保存在结果关系中，而在其他属性上填空值（NULL），那么这种连接就叫做外连接（outer join）。

| A    | B  | C    | E    |
|------|----|------|------|
| a1   | b1 | 5    | 2    |
| a1   | b1 | 5    | 7    |
| a2   | b2 | 6    | NULL |
| NULL | b3 | NULL | 4    |

如果只保留左边关系 R 中的悬浮元组就叫做左外连接（left join）。

| A  | B  | C | E    |
|----|----|---|------|
| a1 | b1 | 5 | 2    |
| a1 | b1 | 5 | 7    |
| a2 | b2 | 6 | NULL |

如果只保留右边关系 S 中的悬浮元组就叫做右外连接（right join）。

| A    | B  | C    | E |
|------|----|------|---|
| a1   | b1 | 5    | 2 |
| a1   | b1 | 5    | 7 |
| NULL | b3 | NULL | 4 |