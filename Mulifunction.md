---
title: 多元函数
date: 2024-03-05 14:57:05
tags: [Math, Calculus]
---
# 多元函数的基本概念
## N 维空间

称有序数组 $(x_1, x_2, \cdots, x_n)$ 为一个 **$n$ 维点（$n$ 维向量）**。所有 $n$ 维点组成的集合称之为 **$n$ 维空间**，记为 $\mathbb{R}^n$。

## N 维空间的距离

设 $A(x_1, x_2, \cdots, x_n)$ 和 $B(y_1, y_2, \cdots, y_n)$ 为 $\mathbb{R}^n$ 空间上任意两点，称
$$
\rho(A, B) = \sqrt{(x_1 - y_1)^2 + (x_2 - y_2)^2 + \cdots + (x_n - y_n)^2}
$$
为 $A, B$ **两点间的距离**。

## 邻域

设 $\alpha = (a_1, a_2, \cdots, a_n) \in \mathbb{R}^n$，$\delta$ 是某一正数，则 $n$ 维空间内的点集
$$
U(a, \delta) = \{x|x\in \mathbb{R}^n, \rho(x, a) < \delta\}
$$
就定义为 $\mathbb{R}^n$ 中点 $a$ 的 $\delta$ **邻域**。

记 $\mathring{U}(a, \delta)$ 为不含 $a$ 点的**去心邻域**。

## 内点、界点和聚点

- 内点：设 $D \subset \mathbb{R}^n$，$P_0 \in \mathbb{R}^n$，若存在 $P_0$ 的一个邻域使此邻域属于 $D$，称 $P_0$ 为 $D$ 的**内点**。

- 界点：设 $D \subset \mathbb{R}^n$，$P_0 \in \mathbb{R}^n$，若对 $P_0$ 的任何邻域总有 $D$ 中的点且总有 $D$ 外的点，则称 $P_0$ 为 $D$ 的**界点**。

- 聚点：$\forall \delta > 0$，点 $P_0$ 的去心邻域 $\mathring{U}(P_0, \delta)$ 中总有 $D$ 中的无穷多个点，称 $P_0$ 为集合 $D$ 的一个**聚点**。

## 其他
- 边界：界点的全体称为 $D$ 的**边界**。
- 开集：由全部内点组成的集合称为**开集**。
- 开区域：连通的开集称为**开区域**。
- 闭区域：开区域 `+` 边界 `=` **闭区域**。
- 有界集：对平面点集 $E$，若 $\exist r > 0$，$E \subset U(O, r)$，$O$ 为坐标原点，称 $E$ 为**有界集**。
# 多元函数的极限

## 定义
设 $z = f(P) = f(x, y)$ 在 $D$ 上有定义，$P_0(x_0, y_0)$ 为 $D$ 的一聚点，$A$ 是一实数，若对 $\forall \varepsilon > 0$，存在 $\delta > 0$，使得当 $0 < \rho(P, P_0) < \delta$ 时，恒有
$$
\left\vert f(P) - A \right\vert = \left\vert f(x, y) - A \right\vert < \varepsilon
$$
则称二元函数 $f(x, y)$ 在点 $P_0$ 处有**二重极限**。

记 $\lim\limits_{P \to P_0} f(P) = \lim\limits_{(x, y) \to (x_0, y_0)} f(x, y) = \lim\limits_{x \to x_0 \atop y \to y_0} f(x, y) = A$

## 性质
$\lim\limits_{x \to x_0 \atop y \to y_0} f(x, y)$ 存在 $\Leftrightarrow$ 点 $P(x, y)$ 沿任何方向、任何路径趋向于 $P_0(x_0, y_0)$ 时，极限都存在且相等。

# 连续

## 定义
设 $(x_0, y_0)$ 是 $D$ 的聚点，$z = f(x, y)$ 在 $D$ 上有定义，且 $\lim\limits_{x \to x_0 \atop y \to y_0} f(x, y) = f(x_0, y_0)$ 或 $\lim\limits_{\Delta x \to 0 \atop \Delta y \to 0}\left[f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0)\right] = 0$，则称 $f(x, y)$ 在点 $(x_0, y_0)$ 处**连续**。

## 性质
反函数性质去掉，其他的和一元函数相同。

# 偏导数
## 定义
设 $z = f(x,y)$ 在 $(x_0, y_0)$ 邻域内有定义，固定 $y= y_0$，若极限 $\lim\limits_{x\to x_0} \frac{f(x,y_0) - f(x_0, y_0)}{x-x_0} = \lim\limits_{\Delta x\to 0} \frac{f(x_0 + \Delta x, y_0) - f(x_0, y_0)}{\Delta x}$ 存在，则称 $f(x,y)$ 在点 $(x_0, y_0)$ 处关于 $x$ 的**偏导数**存在。

