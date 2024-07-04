---
title: 第二型积分
date: 2024-03-02 09:47:36
tags: [Math, Calculus]
---
# 第二型积分
## 定义
设 $\Omega$ 为空间上一有向几何体，即在 $\Omega$ 上每一点 $P$ 处都确定了一方向 $\overrightarrow{e_P}$，$P \in \Omega$，$\overrightarrow{A}(P)$ 为 $\Omega$ 上一向量值函数。首先，将 $\Omega$ 任意分成 $n$ 个有向几何体 $\Delta\Omega_1, \Delta\Omega_2, \cdots, \Delta\Omega_n$；然后在每一个有向几何体上做内积 $\overrightarrow{A}(P) \cdot \Delta\overrightarrow{\Omega_i}(i = 1, 2, \cdots, n), P_i \in \Delta\Omega_i$，$\Delta\overrightarrow{\Omega_i}$ 是以 $\Delta\Omega_i$ 的几何量为模，以 $P_i$ 点的方向为方向的向量，再将上述内积加起来得 $\sum\limits_{i=1}^n \overrightarrow{A}(P_i) \cdot \Delta\overrightarrow{\Omega_i}$。若无论 $\Omega$ 如何分，$P_i \in \Delta \Omega_i$如何取，极限 $\lim\limits_{\lambda\to 0}\sum\limits_{i=1}^n \overrightarrow{A}(P_i) \cdot \Delta \overrightarrow{\Omega_i}$，$\lambda = \max\{d_i \vert i = 1,2,\cdots, n\}$，$d_i$ 是 $\Delta \Omega_i$ 的直径，都存在且相等，则称此极限值为 $\overrightarrow{A}(P_i)$ 在 $\Omega$ 上给定方向 $\overrightarrow{e_P}$ 下的**第二型积分**，记为
$$
\lim\limits_{\lambda\to 0} \sum\limits_{i=1}^n \overrightarrow{A}(P_i) \cdot \Delta\overrightarrow{\Omega_i} \triangleq \int\limits_\Omega \overrightarrow{A} (P)\mathop{}\!\mathrm{d} \overrightarrow{\Omega}
$$

## 性质

# 第二型曲线积分
## 定义
设 $C$ 是空间一有向曲线，其方向为其切线给定方向，引入直角坐标，$\overrightarrow{A}(P) = \left\{P(x,y,z),\ Q(x,y,z),\ R(x,y,z)\right\}$ 是 $C$ 上连续函数，则
$$
\mathop{}\!\mathrm{d}\Omega \cos\alpha_P =\mathop{}\!\mathrm{d}x,\quad\mathop{}\!\mathrm{d}\Omega\cos\beta_P =\mathop{}\!\mathrm{d}y,\quad\mathop{}\!\mathrm{d}\Omega\cos \gamma_P =\mathop{}\!\mathrm{d}z
$$
称 $\int\limits_C \overrightarrow{A}(P)\mathop{}\!\mathrm{d}\overrightarrow{\Omega} = \int\limits_C P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z$ 为 $\overrightarrow{A}(x,y,z)$ 在 $C$ 上给定方向的**第二型曲线积分**。

## 计算方法
### 参数法
设曲线 $C$ 为 $\begin{cases}
    x = x(t) \\
    y = y(t) \\
    z = z(t)
\end{cases}$ 始点 $t=a$，终点 $t=b$，$C$ 为光滑曲线，则
$$
\begin{split}
    \int\limits_C P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z & = \int_a^b P\mathop{}\!\mathrm{d}x(t) + Q\mathop{}\!\mathrm{d}y(t) + R\mathop{}\!\mathrm{d}z(t) \\
    & =\int_a^b \left[P x'(t) + Qy'(t) + Rz'(t)\right]dt
\end{split}
$$
### 格林公式
设 $D$ 为单连通区域，$C$ 为 $D$ 的边界闭曲线，其方向为**正向**。$P(x,y), Q(x,y)$ 是 $C+D$ 上具有连续一阶偏导的函数，则
$$
\oint\limits_C P(x,y)\mathop{}\!\mathrm{d}x + Q(x,y)\mathop{}\!\mathrm{d}y = \oiint\limits_D \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right)\mathop{}\!\mathrm{d}x\mathrm{d}y
$$
#### 推广
设曲线 $C$ 是由 $n+1$ 条简单连续、逐段光滑闭曲线 $C_0, C_1, \cdots, C_n$ 组成，其中 $C_1, \cdots, C_n$ 互不相交，每条都在其余 $n-1$ 条外部区域内，而它们全体又在 $C_0$ 所围区域内部。$C_0$ 与 $C_1, \cdots, C_n$ 所界定区域为 $D$，$C$ 的方向对 $D$ 而言为**左手域方向**，而 $P(x,y), Q(x,y)$ 又是 $C+D$ 上具有连续一阶偏导的函数，则
$$
\oint\limits_C P(x,y)\mathop{}\!\mathrm{d}x + Q(x,y)\mathop{}\!\mathrm{d}y = \oiint\limits_D \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right)\mathop{}\!\mathrm{d}x\mathrm{d}y
$$

