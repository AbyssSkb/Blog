---
title: 留数
date: 2024-10-30 20:00:00
tags: [Math, Complex analysis]
---

# 留数

## 孤立奇点

设 $z_0$ 为 $f(z)$ 的奇点，且存在 $\delta > 0$，使得 $f(z)$ 在去心领域 $0 < |z-z_0| < \delta$ 内解析，则称 $z_0$ 为 $f(z)$ 的**孤立奇点**。

### 孤立奇点的分类

设 $z_0$ 为 $f(z)$ 的孤立奇点，将 $f(z)$ 在 $0 < |z-z_0| < \delta$ 内展开为洛朗级数：$f(z) = \sum\limits_{n=-\infty}^{+\infty} a_n(z-z_0)^n$，根据洛朗级数负幂次项的个数可以将孤立奇点分为以下三类：

- **可去奇点**：不含负幂次项
- **$N$ 阶极点**：含有限个负幂次项，且最高负幂次为 $N$
- **本性奇点**：含无限个负幂次项

### 判断孤立奇点类型的方法

-  **可去奇点**：$\lim\limits_{z\to z_0} f(z) = c$（常数）
- **极点**：$\lim\limits_{z\to z_0}f(z) = \infty$ 
- **本性奇点**：$\lim\limits_{z\to z_0}f(z)$ 不存在且不为 $\infty$

但是对于极点而言，上述方法无法判断阶数，虽然可以展开成洛朗级数后来判断，但是在有些情况下有更方便的方法。

### 判断极点阶数的其他方法

#### 方法一

若 $f(z)$ 在 $0 < |z-z_0| < \delta$ 内解析，则 $z_0$ 是 $f(z)$ 的 **$N$ 阶极点** 的**充要条件**是函数 $f(z)$ 在 $0 < |z-z_0| < \delta$ 内可以表示为
$$
f(z) = \frac{1}{(z-z_0)^N}g(z)
$$
的形式，其中函数 $g(z)$ 在 $z_0$ 点的邻域内解析，且 $g(z_0)\ne 0$

#### 方法二

$z_0$ 是 $f(z)$ 的 **$N$ 阶极点**的**充要条件**是 $z_0$ 是 $\frac{1}{f(z)}$ 的 $N$ 阶零点

#### 方法三

设函数 $f(z) = \frac{P(z)}{Q(z)}$，其中 $P(z)$ 和 $Q(z)$ 是区域 $D$ 上的解析函数。设点 $z_0$ 分别是 $P(z)$ 和 $Q(z)$ 的 $m$ 阶和 $n$ 阶零点，则

1. 若 $m<n$，则 $z_0$ 是 $f(z)$ 的 $m-n$ 阶极点。
2. 若 $m \ge n$，则 $z_0$ 是 $f(z)$ 的可去奇点。

对于方法二和方法三，涉及到**多阶零点**的概念，此处补充一下**多阶零点**的定义。

设函数 $f(z)$ 在 $z_0$ 处解析，则下列条件是等价的：

1. $z_0$ 为 $f(z)$ 的 $m$ 阶零点
2. $f^{(k)}(z_0)=0$，$k=0,1,2,\cdots,m-1$ 且 $f^{(m)}(z_0)\ne 0$
3. $f(z)$ 在 $|z-z_0| < \delta$ 内的泰勒展开式为

$$
\begin{split}
f(z) &= a_m(z-z_0)^m + a_{m+1}(z-z_0)^{m+1}+\cdots \\
	 &= (z-z_0)^m[a_m+a_{m+1}(z-z_0)+a_{m+1}(z-z_0)^2]+\cdots \\
	 &= (z-z_0)^m\varphi(z)
\end{split}
$$

​	其中，$a_m\ne 0$

## 无穷孤立奇点

如果函数 $f(z)$ 在无穷远点 $\infty$ 的去心邻域 $R < |z| < +\infty$ 内解析，则称**点 $\infty$ 为 $f(z)$ 的孤立奇点**。

### 分析无穷孤立奇点的方法

令 $z=\frac{1}{\xi}$，则点 $z=\infty$ 对应于点 $\xi = 0$。相应的，$f(z) = f(\frac{1}{\xi}) = \varphi(\xi)$。因此，函数 $f(z)$ 在无穷远点 $z=\infty$ 的性态可由函数 $\varphi(\xi)$ 在原点 $\xi = 0$ 的性态来刻画。 

### 无穷孤立奇点的分类

将 $f(z)$ 在 $R < |z| < +\infty$ 内展开为洛朗级数：$f(z) = \sum\limits_{n=-\infty}^{+\infty} a_n z^n$，根据洛朗级数正幂次项的个数可以将孤立奇点分为以下三类：

- **可去奇点**：不含正幂次项
- **$N$ 阶极点**：含有限个正幂次项，且最高正幂次为 $N$
- **本性奇点**：含无限个正幂次项

## 留数

### 有限孤立奇点处的留数定义

设 $z_0$ 为函数 $f(z)$ 的孤立奇点，将 $f(z)$ 在 $z_0$ 的去心邻域 $0 < |z-z_0| < \delta$ 内展开成洛朗级数：
$$
f(z) = \sum\limits_{n=-\infty}^{+\infty}a_n(z-z_0)^n = \cdots + \frac{a_{-1}}{z-z_0} + a_0 + a_1(z-z_0) + \cdots
$$
称 $a_{-1}$ 为 $f(z)$ 在 $z_0$ 处的**留数**，记作
$$
\operatorname{Res}[f(z),z_0] = a_{-1} = \frac{1}{2\pi i}\oint_C f(z)dz
$$
其中，$C$ 是 $z_0$ 的去心邻域内绕 $z_0$ 的一条正向简单闭曲线。

