---
title: 幂级数
date: 2024-03-01 22:13:59
tags: [Math, Series]
---
# 函数项级数
## 定义
设 $f_n(x)$ 是定义在 $D$ 上的一串函数（$n = 1, 2, 3, \cdots$），也称之为函数序列，用 `+` 号将其一次连接起来，$f_1(x) + f_2(x) + \cdots + f_n(x) + \cdots \triangleq \sum\limits_{n=1}^\infty f_n(x)$ 称之为 $D$ 上的**函数项级数**。$S_n = f_1(x) + f_2(x) + \cdots + f_n(x)$ 称为**部分和**。$r_n(x) = f_{n+1}(x) + f_{n+2}(x) + \cdots$ 为函数项级数的**余项**。

对 $x_0 \in D$，若 $\sum\limits_{n=1}^\infty f_n(x_0)$ 收敛，则称 $x_0$ 为 $\sum\limits_{n=1}^\infty f_n(x)$ 的**收敛点**，收敛点的全体组成的集合称为 $\sum\limits_{n=1}^\infty f_n(x)$ 的**收敛域**，记 $S(x) = \lim\limits_{n\to\infty} S_n(x)$，称 $S(x)$ 为函数项级数的**和函数**。

## 性质
### **定理1**$\quad$ 函数项级数和函数的连续性
设 $\sum\limits_{n=1}^\infty u_n(x)$ 在 $[a, b]$ 上一致收敛，且级数每一项 $u_n(x)$ 在 $[a, b]$ 上都连续，则和函数 $S(x)$ 在 $[a, b]$ 上连续。

### **定理2**$\quad$ 函数项级数逐项积分性

### **定理3**$\quad$ 函数项级数逐项微分性

# 幂级数
## 定义
称 $\sum\limits_{n=0}^\infty a_n x^n = a_0 + a_1 x + \cdots + a_n x^n + \cdots$ 为标准的**幂级数**，这里 $a_n$，$n = 0, 1, 2, \cdots$ 称之为幂级数的系数。

称 $\sum\limits_{n=0}^\infty a_n (x-x_0)^n = a_0 + a_1(x-x_0) + \cdots + a_n(x-x_0)^n + \cdots$ 为**一般型幂级数**。

称 $\sum\limits_{n=0}^\infty a_n \phi^n(x)$ 为**广义幂级数**。

对于 $\sum\limits_{n=0}^\infty a_n x^n$，当 $x=0$ 时，级数**收敛**，若除 $0$ 以外没有收敛点称为级数**发散**。

任何一个标准的幂级数 $\sum\limits_{n=0}^\infty a_n x^n$，都存在唯一一个 $R$，$(R \ge 0 或 R = +\infty)$ 使 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $(-R, R)$ 内绝对收敛，在 $(-\infty, -R)$ 和 $(R, +\infty)$ 上发散，则称 $R$ 为 $\sum\limits_{n=0}^\infty a_n x^n$ 的**收敛半径**，$(-R, R)$ 称之为 $\sum\limits_{n=0}^\infty a_n x^n$ 的**收敛区间**。

$\sum\limits_{n=0}^\infty a_n x^n$ 的**收敛域** $=$ 收敛区间 $(-R, R) \cup \pm R$ 中收敛的点

## 性质
设 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $x_0 \ne 0$ 点收敛，则 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $\vert x\vert < \vert x_0 \vert$ 上绝对收敛。

**推论**：如果 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $x_0$ 点发散，则 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $\vert x\vert > \vert x_0\vert$ 上发散。

设 $\sum\limits_{n=0}^\infty a_n x^n$ 满足 $\lim\limits_{n\to\infty} \left\vert \frac{a_{n+1}}{a_n}\right\vert$ （或 $\lim\limits_{n\to\infty} \sqrt[n]{\vert a_n\vert}$）$= \rho \ge 0$（或 $+\infty$），则 $R = \frac{1}{\rho}$ 是 $\sum\limits_{n=0}^\infty a_n x^n$ 的收敛半径。