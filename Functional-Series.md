---
title: 函数项级数
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
- **阿贝尔引理**

设 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $x_0 \ne 0$ 点收敛，则 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $\vert x\vert < \vert x_0 \vert$ 上绝对收敛。

**推论**：如果 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $x_0$ 点发散，则 $\sum\limits_{n=0}^\infty a_n x^n$ 在 $\vert x\vert > \vert x_0\vert$ 上发散。

**思考**：这同时也证明了幂级数存在收敛半径，小于这个收敛半径时幂级数收敛，大于这个收敛半径时幂级数发散。
- 如何求收敛域？

设一幂级数为 $\sum\limits_{n=0}^\infty u_n$，令 $\lim\limits_{n\to\infty} \left\vert \frac{u_{n+1}}{u_n}\right\vert < 1$ （或令 $\lim\limits_{n\to\infty} \sqrt[n]{\vert u_n\vert} < 1$），求出来 $x$ 的范围即为 $\sum\limits_{n=0}^\infty u_n$ 的收敛区间，再验证一下区间的左右端点是否收敛即可得到收敛域。

**思考**：为什么能这样做？

正项级数的性质中比值审敛法和根植审敛法都以 1 为边界，而幂级数又存在收敛半径，刚刚好！
- 设 $\sum\limits_{n=0}^\infty a_n x^n$ 的收敛半径为 $R_1$，$\sum\limits_{n=0}^\infty b_n x^n$ 的收敛半径为 $R_2$，令 $R = \min\{R_1, R_2\}$，则有
$$
\sum\limits_{n=0}^\infty a_n x^n + \sum\limits_{n=0}^\infty b_n x^n = \sum\limits_{n=0}^\infty (a_n \pm b_n) x^n, \quad \vert x \vert < R
$$
**思考**：这个性质乍一看似乎没啥用，但是反过来就有大用了！$\sum\limits_{n=0}^\infty (a_n \pm b_n)x^n$ 的收敛域有时候用上一条性质并不好求，但是 $\sum\limits_{n=0}^\infty a_nx^n$ 和 $\sum\limits_{n=0}^\infty b_nx^n$ 的收敛半径 $R_1$ 和 $R_2$ 用上一条性质很好求，那么 $\sum\limits_{n=0}^\infty (a_n \pm b_n)x^n$ 的收敛半径 $R = \min\{R_1, R_2\}$
## 小结
幂级数真的非常美，从阿贝尔引理的证明，到求收敛域的过程，都运用了绝对收敛和正项级数的性质，这也突出学好前面知识的重要性。
# 三角级数
## 定义
称 $\frac{1}{2}a_0 + \sum\limits_{n=1}^\infty a_n\cos nx + b_n \sin nx$ 为**三角级数**。

# 傅里叶级数
## 定义
若 $f(x)$ 以 $2\pi$ 为周期，且以下积分存在
$$
\begin{split}
    &a_0 = \frac{1}{\pi}\int_{-\pi}^\pi f(x)dx \\
    &a_n = \frac{1}{\pi}\int_{-\pi}^\pi f(x)\cos nxdx \\
    &b_n = \frac{1}{\pi}\int_{-\pi}^\pi f(x)\sin nxdx
\end{split}
$$
称 $\frac{1}{2} a_0 + \sum\limits_{n=1}^\infty a_n \cos nx + b_n \sin nx$ 为 $f(x)$ 的**傅里叶级数**，简称为 $F-$ 级数。

其中 $a_0, a_n, b_n(n=1,2,\cdots)$ 为**傅里叶系数**。

若 $f(x)$ 为奇函数，$a_0 = a_n = 0(n=1, 2, \cdots)$，$b_n = \frac{2}{\pi}\int_0^\pi f(x)\sin nx dx$，此时 $F-$ 级数变为 $\sum\limits_{n=1}^\infty b_n \sin nx$，称为 **$F-$ 正弦型级数**。

若 $f(x)$ 为偶函数，$b_n = 0, a_0 = \frac{2}{\pi}\int_0^\pi f(x)dx, a_n = \frac{2}{\pi}\int_0^\pi f(x)\cos nx dx, (n=1,2,\cdots)$，此时 $F-$ 级数变为 $\frac{1}{2} a_0 + \sum\limits_{n=1}^\infty a_n \cos nx$，称为 **$F-$ 余弦型级数**

## 狄利克雷定理
若 $f(x)$ 在 $[-\pi, \pi]$ 上满足：
1. 至多有限个第一类间断点
2. 至多有限个极值

则 $f(x)$ 在 $[-\pi, \pi]$ 上 $F-$ 级数收敛，且
$$
\frac{1}{2}a_0 + \sum\limits_{n=1}^\infty (a_n \cos nx + b_n \sin nx) = \begin{cases}
    f(x) & x 为 (-\pi, \pi) 的连续点 \\
    \frac{1}{2}  \left[f(x^+) + f(x^-)\right] & x 为 (-\pi, \pi) 的第一类间断点 \\
    \frac{1}{2} \left[f(-\pi^+) + f(\pi^-)\right]& x = \pm\pi
\end{cases}
$$

## 以 $2l$ 为周期的函数的傅里叶级数
$f(x)$ 在 $[-l, l]$ 的 $F-$ 级数为 $\frac{1}{2}a_0 + \sum\limits_{n=1}^\infty \left(a_n \cos \frac{n\pi}{l}x + b_n \sin \frac{n\pi}{l}x\right)$，其中
$$
\begin{split}
    &a_0 = \frac{1}{l}\int_{-l}^l f(x)dx \\
    &a_n = \frac{1}{l}\int_{-l}^l f(x)\cos \frac{n\pi}{l}xdx \\
    &b_n = \frac{1}{l}\int_{-l}^l f(x)\sin \frac{n\pi}{l}xdx
\end{split}
$$

## 有限区间上函数的傅里叶级数
对在 $[a,b]$ 定义的函数 $f(x)$ 的傅里叶级数，可以将 $f(x)$ 延拓成以 $T = b-a$ 为周期的函数

### 在 $[0,l]$ 上的正弦型级数
**方法：** 将 $f(x)$ 奇延拓成 $[-l, l]$ 上的奇函数
$$
g(x) = \begin{cases}
    f(x) & x \in [0, l] \\
    -f(x) & x \in [-l, 0)
\end{cases}
$$
则 $g(x)$ 在 $[-l, l]$ 上的 $F-$ 级数就是 $f(x)$ 在 $[0, l]$ 上正弦型级数。
$$
b_n = \frac{2}{l} \int_0^l f(x) \sin \frac{n\pi}{l}xdx
$$
$$
\sum\limits_{n=1}^\infty b_n \sin \frac{n\pi}{l}x = \begin{cases}
\begin{gather*}
    \frac{1}{2}\left[f(x^+) + f(x^-)\right] &x\in (0, l) \\
    0 & x=0,l
\end{gather*}
\end{cases}
$$