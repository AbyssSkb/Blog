---
title: 三角级数
date: 2024-03-02 14:44:43
tags: [Math, Series]
---
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