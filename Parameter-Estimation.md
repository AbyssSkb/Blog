---
title: 参数估计
date: 2024-11-27 08:00:00
tags: [Math, Statistics]
---

# 参数估计

设有一个统计总体，总体的分布函数为 $F(x,\theta)$，其中 $\theta$ 为未知参数。现从该总体取样本 $X_1,X_2,\cdots,X_n$，要依据样本对参数 $\theta$ 作出估计，或估计 $\theta$ 的某个已知函数 $g(\theta)$。这类问题称为**参数估计**。

## 点估计

由样本 $X_1,X_2,\cdots,X_n$ 确定一个统计量 $\hat{\theta} = \theta(X_1,X_2,\cdots,X_n)$ 用它估计总体的未知参数 $\theta$，称为总体参数的**估计量**。当具体的样本抽出后，可求出样本统计量的值 $\hat{\theta} = \theta(x_1,x_2,\cdots,x_n)$ 用它作为总体参数的**估计值**，称为总体参数的**点估计值**。

## 矩估计

**统计思想**：用样本矩估计总体矩，用样本矩函数估计总体矩函数。

**理论依据**：大数定律

**估计步骤**：设总体有 $m$ 个未知参数 $\theta_1,\theta_2,\cdots,\theta_m$，假定总体 $X$ 的前 $m$ 阶矩都存在。$X_1,X_2,\cdots,X_n$ 是来自总体的样本。

1. 求出总体 $X$ 的前 $m$ 阶原点矩
   $$
   \begin{cases}
   \alpha_1 = E(X) = q_1(\theta_1,\theta_2,\cdots,\theta_m) \\
   \alpha_2 = E(X^2) = D(X) + E^2(X) = q_2(\theta_1,\theta_2,\cdots,\theta_m) \\
   \vdots \\
   \alpha_m = E(X^m) = q_m(\theta_1,\theta_2,\cdots,\theta_m)
   \end{cases}
   $$

2. 解上面矩方程组，把未知参数用原点矩表示
   $$
   \begin{cases}
   \theta_1 = h_1(\alpha_1,\alpha_2,\cdots,\alpha_m) \\
   \theta_2 = h_2(\alpha_1,\alpha_2,\cdots,\alpha_m) \\
   \vdots \\
   \theta_m = h_m(\alpha_1,\alpha_2,\cdots,\alpha_m)
   \end{cases}
   $$

3. 用样本各阶原点矩 $A_1,A_2,\cdots,A_m$ 代替总体各阶原点矩 $\alpha_1,\alpha_2,\cdots,\alpha_m$，得到各参数的矩估计

   $\hat{\theta}_k = h_k(A_1,A_2,\cdots,A_m)$（$k=1,2,\cdots,m$），其中 $A_k = \frac{1}{n}\sum\limits_{i=1}^n X_i^k$

## 最大似然估计

**统计思想**：选择一组参数使得实验结果具有最大概率

### 离散型总体的似然函数

设离散型总体 $X$ 的分布列为
$$
P(X=x) = p(x;\theta_1,\cdots,\theta_m)
$$
$\theta_1,\cdots,\theta_m$ 为未知参数，$X_1,\cdots,X_n$ 为样本，其观察值为 $x_1,\cdots,x_n$，观察值 $(X_1=x_1,\cdots,X_n=x_n)$ 出现的概率为
$$
L(\theta_1,\cdots,\theta_m) = P\{X_1=x_1,\cdots,X_n=x_n \} = \prod\limits_{i=1}^n p(x_i;\theta_1,\cdots,\theta_m)
$$
称之为**似然函数**。

### 连续型总体的似然函数

设连续型总体 $X$ 的概率密度为 $f(x;\theta_1,\cdots,\theta_m)$，$\theta_1,\cdots,\theta_m$ 是未知参数，$X_1,\cdots,X_n$ 为样本，其观察值为 $x_1,\cdots,x_n$，样本 $X_1,\cdots,X_n$ 的联合概率密度
$$
L(\theta_1,\cdots,\theta_m) = f(x_1,\cdots,x_m) = \prod\limits_{i=1}^n f(x_i;\theta_1,\cdots,\theta_m)
$$
称之为**似然函数**。

### 最大似然估计

