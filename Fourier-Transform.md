---
title: 傅里叶变换
date: 2024-11-16 8:00:00
tags: [Math, Complex analysis]
---

# 傅里叶变换

## 傅里叶级数的物理含义

$$
f_T(t) = A_0 + \sum\limits_{n=1}^{+\infty} A_n \cos(n\omega_0t + \theta_n)
$$
**含义**：周期信号可以分解为一系列**固定频率**的简谐波之和。

## 傅里叶级数的三角形式

**Dirichlet 定理**：设 $f_T(t)$ 是以 $T$ 为周期的实值函数，且在区间 $[-\frac{T}{2}, \frac{T}{2}]$ 上满足如下条件（称为 Dirichlet 条件）：

1. 连续或只有有限个第一类间断点；
2. 只有有限个极值点。

则在 $f_T(t)$ 的**连续**点处有
$$
f_T(t) = \frac{a_0}{2} + \sum\limits_{n=1}^{+\infty}(a_n\cos n\omega_0t + b_n\sin n\omega_0t)
$$
在**间断**处有
$$
\frac{1}{2}[f_T(t^+) + f_T(t^-)] = \frac{a_0}{2} + \sum\limits_{n=1}^{+\infty}(a_n\cos n\omega_0t + b_n\sin n\omega_0t)
$$

其中
$$
a_n = \frac{2}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}} f_T(t) \cos n\omega_0 tdt,\quad n = 0,1,2,\cdots \\
b_n = \frac{2}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}} f_T(t) \sin n\omega_0 tdt,\quad n = 1,2,\cdots \\
\omega_0 = \frac{2\pi}{T},\quad\text{称之为基频}
$$

## 傅里叶级数的指数形式

$$
f_T(t) = \sum\limits_{n=-\infty}^{+\infty} c_n e^{jn\omega_0t}
$$

其中
$$
c_n = \frac{1}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}}f_T(t) e^{-jn\omega_0 t}dt,\quad n=0,\pm1,\pm2,\cdots
$$

## 非周期函数的傅里叶变换

设函数 $f(t)$ 满足

1. 在 $(-\infty,+\infty)$ 上的任一有限区间内满足 Dirichlet 条件
2. 绝对可积，即 $\int_{-\infty}^{+\infty}|f(t)|dt < \infty$

则在 $f(t)$ 的**连续点**处，有
$$
f(t) = \frac{1}{2\pi}\int_{-\infty}^{+\infty}\left[\int_{-\infty}^{+\infty}f(t)e^{-j\omega t}dt \right]e^{j\omega t}d\omega
$$
称之为**傅里叶积分公式**，在 $f(t)$ 的间断处，公式的左端应为 $\frac{1}{2}[f(t^-)+f(t^+)]$

### 傅里叶积分公式

定义傅里叶正变换为
$$
F(\omega) = \int_{-\infty}^{+\infty} f(t)e^{-j\omega t}dt = \mathscr{F}[f(t)]
$$
定义傅里叶逆变换为
$$
f(t) = \frac{1}{2\pi} \int_{-\infty}^{+\infty}F(\omega)e^{j\omega t}d\omega = \mathscr{F}^{-1}[F(\omega)]
$$
其中，$F(\omega)$ 称为**象函数**，$f(t)$ 称为**象原函数**。$f(t)$ 与 $F(\omega)$ 称为**傅里叶变换对**，记为 $f(t) \leftrightarrow F(\omega)$

## 重要积分公式

$$
\int_{-\infty}^{+\infty} \frac{\sin ax}{x} dx = \begin{cases}
    \pi & a > 0 \\
    0 & a = 0 \\
    -\pi & a < 0 \\
\end{cases}
$$

## 单位脉冲函数

称满足
$$
\begin{split}
    &\delta(t) = \begin{cases}
        0 & t \neq 0 \\
        \infty & t = 0
    \end{cases} \\

    & \int_{-\infty}^{+\infty} \delta(t) dt = 1
\end{split}
$$
的函数叫单位脉冲函数，又叫 Dirac 函数或者 $\delta$ 函数。

### 极限方式的定义

令
$$
\delta_\varepsilon(t) = \begin{cases}
    \frac{1}{\varepsilon} & 0 \le t \le \varepsilon \\
    0 & 其他