### 斯托克斯公式
设 $C$ 为分段光滑有向闭曲线，$S$ 是以 $C$ 为边界的任一分片光滑的有向曲面，$C$ 与 $S$ 的方向满足**右手螺旋方向**，函数 $P(x,y,z), Q(x,y,z), R(x,y,z)$ 是 $S+C$ 上具有连续偏导的函数，则
$$
\begin{split}
    \oint\limits_C P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z & =\iint\limits_S \left(\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z}\right)\mathop{}\!\mathrm{d}y\mathrm{d}z + \left(\frac{\partial P}{\partial z} - \frac{\partial R}{\partial x}\right)\mathop{}\!\mathrm{d}z\mathrm{d}x + \left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right)\mathop{}\!\mathrm{d}x\mathrm{d}y \\
    & = \iint\limits_S \begin{vmatrix}
       \mathop{}\!\mathrm{d}y\mathrm{d}z &\mathop{}\!\mathrm{d}z\mathrm{d}x &\mathop{}\!\mathrm{d}x\mathrm{d}y \\
        \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
        P & Q & R
    \end{vmatrix} \\
    & = \iint\limits_S \begin{vmatrix}
        \cos\alpha & \cos\beta & \cos\gamma \\
        \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
        P & Q & R
    \end{vmatrix}\mathop{}\!\mathrm{d}S
\end{split}
$$
## 平面曲线积分与路径无关
设 $D$ 为单连通区域，$P, Q$ 为 $D$ 上具有连续一阶偏导的函数，在 $D$ 上下述四结论等价：
1. $D$ 上任意闭曲线 $C$，有 $\oint\limits_C P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y = 0$
2. $D$ 上第二型曲线积分 $\int\limits_{AB} P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y$ 与路径无关
3. $P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y$ 是全微分
4. $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$

## 全微分方程
### 定义
如果一阶微分方程 $P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y = 0$ 满足 $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$，则称此方程为**全微分方程（恰当方程）**。

### 解法
$$
\begin{split}
    通解公式\ u(x,y) = & \int_{(x_0, y_0)}^{(x,y)} P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y = C \\
    & \int_{x_0}^x P(x,y_0)\mathop{}\!\mathrm{d}x + \int_{y_0}^y Q(x,y)\mathop{}\!\mathrm{d}y = C
\end{split}
$$

**更一般地**，方程两端乘以一个因子 $u(x,y)$ 才可以变成全微分方程。

## 空间曲线积分与路径无关
设 $\Omega$ 为空间二维单连通区域，$P, Q, R$ 为 $\Omega$ 上具有连续一阶偏导的函数，在 $\Omega$ 上下述四结论等价：
1. $\Omega$ 上任意闭曲线 $C$，有 $\oint\limits_C P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z = 0$
2. $\Omega$ 上第二型曲线积分 $\int_{AB} P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z$ 与路径无关
3. $P\mathop{}\!\mathrm{d}x + Q\mathop{}\!\mathrm{d}y + R\mathop{}\!\mathrm{d}z$ 是全微分
4. $\frac{\partial R}{\partial y} = \frac{\partial Q}{\partial z}, \frac{\partial P}{\partial z} = \frac{\partial R}{\partial x}, \frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
# 第二型曲面积分
## 定义
设 $S$ 是空间一有向曲面，其方向 $\overrightarrow{n_P}, P \in S$ 为给定 $S$ 上一法向，$\overrightarrow{A}(P) = \{P(x,y,z),Q(x,y,z),R(x,y,z)\}$ 是 $S$ 上连续函数，则
$$
d\Omega \cos\alpha_P =\mathop{}\!\mathrm{d}y\mathrm{d}z,\quad\mathop{}\!\mathrm{d}\Omega\cos\beta_P =\mathop{}\!\mathrm{d}z\mathrm{d}x,\quad\mathop{}\!\mathrm{d}\Omega\cos \gamma_P =\mathop{}\!\mathrm{d}x\mathrm{d}y
$$
称 $\int\limits_S \overrightarrow{A}(P)\mathop{}\!\mathrm{d}\overrightarrow{\Omega} = \int\limits_S P\mathop{}\!\mathrm{d}y\mathrm{d}z + Q\mathop{}\!\mathrm{d}z\mathrm{d}x + R\mathop{}\!\mathrm{d}x\mathrm{d}y$ 为 $\overrightarrow{A}(x,y,z)$ 在 $S$ 上给定一侧的**第二型曲面积分**。