记为 $z'_x \Big| _{x=x_0\atop y=y_0} = f'_x(x_0, y_0) = f'_1(x_0, y_0) = \frac{\partial z}{\partial x}\Big|_{(x_0,y_0)}$ 

同样定义

$$
\begin{split}
    \lim\limits_{y\to y_0} \frac{f(x_0,y) - f(x_0, y_0)}{y-y_0} = \lim\limits_{\Delta y\to 0} \frac{f(x_0 , y_0+ \Delta y) - f(x_0, y_0)}{\Delta y} \\
    = z'_y \Big| _{x=x_0\atop y=y_0} = f'_y(x_0, y_0) = f'_2(x_0, y_0) = \frac{\partial z}{\partial y}\Big|_{(x_0,y_0)}
\end{split}
$$ 

设 $z=f(x,y)$ 在 $D$ 上每一点都有偏导，则其偏导又是 $D$ 上一个新的二元函数——称之为 $f(x,y)$ 在 $D$ 上的**偏导（函）数**。

记为 $z'_x = f'_x = f'_1 = \frac{\partial z}{\partial x}$；$z'_y = f'_y = f'_2 = \frac{\partial z}{\partial y}$。

## 几何意义
$f'_x(x_0, y_0)$ 表示曲线 $\begin{cases}
    y = y_0 \\
    z = f(x,y)
\end{cases}$ 在点 $(x_0, y_0, f(x_0, y_0))$ 处切线的斜率。

## 性质
若 $z = f(x,y)$ 的二阶混合偏导数 $f''_{xy}, f_{yx}''$ 都存在且连续，则 $f''_{xy} = f_{yx}''$。

# 全微分
## 定义
设 $z = f(x,y)$ 在 $(x_0, y_0)$ 邻域内有定义，$f(x,y)$ 的**全增量** $\Delta z = f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0)$ 可表示为 $\Delta z = A \Delta x + B \Delta y + o(\rho)$，其中 $A, B$ 为常数，$\rho = \sqrt{(\Delta x)^2 + (\Delta y)^2}$，则称 $f(x,y)$ 在点 $(x_0, y_0)$ 处**可微**，并称 $A\Delta x + B\Delta y$ 为 $f(x,y)$ 在点 $(x_0, y_0)$ 处的**全微分**。

记为 $dz$，即 $dz = A\Delta x + B\Delta y = Adx + Bdy$

## 性质
- 设 $z = f(x,y)$ 在 $(x_0, y_0)$ 点可微，则 $f(x,y)$ 在 $(x_0, y_0)$ 点处连续。

- 设 $z = f(x,y)$ 在 $(x_0, y_0)$ 点可微，则 $f(x,y)$ 在 $(x_0, y_0)$ 点处两个偏导数 $f'_x(x_0, y_0), f'_y(x_0, y_0)$ 都存在，且
$$
dz \Big|_{x=x_0\atop y=y_0} = f'_x(x_0, y_0)dx + f'_y(x_0, y_0)dy
$$

- 设 $z = f(x,y)$ 在 $(x_0, y_0)$ 点偏导数 $f'_x(x_0, y_0), f'_y(x_0, y_0)$ 都存在，且这两个偏导又在点 $(x_0, y_0)$ 处连续，则 $f(x,y)$ 在 $(x_0, y_0)$ 点可微。

## 几何意义
$z = f(x_0, y_0) + f'_x(x_0, y_0)(x-x_0) + f'_y(x_0, y_0)(y-y_0)$ 是一个平面。

该平面是过曲线 $\begin{cases}
    x = x_0 \\
    z = f(x,y)
\end{cases}$ 和 $\begin{cases}
    y = y_0 \\
    z = f(x,y)
\end{cases}$ 在点 $(x_0, y_0, f(x_0, y_0))$ 处两切线的平面。

# 复合函数
## 链式法则
设 $z = f(u, v)$ 可微，而 $u = \varphi(x,y),v=\psi(x,y)$ 偏导存在，则 $z$ 关于 $x$ 和 $y$ 的偏导数存在，且
$$
    \frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial x} = f'_u\varphi'_x + f'_v \psi'_x 
$$
$$
    \frac{\partial z}{\partial x} = \frac{\partial z}{\partial u} \cdot \frac{\partial u}{\partial x} + \frac{\partial z}{\partial v} \cdot \frac{\partial v}{\partial x} = f'_u\varphi'_x + f'_v \psi'_x
$$

## 全微分
设 $z = f(u,v),u=\varphi(x,y),v=\psi(x,y)$ 均可微，则不论将 $z$ 看成 $(u,z)$ 的函数还是 $(x,y)$ 的函数，其**微分形式不变**，即
$$
dz = \frac{\partial z}{\partial u} du + \frac{\partial z}{\partial v} dv = \frac{\partial z}{\partial x} dx + \frac{\partial z}{\partial y} dy
$$