\end{cases}
$$
则 $\delta(t) = \lim\limits_{\varepsilon \to 0}\delta_\varepsilon(t)$

### 性质

1. **筛选性质**：设 $f(t)$ 是任意函数，若 $f(t)$ 在 $t = t_0$ 处连续，则 $\int_{-\infty}^{+\infty}\delta(t-t_0)f(t)dt = f(t_0)$
2. **缩放性质**：设 $a\in R, a \neq 0$，则 $\delta(at) = \frac{1}{|a|}\delta(t)$
3. **导数性质**：设 $n \in N$，则 $\delta^{(n)}(-t) = (-1)^n\delta^{(n)}(t)$
4. $\delta(t)$ 为偶函数

## 常用傅里叶变换对

- $\delta(t) \leftrightarrow 1$
- $\delta(t-t_0) \leftrightarrow e^{-j\omega t_0}$
- $1 \leftrightarrow 2\pi\delta(\omega)$
- $e^{j\omega_0 t} \leftrightarrow 2\pi\delta(\omega - \omega_0)$
- $\operatorname{sgn}t \leftrightarrow \frac{2}{j\omega}$
- $u(t) \leftrightarrow \frac{1}{j\omega} + \pi\delta(\omega)$
- $\chi_{[-a, a]} \leftrightarrow 2 \frac{\sin a\omega}{\omega}, a>0$
- $u(t)e^{-\alpha t} \leftrightarrow \frac{1}{\alpha + j\omega}, \alpha>0$

## 傅里叶变换的性质

- **线性性质**：设 $a,b$ 为常数，则 $\mathscr{F}[af(t) + bg(t)] = aF(\omega) + bG(\omega)$。逆变换同理 $\mathscr{F}^{-1}[aF(\omega) + bG(\omega)] = af(t) + bg(t)$
- **缩放平移性质**
  1. $\mathscr{F}[f(at+b)](\omega) = \frac{1}{|a|}e^{\frac{jb\omega}{a}}F(\frac{\omega}{a})$
  2. $\mathscr{F}[e^{j\omega_0 t}f(t)] = F(\omega - \omega_0)$
- **微分性质**：若 $\lim\limits_{|t|\to +\infty}f^{(k)}(t) = 0$，（$k=0,1,2,\cdots,n-1$），则 $\mathscr{F}[f^{(n)}(t)]=(j\omega)^nF(\omega)$。同理，$\mathscr{F}^{-1}[F^{(n)}(\omega)] = (-jt)^n f(t)$
- **帕塞瓦尔等式**：$\int_{-\infty}^{+\infty}|f(t)|^2dt = \frac{1}{2\pi}\int_{-\infty}^{+\infty}|F(\omega)|^2 d\omega$，该定理表明信号在时域中的总能量和在频域中的总能量是相等的。

## 卷积

设函数 $f_1(t)$ 与 $f_2(t)$ 在区间 $(-\infty, +\infty)$ 上有定义，如果广义积分 $\int_{-\infty}^{+\infty}f_1(\tau)f_2(t-\tau)d\tau$ 对任何实数 $t$ 都收敛，则称此 $g(t) = f_1(t) * f_2(t) = \int_{-\infty}^{+\infty}f_1(\tau)f_2(t-\tau)d\tau$ 函数为 $f_1(t)$ 与 $f_2(t)$ 的**卷积**，记为 $f_1(t)*f_2(t)$

### 卷积的性质

1. **交换性质**：$f_1(t)*f_2(t) = f_2(t) * f_1(t)$
2. **结合性质**：$f_1(t)*[f_2(t)*f_3(t)] = [f_1(t)*f_2(t)]*f_3(t)$
3. **线性性质**：$g(t)*[af_1(t)+bf_2(t)]=ag(t)*f_1(t)+bg(t)*f_2(t)$

### 卷积定理

设 $\mathscr{F}[f_1(t)] = F_1(\omega)$，$\mathscr{F}[f_2(t)]=F_2(\omega)$，则有
$$
\mathscr{F}[f_1(t)*f_2(t)]=F_1(\omega)\cdot F_2(\omega) \\
\mathscr{F}^{-1}[F_1(\omega)*F_2(\omega)] = 2\pi f_1(t) \cdot f_2(t)
$$
