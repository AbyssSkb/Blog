---
title: 数理统计
date: 2024-11-19 20:00:00
tags: [Math, Statistics]
---
# 数理统计

数理统计是以概率论为理论基础，研究怎样用**有效**的方法去收集、整理、分析带随机影响的**数据**，以便对所研究的问题给出估计和推断，为决策提供依据和建议。

## 总体和个体

- **总体**：研究对象的全体。
- **个体**：总体中每个成员。

根据总体中个体的数目是否有限可以把总体分为**有限总体**和**无限总体**。

## 样本

- **样本**：按一定规则从总体中抽取的一部分个体。
- **样本容量**：样本中所含个体的数目。
- **抽样**：抽取样本的过程。

## 简单随机样本

若 $X_1,X_2,\cdots,X_n$ 相互独立且与总体 $X$ 有相同的分布，则称 $X_1,X_2,\cdots,X_n$ 为来自总体 $X$ 的一个容量为 $n$ 的**简单随机样本**，简称为 $X$ 的一个样本。获得简单随机样本的抽样称为**简单随机抽样**。

样本 $(X_1,X_2,\cdots,X_n)$ 的每一个观察值 $(x_1,x_2,\cdots,x_n)$ 称为**样本值**或样本的一次实现。

样本值的集合称为**样本空间**。

## 三大分布

### $\chi^2$ 分布

设 $X_1, X_2, \cdots, X_n$ 相互独立，都服从标准正态分布 $N(0,1)$，则称随机变量
$$
Y = \sum\limits_{i=1}^nX_i^2
$$
服从自由度为 $n$ 的 $\chi^2$ 分布，记为 $Y \sim \chi^2(n)$

#### $\chi^2$ 分布的性质

1. 设 $X \sim \chi^2(n)$，则 $E(X)=n$，$D(X)=2n$
2. 设 $X_1,X_2,\cdots,X_m$ 独立，且 $X_i \sim \chi^2(n_i)$，则 $\sum\limits_{i=1}^m X_i \sim\chi^2(\sum\limits_{i=1}^m n_i)$

#### $\chi^2$ 分布的上侧 $\alpha$ 分位数或临界值

设 $\alpha(0<\alpha<1)$，称满足等式 $P(X\ge \chi_\alpha^2(n)) = \alpha$ 的点 $\chi_\alpha^2(n)$ 为 $\chi^2(n)$ 分布的上侧 $\alpha$ 分位数或临界值。

### $t$ 分布

设 $X,Y$ 相互独立，且 $X \sim N(0,1)$，$Y\sim \chi^2(n)$，则称随机变量
$$
T = \frac{X}{\sqrt{\frac{Y}{n}}}
$$
服从自由度为 $n$ 的 $t$ 分布，记为 $T \sim t(n)$

#### $t$ 分布的上侧 $\alpha$ 分位数或临界值

设 $\alpha(0<\alpha<1)$，称满足等式 $P(T\ge t_\alpha(n)) = \alpha$ 的点 $t_\alpha(n)$ 为 $t(n)$ 分布的上侧 $\alpha$ 分位数或临界值。

### $F$ 分布

设 $X,Y$ 相互独立，$X\sim\chi^2(n_1)$，$Y\sim\chi^2(n_2)$，则称随机变量
$$
F = \frac{X/n_1}{Y/n_2}
$$
服从第一自由度为 $n_1$，第二自由度为 $n_2$ 的 $F$ 分布，记为 $F\sim F(n_1,n_2)$

#### $F$ 分布的上侧 $\alpha$ 分位数或临界值

设 $\alpha(0<\alpha<1)$，称满足等式 $P(F\ge F_\alpha(n_1,n_2)) = \alpha$ 的点 $F_\alpha(n_1,n_2)$ 为 $F(n_1,n_2)$ 分布的上侧 $\alpha$ 分位数或临界值。

## 统计量

设 $X_1,X_2,\cdots,X_n$ 为总体 $X$ 的容量为 $n$ 的样本，$T(X_1,X_2,\cdots,X_n)$ 是定义在样本空间上，不含未知参数的连续函数，则称 $T(X_1,X_2,\cdots,X_n)$ 为一个统计量。

### 常用统计量

1. **样本均值**：$\overline{X} = \frac{1}{n}\sum\limits_{i=1}^n X_i$

