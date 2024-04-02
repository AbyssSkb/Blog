---
title: 级数
date: 2024-02-29 12:08:56
tags: [Math, Series]
description: 级数（英语：Series）是数学中一个有穷或无穷的序列之和，如果序列是有穷序列，其和称为有穷级数；反之，称为无穷级数（一般也简称为级数）。
---
# 级数
## 定义
设 $\{a_n\}$ 为一个无穷数列，用 `+` 将 $a_n$ 的项依次连起来，得到一个式子 $a_1 + a_2 + \cdots + a_n + \cdots$，称此式子为 **（无穷数项）级数**，简记为 $\sum\limits_{n=1}^\infty a_n$

$a_1$ 称为第一项，$a_n$ 称为通项，$S_n = a_1 + a_2 + \cdots + a_n$ 称为**部分和**。

## 敛散性
设 $\sum\limits_{n=1}^\infty a_n$ 为一级数，$S_n = a_1 + a_2 + \cdots + a_n$ 为其部分和，若 $\lim\limits_{n\to\infty} S_n$ 存在，则称级数 $\sum\limits_{n=1}^\infty a_n$ **收敛**，此时 $\lim\limits_{n\to\infty} S_n = \sum\limits_{n=1}^\infty a_n$。若 $\lim\limits_{n\to\infty} S_n$ 不存在，则称级数 $\sum\limits_{n=1}^\infty a_n$ **发散**。

## 性质
1. $k \ne 0$ 时，$\sum\limits_{n=1}^\infty a_n$ 与 $\sum\limits_{n=1}^\infty ka_n$ 的敛散性一致，且收敛时 $\sum\limits_{n=1}^\infty ka_n = k\sum\limits_{n=1}^\infty a_n$。
2. 若 $\sum\limits_{n=1}^\infty a_n$ 与 $\sum\limits_{n=1}^\infty b_n$ 都收敛，则 $\sum\limits_{n=1}^\infty (a_n \pm b_n)$ 也收敛，且 $\sum\limits_{n=1}^\infty (a_n \pm b_n) = \sum\limits_{n=1}^\infty a_n \pm \sum\limits_{n=1}^\infty b_n$。
3. 一个级数去掉或添加有限项不改变级数的敛散性。
4. 收敛级数满足结合律。
5. 若 $\sum\limits_{n=1}^\infty a_n$ 收敛，则 $\lim\limits_{n\to\infty} a_n = 0$。

## 两个重要级数
### 等比级数 
$$\sum\limits_{n=1}^\infty r^n$$

当 $\vert r\vert < 1$ 时收敛；

当 $\vert r \vert \ge 1$ 时发散。

### p-级数
$$\sum\limits_{n=1}^\infty \frac{1}{n^p}$$

当 $0 < p \le 1$ 时发散；

当 $p>1$ 时收敛。

# 正项级数
## 定义
称满足 $a_n > 0$ 的无穷级数 $\sum\limits_{n=1}^\infty a_n$ 为**正项级数**。

## 敛散性判别法
1. 正项级数 $\sum\limits_{n=1}^\infty$ 收敛 $\Leftrightarrow$ 部分和有上界。
2. 比较判别法

设 $\sum\limits_{n=1}^\infty a_n$，$\sum\limits_{n=1}^\infty b_n$ 为两个正项级数，若从某项以后有 $a_n \le b_n$，则

当 $\sum\limits_{n=1}^\infty b_n$ 收敛时，$\sum\limits_{n=1}^\infty a_n$ 收敛；

当 $\sum\limits_{n=1}^\infty a_n$ 发散时，$\sum\limits_{n=1}^\infty b_n$ 发散。

# 交错级数
## 定义
设 $a_n > 0$，称 $\sum\limits_{n=1}^\infty (-1)^n a_n$ 或 $\sum\limits_{n=1}^\infty (-1)^{n+1} a_n$ 为**交错级数**。

## 性质
设交错级数 $\sum\limits_{n=1}^\infty (-1)^n a_n$ 满足 $\lim\limits_{n\to\infty} a_n = 0$，且 $a_n \ge a_{n+1}$，$n = 1, 2, \cdots$，则交错级数 $\sum\limits_{n=1}^\infty (-1)^n a_n$ 收敛。

# 绝对收敛级数
## 定义
若 $\sum\limits_{n=1}^\infty \vert u_n \vert$ 收敛，则称级数 $\sum\limits_{n=1}^\infty u_n$ 为**绝对收敛**。

## 性质
- 绝对收敛级数必收敛
- 绝对收敛级数满足交换律

# 条件收敛级数
## 定义
若 $\sum\limits_{n=1}^\infty \vert u_n \vert$ 发散，而 $\sum\limits_{n=1}^\infty u_n$ 收敛，则称级数 $\sum\limits_{n=1}^\infty u_n$ **条件收敛**。

## 性质
条件收敛级数不满足交换律。