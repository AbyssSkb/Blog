---
title: 场
date: 2024-7-3 16:00:00
tags: [Math]
---
# 数量场
## 定义
若对于空间区域 $G$ 内任一点 $M$，都有一确定数量 $f(M)$ 与之对应，则称这个空间区域 $G$ 内确定了一个**数量场**

## 方向导数
### 定义
设 $u = f(P)$ 是定义在 $\Omega$ 上的一数量场，$P_0 \in \Omega$，以 $P_0$ 为始点作一射线，若方向与向量 $\vec{l}$ 一致，在此射线上任取一点 $P \neq P_0$，若极限
$$
\lim\limits_{P\to P_0}\frac{f(P) - f(P_0)}{\left\vert\overline{P_0P} \right\vert}
$$
存在，称此极限值为数量场 $u = f(P)$ 在点 $P_0$ 处沿 $\vec{l}$ 方向的方向导数，记为 $\frac{\partial u}{\partial \vec{l}}\big|_{P_0}$

### 计算
若数量场 $u = f(x,y,z)$ 在 $P_0$ 处可微，则其沿任何方向 $\vec{l} = (\cos\alpha, \cos\beta, \cos\gamma)$ 的方向导数都存在，且
$$
\frac{\partial u}{\partial\vec{l}}\big|{P_0}
 = f'_x\cos\alpha + f'_y\cos\beta + f'_z\cos\gamma = \operatorname{grad}u \cdot \vec{l}
$$
## 梯度
### 定义
设 $u = f(P)$ 是 $\Omega$ 上一数量场，$P_0$ 为 $\Omega$ 上任一点，若 $u = f(P)$ 在 $P_0$ 点处沿任何方向方向导数都存在，称以 $P_0$ 点处方向导数最大的方向为方向，以这个最大方向导数的模为模的向量为 $u = f(P)$ 在 $P_0$ 点的**梯度**，记为 $\operatorname{grad}u\big|_{P_0}$

### 计算
若 $u$ 可微，则
$$
\operatorname{grad}u = \left(\frac{\partial u}{\partial x},\frac{\partial u}{\partial y},\frac{\partial u}{\partial z}\right)
$$
# 向量场
## 定义
若对于空间区域 $\Omega$ 内任一点 $M$，都有一确定向量 $\vec{A}(M)$ 与之对应，则称这个空间区域 $G$ 内确定了一个**向量场**。

## 平均散发量
设 $\vec{A}$ 为一向量场，$\Omega$ 为一空间区域，$S$ 是 $\Omega$ 的边界闭曲面，方向为外法方向，称 $\oiint\limits_S Pdydz + Qdzdx + Rdxdy$ 为 $\vec{A}$ 在 $S$ 上的**总散发量（通量）**，而 $\frac{1}{\Omega} \oiint\limits_S Pdydz + Qdzdx + Rdxdy$ 为 $\vec{A}$ 在 $S$ 的**平均散发量**。

## 散度  
### 定义
设 $\vec{A}$ 为一向量场，$M$ 是空间上一点，做一个含 $M$ 点的空间区域 $\Delta\Omega$，$\Delta S$ 是 $\Delta\Omega$ 的边界闭曲面，若 $\lim\limits_{\Delta\Omega \to M}\frac{1}{\Delta\Omega}\oiint\limits_{\Delta S} Pdydz + Qdzdx + Rdxdy$（$\Delta S$ 为外法方向）存在，称此极限值为向量场 $\vec{A}$ 在 $M$ 点的**散度**，记为 $\operatorname{div}\vec{A}(M) = \nabla\cdot A$。

当 $\operatorname{div}\overrightarrow{A}(M) > 0$ 时，$M$ 点为 $\overrightarrow{A}$ 的**正源**

当 $\operatorname{div}\overrightarrow{A}(M) < 0$ 时，$M$ 点为 $\overrightarrow{A}$ 的**负源**

当 $\operatorname{div}\overrightarrow{A}(M) = 0$ 时，$M$ 点非 $\overrightarrow{A}$ 的源

### 计算
$$
\begin{split}
    \operatorname{div} \overrightarrow{A}(M_0)& = \left(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}\right)\Bigg|_{M_0} \\
    & = \nabla\cdot \overrightarrow{A}(M_0)
\end{split}
$$

## 环流面密度
### 定义
设 $\vec{A}$ 为一向量场，$M$ 为空间一点，以 $M$ 为始点做一向量 $\vec{n} = \{\cos \alpha, \cos\beta, \cos\gamma\}$，过 $M$ 点做空间一开曲面 $\Delta S$，要求此曲面在 $M$ 点的法相为 $\vec{n}$，设 $\Delta S$ 的边界曲线为 $\Delta C$，$\Delta S$ 与 $\Delta C$ 的方向感满足右手螺旋。若 $\lim\limits_{\Delta S \to M} \frac{1}{\Delta S} \oint\limits_{\Delta C} Pdx + Qdy + Rdz$ 存在，则称此极限值为 $\vec{A}$ 在 $M$ 点处沿方向 $\vec{n}$ 的**环流面密度**。
### 计算
若 $P$，$Q$，$R$ 具有连续偏导，则
$$
\lim\limits_{\Delta S \to M}\frac{1}{\Delta S} \oint\limits_{\Delta C} P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z = \begin{vmatrix}
        \cos\alpha & \cos\beta & \cos\gamma \\
        \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
        P & Q & R
    \end{vmatrix}_M = \operatorname{rot} \vec{A} \cdot \vec{n}
$$

## 旋度
### 定义
设 $\vec{A}$ 为一像向量场，$M$ 为场内一点，$M$ 点处存在这样一个向量 $\vec{H}$，此向量的方向是 $M$ 点环流面密度最大的方向，它的模是环流面密度最大的值，称 $\vec{H}$ 为像向量场 $\vec{A}$ 在 $M$ 点处的**旋度**，记为 $\operatorname{rot}\vec{A}(M) = \vec{H}$

### 计算
$$
\operatorname{rot}\vec{A}(M) = \begin{vmatrix}
    i & j & k \\
    \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
    P & Q & R
\end{vmatrix}_M
$$