### 有限孤立奇点处的留数计算

根据留数的定义，针对不同类型的孤立奇点有不同的方法

- **可去奇点**：$\operatorname{Res}[f(z),z_0] = 0$

- **本性奇点**：没啥方法，老老实实展开成洛朗级数吧（

- **一阶极点**

若 $z_0$ 为 $f(z)$ 的一阶极点，则
$$
\operatorname{Res}[f(z),z_0] = \lim\limits_{z\to z_0} (z-z_0) f(z) 
$$
特别的，若 $f(z) = \frac{P(z)}{Q(z)}$，满足 $Q(z_0) = 0$，$Q'(z_0)\ne 0$，$P(z_0)\ne 0$，且$P(z)$，$Q(z)$ 在 $z_0$ 点解析，则
$$
\operatorname{Res}[f(z),z_0] = \frac{P(z_0)}{Q'(z_0)}
$$

- **$N$ 阶极点**

若 $z_0$ 为 $f(z)$ 的 $m$ 阶极点，则
$$
\operatorname{Res}[f(z),z_0] = \frac{1}{(m-1)!}\lim\limits_{z\to z_0}\frac{\operatorname{d}^{m-1}}{\operatorname{d}z^{m-1}}[(z-z_0)^mf(z)]
$$

### 无穷孤立奇点处的留数定义

设函数 $f(z)$ 在圆环域 $R<|z|<+\infty$ 内解析，则 $f(z)$ 在 $\infty$ 点的留数定义为：
$$
\operatorname{Res}[f(z),\infty]=\frac{1}{2\pi i}\oint_{C^-}f(z)dz = -a_{-1}
$$
其中，$C$ 为 $|z|=\rho>R$

### 无穷孤立奇点处的留数计算

$$
\operatorname{Res}[f(z),\infty] = -\operatorname{Res}[f(\frac{1}{z})\cdot\frac{1}{z^2},0]
$$

即转化为在有限孤立奇点处的留数计算。

## 留数基本定理

设 $f(z)$ 在区域 $D$ 内以及边界 $C$ 上除有限个孤立奇点 $z_1, z_2, \cdots, z_n$ 外处处解析，则
$$
\oint_C f(z) dz = 2\pi i\sum\limits_{k=1}^n \operatorname{Res}[f(z),z_k]
$$
设 $f(z)$ 在扩充平面上除有限个孤立奇点 $z_1,z_2, \cdots, z_n, \infty$ 外处处解析，则
$$
\sum\limits_{k=1}^n\operatorname{Res}[f(z),z_k] + \operatorname{Res}[f(z),\infty] = 0
$$

## 留数在定积分计算中的应用

### 形如 $\int_0^{2\pi} R(\cos\theta, \sin\theta)d\theta$ 的积分

> 要求 $R(u,v)$ 是 $u,v$ 的有理函数，且 $R(u,v)$ 在 $u^2+v^2=1$ 无奇点。

令 $z=e^{i\theta}$，则 $d\theta = \frac{dz}{iz}$，故积分转化为
$$
\begin{split}
\int_0^{2\pi} R(\cos\theta,\sin\theta)d\theta &= \oint_{|z|=1}R\left(\frac{z^2+1}{2z},\frac{z^2-1}{2iz} \right)\frac{1}{iz}dz \\
&= \oint_{|z|=1}f(z)dz \\
&= 2\pi i\sum\limits_k\operatorname{Res}[f(z),z_k]
\end{split}
$$
其中，$z_k$ 是 $f(z)$ 在 $|z|=1$ 内的孤立奇点。

### 形如 $\int_{-\infty}^{+\infty}R(x)dx$ 的积分

> 要求 $R(x)=\frac{P(x)}{Q(x)}$，其中 $P(x)$，$Q(x)$ 为多项式，$Q(x)$ 的次数比 $P(x)$ 的次数至少**高二次**，且 $Q(x)$ 无实零点。

$$
\int_{-\infty}^{+\infty}R(x)dx = 2\pi i\sum\limits_k\operatorname{Res}[R(z),z_k]
$$

其中，$z_k$ 是 $R(z)$ 在**上半平面**内的孤立奇点。

### 形如 $\int_{-\infty}^{+\infty}R(x)e^{iax}dx$（$a>0$）的积分

> 要求 $R(x)=\frac{P(x)}{Q(x)}$，其中 $P(x)$，$Q(x)$ 为多项式，$Q(x)$ 的次数比 $P(x)$ 的次数至少**高一次**，且 $Q(x)$ 无实零点。

$$
\begin{split}
\int_{-\infty}^{+\infty}R(x)e^{iaz}dx &= 2\pi i\sum\limits_k\operatorname{Res}[R(z)e^{iaz},z_k] \\
&= A + i B
\end{split}
$$

其中，$z_k$ 是 $R(z)$ 在**上半平面**内的孤立奇点。

特别的，$\int_{-\infty}^{+\infty}R(x)\cos{ax}dx = A$，$\int_{-\infty}^{+\infty}R(x)\sin{ax}dx = B$

### 关于第二、三型积分中 $R(z)$ 有实孤立奇点的情况

若 $R(z)$ 在上半平面有孤立奇点 $z_1,z_2,\cdots,z_m$，在**实轴**上有孤立奇点 $x_1,x_2,\cdots,x_n$，则
$$
\int_{-\infty}^{+\infty}f(z)dz = 2\pi i\sum\limits_{k=1}^m\operatorname{Res}[f(z),z_k] + \pi i\sum\limits_{k=1}^n\operatorname{Res}[f(z),x_k]
$$
其中，$f(z)$ 为第二、三型积分中的被积函数。
