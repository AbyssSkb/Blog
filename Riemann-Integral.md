---
title: 黎曼积分
date: 2024-02-28 20:03:27
tags: [Math, Calculus]
description: 在实分析中，由黎曼创立的黎曼积分（英语：Riemann integral）首次对函数在给定区间上的积分给出了一个精确定义。黎曼积分在技术上的某些不足之处可由后来的黎曼－斯蒂尔杰斯积分和勒贝格积分得到修补。
---
# 黎曼积分
## 定义
设 $\Omega$ 为有限的几何体（一段曲线，一段曲面，一块有限空间体），$u = f(P)$ 是定义在 $\Omega$ 上的点函数，将 $\Omega$ 任意分成 $n$ 个小的几何体，$\Delta\Omega_1,\Delta\Omega_2,\cdots,\Delta\Omega_n$，并用此记号表示其几何量，称 $\sup\limits_{P_1, P_2 \in \Delta\Omega_i}\left\{\left\vert P_1P_2 \right\vert\right\} = d_i$ 为 $\Delta\Omega_i$ 的直径，$\lambda = \max\limits_{i=1,2,\cdots,n}\{d_i\}$，然后在每个小的几何形体 $\Delta\Omega_i$ 上做乘积 $f(P_i)\Delta\Omega_i, P_i \in \Delta\Omega_i$，并将它们加起来，得 $\sum_{i=1}^n f(P_i)\Delta\Omega_i$。如果不论 $\Omega$ 如何分，$P_i \in \Delta\Omega_i$ 如何取，下述极限 $\lim\limits_{\lambda \to 0} \sum_{i=1}^n f(P_i)\Delta\Omega_i$ 均存在且相等，则称 $f(P)$ 在 $\Omega$ 上可积，其极限值为 $f(P)$ 在 $\Omega$ 上黎曼积分。一般记号，$\lim\limits_{\lambda\to 0} \sum_{i=1}^n f(P_i)\Delta\Omega_i \triangleq \int\limits_\Omega f(P)d\Omega$

## 性质
1. $\int\limits_\Omega f(P)d\Omega = \int\limits_\Omega f(P)dV$，积分与变量无关
2. $\int\limits_\Omega d\Omega = \Omega$
3. $\int\limits_\Omega \left[\alpha f(P) \pm \beta g(P)\right]d\Omega = \alpha \int\limits_\Omega f(P)d\Omega \pm \beta\int\limits_\Omega g(P)d\Omega$
4. 若 $\Omega = \Omega_1 + \Omega_2$，则 $\int\limits_\Omega f(P) d\Omega = \int\limits_{\Omega_1} f(P) d\Omega + \int\limits_{\Omega_2} f(P)d\Omega$
5. 若 $f(P) \ge g(P), P \in \Omega$，则 $\int\limits_\Omega f(P) d\Omega \ge \int\limits_\Omega g(P)d\Omega$
6. 若 $P \in \Omega$，则 $\left\vert \int\limits_\Omega f(P)d\Omega \right\vert \le \int\limits_\Omega \left\vert f(P) \right\vert d\Omega$
7. 若 $m \le f(P) \le M, P \in \Omega$，则 $m\Omega \le \int\limits_\Omega f(P)d\Omega \le M\Omega$
8. 设 $f(P)$ 是有界闭区域 $\Omega$ 上连续函数，则 $\int\limits_\Omega f(P)d\Omega = f(P^*)\Omega, P^* \in \Omega$
9. 若 $\Omega$ 关于 $x=0(y=0,z=0)$ 对称，且 $f(P)$ 是关于 $x(y,z)$ 的奇函数，则 $\int\limits_\Omega f(P)d\Omega = 0$


## 一般意义
表示以 $f(P)$ 为密度函数的几何体 $\Omega$ 的质量代数和。

# 二重积分
## 定义
若 $D$ 是坐标面（不妨设为）$oxy$ 平面上的一个有界闭区域，在坐标系下 $f(P)$ 就是一个二元函数 $f(x,y)$，称它在 $D$ 上的黎曼积分为 $f(x,y)$ 在 $D$ 上的**二重积分**，记为
$$
\iint\limits_D f(x,y)d\sigma = \iint\limits_D f(x,y)dxdy
$$

## 物理意义
表示以 $f(x,y)$ 为面密度的有限平面区域质量的代数和。

## 几何意义
表示以 $D$ 为底，以 $z=f(x,y)$ 为顶的曲顶柱体体积的代数和。

## 计算公式
- $Y-$ 型：$\begin{cases}
    a \le y \le b \\
    \varphi(y) \le x \le \psi(y)