## 计算方法
### 分面计算法
$$
\iint\limits_S R\mathop{}\!\mathrm{d}x\mathrm{d}y = \begin{cases}
    \iint\limits_{D_{xy}} R(x, y, g(x,y))\mathop{}\!\mathrm{d}x\mathrm{d}y & S为上侧 \\
    -\iint\limits_{D_{xy}} R(x,y, g(x,y))\mathop{}\!\mathrm{d}x\mathrm{d}y & S为下侧
\end{cases}
$$

$$
\iint\limits_S P\mathop{}\!\mathrm{d}y\mathrm{d}z = \begin{cases}
    \iint\limits_{D_{yz}} P(g(y,z), y, z)\mathop{}\!\mathrm{d}y\mathrm{d}z & S为前侧 \\
    -\iint\limits_{D_{yz}} R(g(y, z), y, z)\mathop{}\!\mathrm{d}y\mathrm{d}z & S为后侧
\end{cases}
$$

$$
\iint\limits_S Q\mathop{}\!\mathrm{d}z\mathrm{d}x = \begin{cases}
    \iint\limits_{D_{xz}} Q(x, g(x, z), z)\mathop{}\!\mathrm{d}x\mathrm{d}y & S为右侧 \\
    -\iint\limits_{D_{xz}} Q(x, g(x, z), z)\mathop{}\!\mathrm{d}x\mathrm{d}y & S为左侧
\end{cases}
$$

### 投影法
$$
\begin{split}
    \iint\limits_S P\mathop{}\!\mathrm{d}y\mathrm{d}z + Q\mathop{}\!\mathrm{d}z\mathrm{d}x + R\mathop{}\!\mathrm{d}x\mathrm{d}y & =\iint\limits_S \left[P\left(-\frac{\partial z}{\partial x}\right) + Q\left(-\frac{\partial z}{\partial y}\right) + R\right]\mathop{}\!\mathrm{d}x\mathrm{d}y \\
    & = \pm \iint\limits_D \left[P\left(-\frac{\partial z}{\partial x}\right) + Q\left(-\frac{\partial z}{\partial y}\right) + R\right]\mathop{}\!\mathrm{d}x\mathrm{d}y
\end{split}
$$

### 高斯公式
设**空间二维单连通**区域 $\Omega$ 的边界 $S$ 是光滑的，其方向为**外法方向**，函数 $P(x,y,z)$，$Q(x,y,z)$，$R(x,y,z)$ 在 $\Omega$ 上具有连续一阶偏导数，则有
$$
\oiint\limits_S P\mathop{}\!\mathrm{d}y\mathrm{d}z + Q\mathop{}\!\mathrm{d}z\mathrm{d}x + R\mathop{}\!\mathrm{d}x\mathrm{d}y = \iiint\limits_\Omega \left(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}\right)\mathop{}\!\mathrm{d}\Omega
$$

#### 推广
设 $S$ 是由两个闭曲面 $S_1, S_2$ 组成，$S_1$ 的方向为外法方向，$S_2$ 的方向为内法方向，且 $S_2$ 在 $S_1$ 所围区域内部，介于 $S_1, S_2$ 之间区域为 $\Omega$，函数 $P(x,y,z), Q(x,y,z), R(x,y,z)$ 在 $\Omega$ 与 $S$ 上具有连续一阶偏导数，则有
$$
\oiint\limits_S P\mathop{}\!\mathrm{d}y\mathrm{d}z + Q\mathop{}\!\mathrm{d}z\mathrm{d}x + R\mathop{}\!\mathrm{d}x\mathrm{d}y = \iiint\limits_\Omega \left(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}\right)\mathop{}\!\mathrm{d}\Omega
$$