若统计量 $\hat{\theta}_1(X_1,\cdots,X_n),\cdots,\hat{\theta}_m(X_1,\cdots,X_n)$ 使得
$$
L(\hat{\theta}_1,\cdots,\hat{\theta}_m) = \max\limits_{\theta_1,\cdots,\theta_m}L(\theta_1,\cdots,\theta_m)
$$
则称 $\hat{\theta}_1(X_1,\cdots,X_n),\cdots,\hat{\theta}_m(X_1,\cdots,X_n)$ 为 $\theta_1,\cdots,\theta_m$ 的**最大似然估计量**。$\hat{\theta}_i(x_1,\cdots,x_n)$，$i=1,2,\cdots,m$ 为 $\theta_i$ 的**最大似然估计值**。

**估计步骤**：

1. 写出似然函数
   $$
   L = L(\theta_1,\theta_2,\cdots,\theta_m) = L(x_1,x_2,\cdots,x_n;\theta_1,\theta_2,\cdots,\theta_m)
   $$

2. 对似然函数取对数
   $$
   \ln{L} = \begin{cases}
   \sum\limits_{i=1}^n \ln{f}(x_i;\theta_1,\cdots,\theta_m) & 连续总体 \\
   \sum\limits_{i=1}^n \ln{P}(X_i=x_i;\theta_i,\cdots,\theta_m) & 离散总体
   \end{cases}
   $$

3. 建立似然方程
   $$
   \frac{\partial \ln L(\theta_1,\cdots,\theta_m)}{\partial\theta_j} = 0 \quad (j=1,\cdots,m)
   $$

4. 解似然方程，即可求出参数 $\theta_j$ 的最大似然估计。若似然函数不可微，用定义求。

## 区间估计

**定义1**：设总体 $X$ 的分布函数为 $F(x,\theta)$，$\theta$ 是未知参数，对给定 $\alpha$（$0<\alpha<1$），由样本 $X_1,\cdots,X_n$ 确定两个统计量
$$
\hat{\theta}_1 = \hat{\theta}_1(X_1,\cdots,X_n)\quad 和 \quad \hat{\theta}_2=\hat{\theta}_2(X_1,\cdots,X_n)
$$
使得
$$
P(\hat{\theta}_1<\theta < \hat{\theta}_2) \ge 1 - \alpha
$$
称 $(\hat{\theta}_1,\hat{\theta}_2)$ 为 $\theta$ 置信度为 $1-\alpha$ 的**置信区间**，$\hat{\theta}_1$ 和 $\hat{\theta}_2$ 分别称为**置信下限**和**置信上限**。

**定义2**：设总体 $X$ 的分布函数为 $F(x,\theta)$，$\theta$ 是未知参数，对给定 $\alpha$（$0<\alpha<1$），由样本 $X_1,\cdots,X_n$ 确定的统计量 $\hat{\theta}_L = \hat{\theta}_L(X_1,\cdots,X_n)$ 满足
$$
P(\theta>\hat{\theta}_L) \ge 1 - \alpha
$$
称 $\hat{\theta}_L$ 为 $\theta$ 的置信度为 $1-\alpha$ 的**单侧置信下限**。

若由样本确定的统计量 $\hat{\theta}_U=\hat{\theta}_U(X_1,\cdots,X_n)$ 满足
$$
P(\theta < \hat{\theta}_U) \ge 1 - \alpha
$$
称 $\hat{\theta}_U$ 为 $\theta$ 的置信度为 $1-\alpha$ 的**单侧置信上限**。

**估计步骤**：

1. 从 $\theta$ 的一个点估计 $\hat{\theta}$ 出发，构造 $\hat{\theta}$ 与 $\theta$ 的一个函数 $G(\hat{\theta},\theta)$，使得 $G$ 的分布已知且与 $\theta$ 无关。通常称函数 $G(\hat{\theta},\theta)$ 为**枢轴量**

2. 对给定的 $\alpha$，根据 $G$ 的分布找两个临界值 $c$ 和 $d$，使得
   $$
   P(c<G(\hat{\theta},\theta)<d)=1-\alpha
   $$

3. 从 $c<G(\hat{\theta},\theta)<d$ 解出 $\hat{\theta}_1<\theta<\hat{\theta}_2$。$\hat{\theta}_1,\hat{\theta}_2$ 为 $\theta$ 置信度为 $1-\alpha$ 的**置信区间**

## 单个正态总体参数的区间估计

设总体 $X\sim N(\mu,\sigma^2)$，$X_1,X_2,\cdots,X_n$ 为总体 $X$ 的样本，$\overline{X}$，$S^2$ 分别为样本均值，样本方差，置信度为 $1-\alpha$

### $\sigma$ 已知，求 $\mu$ 的置信区间

