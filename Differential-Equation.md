---
title: 微分方程
date: 2024-03-13 23:45:07
tags: [Math, Calculus]
---
# 高阶线性微分方程

# 常系数齐次线性微分方程
## 定义
在二阶齐次线性微分方程
$$
y'' + P(x)y' + Q(x)y = 0
$$
中，如果 $y'$，$y$ 的系数 $P(x)$，$Q(x)$ 均为常数
$$
y'' + py' + qy = 0
$$
其中 $p,q$ 是常数，那么称其为**二阶常系数齐次线性微分方程**。如果 $p,q$ 不全为常数，称其为**二阶变系数齐次线性微分方程**。

## 解法
称 $r^2 + pr + q=0$ 为微分方程的**特征方程**。

微分方程的通解有三种不同的情形
1. 特征方程有两个不相等的实根：$r_1 \neq r_2$

微分方程的通解为
$$
y = C_1 e^{r_1x} + C_2 e^{r_2x}
$$

2. 特征方程有两个相等的实根：$r_1 = r_2$

微分方程的通解为
$$
y = (C_1 + C_2x) e^{r_1x}
$$

3. 特征方程有一对共轭复根：$r_1 = \alpha + \beta i$，$r_2 = \alpha - \beta i$（$\beta \neq 0$）

此时微分方程的通解为
$$
y = e^{\alpha x}(C_1 \cos \beta x + C_2 \sin \beta x)
$$

## 拓展
**$n$ 阶常系数齐次线性微分方程**的一般形式是
$$
y^{(n)} + p_1 y^{(n-1)} + p_2 y^{(n-2)} + \cdots + p_{n-1}y' + p_n y = 0
$$
其中 $p_1,p_2,\cdots,p_{n-1},p_n$ 都是常数。

此时微分方程的特征方程为
$$
r^n + p_1 r^{n-1} + p_2 r^{n-2} + \cdots + p_{n-1} r + p_n = 0
$$

根据特征方程的根，可以写出其对应的微分方程的解如下：
| 特征方程的根 | 微分方程通解中的对应项 |
| --- | --- |
| $k$ 重实根 $r$ | $e^{rx}(C_1 + C_2x + \cdots + C_k x^{k-1})$ |
| 一对 $k$ 重复根 $r_{1,2} = \alpha \pm \beta i$ | $e^{\alpha x}[(C_1 + C_2x + \cdots + C_k x^{k-1})\cos \beta x + (D_1 + D_2 x + \cdots + D_k x^{k-1}) \sin \beta x]$ |
 
从代数学知道，$n$ 次代数方程有 $n$ 个根（重根按重数计算），而特征方程的每一个根都对应着通解中的一项，且每项各含一个任意常数，这样就得到 $n$ 阶常系数齐次线性微分方程的通解
$$
y = C_1 y_1 + C_2 y_2 + 
\cdots + C_n y_n
$$

# 常系数非齐次线性微分方程
1. $y'' + py' + qy = P_m(x)e^{\lambda x}$

$\lambda$ 为特征方程的 $k$ 重根，则设特解为
$$
y^* = x^k Q_m(x)e^{\lambda x}
$$

2. $y'' + py' + qy = e^{\lambda x}\left[P_l(x)\cos\omega x + \widetilde{P}_n(x)\sin\omega x\right]$

$\lambda \pm i\omega$ 为特征方程的 $k$ 重根，则设特解为
$$
y^* = x^k e^{\lambda x}\left[R_m(x)\cos\omega x + \widetilde{R}_m(x)\sin\omega x\right]
$$

# 欧拉方程
$$
x^n y^{(n)} + p_1 x^{n - 1}y^{(n - 1)} + \cdots + p_{n - 1}xy' + p_n y = f(x)
$$
令 $x = e^t$，即 $t = \ln x$