2. **样本方差**：$S^2 = \frac{1}{n-1}\sum\limits_{i=1}^n(X_i - \overline{X})^2$

3. **样本标准差**：$S = \sqrt{\frac{1}{n-1}\sum\limits_{i=1}^n(X_i - \overline{X})^2}$

4. **样本 $k$ 阶原点矩**：$A_k = \frac{1}{n}\sum\limits_{i=1}^nX_i^k$

5. **样本 $k$ 阶中心原点矩**：$B_k = \frac{1}{n}\sum\limits_{i=1}^n(X_i-\overline{X})^k$

6. **顺序统计量**：设 $X_1, X_2, \cdots, X_n$ 为总体 $X$ 的一个样本，$X_1,X_2,\cdots,x_n$ 是样本值，将它们按大小次序排列，得
   $$
   x_{(1)} \le x_{(2)} \le \cdots \le x_{(n)}
   $$
   称 $X_{(i)}$ 为第 $i$ 个顺序统计量，如果不论样本 $X_1, X_2, \cdots, X_n$ 取哪组观测值 $x_1, x_2, \cdots, x_n$，$X_{(i)}$ 总是取 $x_{(i)}$ 为观测值，即
   $$
   X_{(1)} \le X_{(2)} \le \cdots \le X_{(n)}
   $$
   特别的，称 $X_{(1)}$ 为**最小顺序统计量**，$X_{(n)}$ 为**最大顺序统计量**。

7. **样本中位数**
   $$
   M = \begin{cases}
   X_{(\frac{n+1}{2})} & n为奇数 \\
   \frac{1}{2}\left[X_{(\frac{n}{2})} + X_{(\frac{n}{2}+1)} \right] & n为偶数
   \end{cases}
   $$

8. **样本极差**：$R=X_{(n)} - X_{(1)}$

## 抽样分布

当用统计量推断总体时，必须知道统计量的分布，统计量的分布属于样本函数的分布，人们把样本函数的分布统称为**抽样分布**。

## 单个正态总体统计量的分布

### 样本均值的分布

设 $X_1, X_2, \cdots, X_n$ 为总体 $N(\mu,\sigma^2)$ 的一个样本，样本均值 $\overline{X}=\frac{1}{n}\sum\limits_{i=1}^n X_i$，则
$$
\overline{X} \sim N(\mu,\frac{\sigma^2}{n})
$$

### 样本方差的分布

设 $X_1,X_2,\cdots,X_n$ 为总体 $N(\mu,\sigma^2)$ 的一个样本，样本方差 $S^2 = \frac{1}{n-1} \sum\limits_{i=1}^n (X_i-\overline{X})^2$，则

1. 样本方差 $S^2$ 与样本均值 $\overline{X}$ 相互独立；
2. $\frac{(n-1)S^2}{\sigma^2}\sim \chi^2(n-1)$

### 定理3

设 $X_1,X_2,\cdots,X_n$ 为总体 $N(\mu,\sigma^2)$ 的一个样本，$\overline{X}$ 和 $S^2$ 分别为样本均值和样本方差，则
$$
\frac{\sqrt{n}(\overline{X}-\mu)}{S} \sim t(n-1)
$$

## 两个正态总体统计量的分布

### 定理4

设 $X_1,X_2,\cdots,X_{n_1}$ 和 $Y_1,Y_2,\cdots,Y_{n_2}$ 分别是来自总体 $N(\mu_1,\sigma_1^2)$ 和 $N(\mu_2,\sigma_2^2)$ 的两个样本，它们**相互独立**，样本均值分别为 $\overline{X}$ 和 $\overline{Y}$，样本方差分别为 $S_1^2$ 和 $S^2_2$，则
$$
\frac{S_1^2/\sigma_1^2}{S_2^2/\sigma_2^2} \sim F(n_1-1,n_2-1)
$$
当 $\sigma_1^2=\sigma_2^2=\sigma^2$ 时
$$
\frac{\overline{X}-\overline{Y}-(\mu_1-\mu_2)}{S_w\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}} \sim t(n_1+n_2-2)
$$
其中
$$
S_w = \sqrt{\frac{(n_1-1)S_1^2+(n_2-1)S_2^2}{n_1+n_2-2}}
$$