取枢轴量 $u=\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\sim N(0,1)$

则
$$
P\left(-u_{\frac{\alpha}{2}}<\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}<u_{\frac{\alpha}{2}}\right) = 1-\alpha
$$
解得 $\mu$ 的置信度为 $1-\alpha$ 的置信区间为
$$
\left(\overline{X}-u_{\frac{\alpha}{2}}\frac{\alpha}{\sqrt{n}}, \overline{X}+u_{\frac{\alpha}{2}}\frac{\alpha}{\sqrt{n}}\right)
$$
同理可得：

$\mu$ 的置信度为 $1-\alpha$ 单侧置信下限为 $\overline{X}-u_{\alpha}\frac{\alpha}{\sqrt{n}}$

$\mu$ 的置信度为 $1-\alpha$ 单侧置信上限为 $\overline{X}+u_{\alpha}\frac{\alpha}{\sqrt{n}}$

### $\sigma$ 未知，求 $\mu$ 的置信区间

取枢轴量 $t=\frac{\overline{X}-\mu}{S/\sqrt{n}}\sim t(n-1)$

则
$$
P\left(-t_{\frac{\alpha}{2}}(n-1) <\frac{\overline{X}-\mu}{S/\sqrt{n}}<t_{\frac{\alpha}{2}}(n-1) \right) = 1-\alpha
$$
解得 $\mu$ 的置信度为 $1-\alpha$ 的置信区间为
$$
\left(\overline{X}-t_{\frac{\alpha}{2}}(n-1) \frac{S}{\sqrt{n}}, \overline{X}+t_{\frac{\alpha}{2}}(n-1) \frac{S}{\sqrt{n}}\right)
$$
同理可得：

$\mu$ 的置信度为 $1-\alpha$ 单侧置信下限为 $\overline{X}-t_{\alpha}(n-1) \frac{S}{\sqrt{n}}$

$\mu$ 的置信度为 $1-\alpha$ 单侧置信上限为 $\overline{X}+t_{\alpha}(n-1) \frac{S}{\sqrt{n}}$

### 求 $\sigma^2$ 的置信区间

取枢轴量 $\chi^2 = \frac{(n-1)S^2}{\sigma^2}\sim \chi^2(n-1)$

则
$$
P\left(\chi^2_{1-\frac{\alpha}{2}}(n-1)<\frac{(n-1)S^2}{\sigma^2}<\chi^2_{\frac{\alpha}{2}}(n-1) \right) = 1-\alpha
$$
解得 $\sigma^2$ 的置信度为 $1-\alpha$ 的置信区间为
$$
\left(\frac{(n-1)S^2}{\chi^2_{\frac{\alpha}{2}}(n-1)}, \frac{(n-1)S^2}{\chi^2_{1-\frac{\alpha}{2}}(n-1)}\right)
$$
同理可得：

$\sigma^2$ 的置信度为 $1-\alpha$ 单侧置信下限为 $\frac{(n-1)S^2}{\chi^2_{\alpha}(n-1)}$

$\sigma^2$ 的置信度为 $1-\alpha$ 单侧置信上限为 $\frac{(n-1)S^2}{\chi^2_{1-\alpha}(n-1)}$

## 两个正态总体参数的估计

### $\sigma_1^2,\sigma_2^2$ 均已知，求 $\mu_1-\mu_2$ 的置信区间

$$
\overline{X}-\overline{Y} \sim N(\mu_1-\mu_2,\frac{\sigma^2_1}{n_1}+\frac{\sigma_2^2}{n_2})
$$

取枢轴量 $u=\frac{(\overline{X}-\overline{Y})-(\mu_1-\mu_2)}{\sqrt{\frac{\sigma^2_1}{n_1}+\frac{\sigma_2^2}{n_2}}}\sim N(0,1)$

### $\sigma_1^2=\sigma_2^2=\sigma^2$，但 $\sigma^2$ 未知，求 $\mu_1-\mu_2$ 的置信区间

用 $S^2_w = \frac{(n_1-1)S_1^2+(n_2-1)S_2^2}{n_1+n_2-2}$ 代替 $\sigma^2$ 的枢轴量
$$
t=\frac{(\overline{X}-\overline{Y})-(\mu_1-\mu_2)}{S_w\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}\sim t(n_1+n_2-2)
$$

### $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信区间

选枢轴量 $F = \frac{S_1^2/S_2^2}{\sigma_1^2/\sigma_2^2}\sim F(n_1-1,n_2-1)$