\end{cases}$
$$
\iint\limits_D f(x,y)dxdy = \int_a^b dy \int_{\varphi(y)}^{\psi(y)}f(x,y)dx
$$

- $X-$ 型：$\begin{cases}
    a \le x \le b \\
    \varphi(x) \le y \le \psi(x)
\end{cases}$
$$
\iint\limits_D f(x,y)dxdy = \int_a^b dx \int_{\varphi(x)}^{\psi(x)}f(x,y)dy
$$

- 极坐标系：$\begin{cases}
    \alpha \le \theta \le \beta \\
    \varphi(\theta) \le r \le \psi(\theta)
\end{cases}$
$$
\iint\limits_D f(x,y)dxdy = \int_\alpha^\beta d\theta \int_{\varphi(\theta)}^{\psi(\theta)}f(r\cos\theta, r\sin\theta)rdr
$$

## 积分换序
如果 $X-$ 型走不通，不妨用 $Y-$ 型试试。

# 三重积分
## 定义
若 $\Omega$ 是一有限空间体，$f(P)$ 是 $\Omega$ 上的点函数，在坐标系下 $f(P)$ 就是一个三元函数 $f(x,y,z)$，它在 $\Omega$ 上的黎曼积分称之为 $f(x,y,z)$ 在 $\Omega$ 上的**三重积分**，记为
$$
\iiint\limits_\Omega f(x,y,z)d\Omega = \iiint\limits_\Omega f(x,y,z)dxdydz
$$

## 物理意义
表示以 $f(x,y,z)$ 为体密度的有限空间体 $\Omega$ 质量的代数和。

## 计算方法
- 柱形域：$\begin{cases}
    \varphi(x,y) \le z \le \psi(x,y) \\
    (x,y) \in D_{xy}
\end{cases}$
$$
\iiint\limits_\Omega f(x,y,z) dxdydz = \iint\limits_{D_{xy}}dxdy \int_{\phi(x,y)}^{\psi(x,y)}f(x,y,z)dz
$$

- 片型域：$\begin{cases}
    a \le z \le b \\
    (x,y) \in D_z
\end{cases}$
$$
\iiint_\Omega f(x,y,z)dxdydz = \int_a^b dz\iint\limits_{D_z}f(x,y,z)dxdy
$$

- 球坐标系：$\begin{cases}
    a \le \theta \le b \\
    c \le \phi \le d \\
    g(\theta, \phi) \le \rho \le h(\theta, \phi)
\end{cases}$
$$
\iiint\limits_\Omega f(x,y,z)dxdydz = \int_a^b d\theta \int_c^d d\phi \int_{g(\theta, \phi)}^{h(\theta, \phi)} f(\rho\sin\phi\cos\theta, \rho\sin\phi\sin\theta, \rho\cos\phi)\rho^2\sin\phi d\rho
$$

# 第一型曲线积分
## 定义
若 $C$ 是空间（或平面）一有限曲线段，$f(P)$ 是 $C$ 上点函数，在引进坐标系下，$f(P) = f(x,y,z)(f(x,y))$，称 $f(P)$ 在 $C$ 上黎曼积分叫 $f$ 在 $C$ 上的**第一型曲线积分**，记为
$$
\int\limits_C f(x,y,z) ds \left(或\int\limits_C f(x,y)ds\right)
$$

## 物理意义
表示以 $f(x,y,z)$ 或 $f(x,y)$ 为线密度的曲线 $C$ 的质量的代数和。

## 几何意义
表示以 $C$ 为准线，母线平行于 $oz$ 轴的柱面介于 $oxy$ 平面与 $z=f(x,y)$ 之间面积的代数和。

## 计算方法
将曲线 $C$ 用参数方程来表示，然后代入积分公式转化成一元积分。

# 第一型曲面积分
## 定义
若 $S$ 是空间上一有限曲面，$f(P)$ 是 $S$ 上的点函数，在引进坐标系下，$f(P) = f(x,y,z)$，$f(P)$ 在 $S$ 上黎曼积分叫 $f(P)$ 在 $S$ 上的**第一型曲面积分**，记为
$$
\iint\limits_S f(x,y,z) dS
$$

## 物理意义
表示以 $f(x,y,z)$ 为面密度的曲面 $S$ 的质量的代数和。

## 计算方法
转化为二重积分
$$
\iint\limits_S f(x,y,z)dS = \iint\limits_D f(x,y,g(x,y)) \sqrt{g_x^{\prime\ 2} + g_y^{\prime\ 2} + 1} dxdy
$$