# 隐函数
## 隐函数存在的微分法则
设 $F(x,y)$ 是 $(x_0,y_0)$ 邻域内满足
1. $F(x_0,y_0) = 0$
2. $F'_x(x,y),F'_y(x,y)$ 连续
3. $F'_y(x_0,y_0)\ne 0$

则方程 $F(x,y)=0$ 在 $(x_0,y_0)$ 邻域内能唯一确定 $y=f(x)$，且此函数连续可导，而 $\frac{dy}{dx} = -\frac{F'_x(x,y)}{F'_y(x,y)}$

### 推广
设 $F(x,y,z)$ 是 $(x_0,y_0,z_0)$ 邻域内满足
1. $F(x_0, y_0, z_0) = 0$
2. $F'_x(x,y,z),F'_y(x,y,z),F'_z(x,y,z)$ 连续
3. $F'_z(x_0,y_0,z_0) \ne 0$

则方程 $F(x,y,z) = 0$ 在 $(x_0,y_0,z_0)$ 邻域唯一确定一个单值函数 $z=f(x,y)$，且此函数连续可导，而
$$
\frac{\partial z}{\partial x} = -\frac{F'_x}{F'_z},\frac{\partial z}{\partial y} = -\frac{F'_y}{F'_z}
$$

## 方程组确定隐函数
### 存在准则
略，不常用且难记。
### 前置芝士
$n$ 个方程，$m$ 个变量组成方程组（$m>n$）能确定 $n$ 个 $m-n$ 元函数。
### 解法
求解的时候判断是一元函数还是多元函数，一元函数就求导，多元函数就求偏导，最后解方程组即可求出答案。

# 极值
## 二元函数的 `Taylor` 公式
若 $f(x,y)$ 在 $(x_0,y_0)$ 邻域内有 $n+1$ 阶连续偏导数，则称
$$
f(x_0 + \Delta x, y_0 + \Delta y) = f(x_0, y_0) + \frac{1}{1!}\left(\Delta x\frac{\partial}{\partial x} + \Delta y \frac{\partial}{\partial y}\right)f(x_0, y_0) + \frac{1}{2!}\left(\Delta x\frac{\partial}{\partial x} + \Delta y \frac{\partial}{\partial y}\right)^2f(x_0, y_0) + \cdots + \frac{1}{n!}\left(\Delta x\frac{\partial}{\partial x} + \Delta y \frac{\partial}{\partial y}\right)^nf(x_0, y_0) + \frac{1}{(n+1)!}\left(\Delta x\frac{\partial}{\partial x} + \Delta y \frac{\partial}{\partial y}\right)^{n+1}f(x_0+\theta\Delta x, y_0+\theta\Delta y),\theta \in (0,1)
$$
为 $f(x,y)$ 在 $(x_0, y_0)$ 点处 $n$ 阶 `Taylor` 公式。

## 二元函数极值
设 $z=f(x,y)$ 在 $(x_0,y_0)$ 邻域内有连续二阶偏导，且
$$
f'_x(x_0,y_0) = f'_y(x_0,y_0) = 0
$$
令 $A = f''_{xx}(x_0, y_0), B=f''_{xy}(x_0,y_0),C=f''_{yy}(x_0,y_0)$
1. 当 $\Delta = B^2 - AC >0$ 时，$f(x_0,y_0)$ 不是极值；
2. 当 $\Delta = B^2 - AC < 0$时，$f(x_0,y_0)$ 是极值。
    - 若 $A>0$（或 $C>0$）时，$f(x_0,y_0)$ 是极小值；
    - 若 $A<0$（或 $C<0$）时，$f(x_0,y_0)$ 是极大值。

## 条件极值
### 定义
若 $z = f(x,y)$ 为 $D$ 上的二元函数，求 $z=f(x,y)$ 在 $D$ 上满足条件 $g(x,y)=0$ 的极值称之为函数的**条件极值**。

### 拉格朗日乘数法
设 $f(x_1,x_2,\cdots,x_n)$ 为 $D$ 上 $n$ 元函数，$g_i(x_1, x_2, \cdots, x_n)=0$（$i = 1,2,\cdots,m$ 且 $m < n$）是 $D$ 上 $m$ 个条件，则 $f$ 在这 $m$ 个条件下极值（驻点）等价于（$m+n$）元函数
$$
F(x_1,x_2,\cdots,x_n,\lambda_1,\lambda_2,\cdots,\lambda_m) = f(x_1,x_2,\cdots,x_n) + \sum\limits_{i=1}^m \lambda_ig_i(x_1,x_2,\cdots,x_n)
$$
的无条件极值（驻点）。
# 关系图
|  | 连续 | 偏导 | 可微 | 方向导数 | 
| --- | --- | --- | --- | --- |
| 连续 | √ | × | × | × |
| 偏导 | × | √ | × | × |
| 可微 | √ | √ | √ | √ |
| 方向导数 | × | × | × | √ |