---
title: 静电场
date: 2024-06-15 20:00:00
tags: [Physics]
---
# 静电场
## 库仑定律
定义 $q_1$ 对 $q_2$ 施加的力
$$
\overrightarrow{F} = \frac{1}{4\pi\varepsilon_0} \frac{q_1 q_2}{r^2} \overrightarrow{e_r}
$$
其中 $\overrightarrow{e_r}$ 是由 $q_1$ 指向 $q_2$ 的单位向量

## 电场强度
描述电场中各点电场强弱和方向的物理量
$$
\overrightarrow{E} = \frac{\overrightarrow{F}}{q_0}
$$

具体到静电场中，拿点电荷来举例
$$
\overrightarrow{E} = \frac{\overrightarrow{F}}{q_0} = \frac{1}{4\pi\varepsilon_0}\frac{q}{r^2} \overrightarrow{e_r}
$$

根据力的可叠加性，由此可以计算复杂带电体在空间某一点的电场强度

下面列出一些常见带电体的公式

### 均匀带电圆环轴线上的电场强度
$$
E = \frac{xQ}{4\pi\varepsilon_0 (x^2 + R^2)^{\frac{3}{2}}} = \frac{\lambda xR}{2\varepsilon_0 (x^2 + R^2)^{\frac{3}{2}}}
$$

### 无限大带电平面的场强
$$
E = \frac{\sigma}{2\varepsilon_0}
$$
### 无限长带电直线周围的电场
$$
E = \frac{\lambda}{2\pi\varepsilon_0 r}
$$

### 电偶极子的电场强度
我们定义电距
$$
\overrightarrow{p} = q \overrightarrow{r_0}
$$
$\overrightarrow{r_0}$ 为由 $-q$ 指向 $q$ 的距离向量

#### 轴线延长线上一点的电场强度
若 $x \gg r_0$，则
$$
\overrightarrow{E} = \frac{1}{4\pi\varepsilon_0}\frac{2\overrightarrow{p}}{x^3}
$$

#### 轴线中垂线上一点的电场强度
若 $y \gg r_0$，则
$$
\overrightarrow{E} = -\frac{1}{4\pi\varepsilon_0}\frac{\overrightarrow{p}}{y^3}
$$

### 电场强度通量
描述通过电场中某个面的电场线数目的物理量
$$
\varPhi_e = \int_S \overrightarrow{E} \cdot\mathop{}\!\mathrm{d}\overrightarrow{S}
$$

### 高斯定理
$$
\varPhi_e = \oint\limits_S \overrightarrow{E} \cdot\mathop{}\!\mathrm{d}\overrightarrow{S} = \frac{1}{\varepsilon_0} Q_{in}
$$

### 静电场的环路定理
由于静电力是保守力，因此静电力做功仅于 $q_0$ 的始末位置有关，绕一圈的做功为零，由此可推出静电场的环路定理。
$$
\oint_l \overrightarrow{E} \cdot\mathop{}\!\mathrm{d}\overrightarrow{l} = 0
$$

## 电势
令 $V_B = 0$，则 $A$ 点电势
$$
V_A = \int_{AB} \overrightarrow{E} \cdot\mathop{}\!\mathrm{d}\overrightarrow{l}
$$

## 电势差
物理意义：将**单位正电荷**从 $A$ 移动到 $B$ 时电场力做的功
$$
U_{AB} = V_A - V_B = \int_{AB} \overrightarrow{E} \cdot\mathop{}\!\mathrm{d}\overrightarrow{l}
$$

拿点电荷的电场来举例，令 $V_\infty = 0$，则
$$
\begin{split}
    V &= \int_r^\infty \frac{q}{4\pi\varepsilon_0r^2}\overrightarrow{e_r}\cdot\mathop{}\!\mathrm{d}\overrightarrow{l} \\
    &= \int_r^\infty \frac{q\mathop{}\!\mathrm{d}r}{4\pi\varepsilon_0r^2} \\
    &= \frac{q}{4\pi\varepsilon_0r}
\end{split}
$$

由 $V_A = \int_A^B \overrightarrow{E} \cdot d\overrightarrow{l}$ 可得