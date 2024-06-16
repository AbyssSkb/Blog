---
title: 静电场
date: 2024-06-15 20:00:00
tags: [Physics]
---
# 静电场
## 库仑定律
定义 $q_1$ 对 $q_2$ 施加的力
$$
\vec{F} = \frac{1}{4\pi\varepsilon_0} \frac{q_1 q_2}{r^2} \vec{e_r}
$$
其中 $\vec{e_r}$ 是由 $q_1$ 指向 $q_2$ 的单位向量

## 电场强度
描述电场中各点电场强弱和方向的物理量
$$
\vec{E} = \frac{\vec{F}}{q_0}
$$

具体到静电场中，拿点电荷来举例
$$
\vec{E} = \frac{\vec{F}}{q_0} = \frac{1}{4\pi\varepsilon_0}\frac{q}{r^2} \vec{e_r}
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

## 电场强度通量
描述通过电场中某个面的电场线数目的物理量
$$
\varPhi_e = \int_S \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{S}
$$

### 高斯定理
$$
\varPhi_e = \oint\limits_S \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{S} = \frac{1}{\varepsilon_0} Q_{in}
$$

## 电势能
由功能原理，静电场力对电荷所做的功就等于**电荷电势能增量的负值**
$$
W_{AB} = -(E_{pB} - E_{pA}) = E_{pA} - E_{pB}
$$
又因为
$$
W_{AB} = \int_{AB} q_0 \vec{E}\cdot \mathop{}\!\mathrm{d}\vec{l}
$$
令 $E_{pB} = 0$，则
$$
E_{pA} = \int_{AB} q_0 \vec{E} \cdot \mathop{}\!\mathrm{d}\vec{l}
$$

物理意义：把试验电荷 $q_0$ 从 $A$ 点移动到零电势能点处静电场力所做的功
### 静电场的环路定理
由于静电力是保守力，因此静电力做功仅于 $q_0$ 的始末位置有关，绕一圈的做功为零，由此可推出静电场的环路定理。
$$
\oint_l \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{l} = 0
$$

## 电势
令 $V_B = 0$，则 $A$ 点电势
$$
V_A = \int_{AB} \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{l}
$$

## 电势差
物理意义：将**单位正电荷**从 $A$ 移动到 $B$ 时电场力做的功
$$
U_{AB} = V_A - V_B = \int_{AB} \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{l}
$$

拿点电荷的电场来举例，令 $V_\infty = 0$，则
$$
\begin{split}
    V &= \int_r^\infty \frac{q}{4\pi\varepsilon_0r^2}\vec{e_r}\cdot\mathop{}\!\mathrm{d}\vec{l} \\
    &= \int_r^\infty \frac{q\mathop{}\!\mathrm{d}r}{4\pi\varepsilon_0r^2} \\
    &= \frac{q}{4\pi\varepsilon_0r}
\end{split}
$$

## 电场强度与电势梯度
由 $V_A = \int_A^B \vec{E} \cdot\mathop{}\!\mathrm{d}\vec{l}$ 可得
$$
\vec{E} = -\nabla V
$$

## 静电场中的电偶极子
我们定义电距
$$
\vec{p} = q \vec{r_0}
$$
$\vec{r_0}$ 为由 $-q$ 指向 $q$ 的距离向量

#### 轴线延长线上一点的电场强度
若 $x \gg r_0$，则
$$
\vec{E} = \frac{1}{4\pi\varepsilon_0}\frac{2\vec{p}}{x^3}
$$

#### 轴线中垂线上一点的电场强度
若 $y \gg r_0$，则
$$
\vec{E} = -\frac{1}{4\pi\varepsilon_0}\frac{\vec{p}}{y^3}
$$

#### 在匀强电场中受到的力
$$
\vec{F} = \vec{0}
$$

#### 受到的力矩
$$
\vec{M} = \vec{p} \times \vec{E}
$$

#### 电势能
$$
E_p = - \vec{p} \cdot \vec{E}
$$