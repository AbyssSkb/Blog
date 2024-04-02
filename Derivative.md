---
title: 导数
date: 2024-03-12 13:43:17
tags: [Math, Calculus]
---
# 导数 
## 定义
设函数 $y = f(x)$ 在点 $x_0$ 的某个邻域内有定义，当自变量 $x$ 在 $x_0$ 处取得增量 $\Delta x$（点 $x_0 + \Delta x$ 仍在该邻域内）时，相应地，因变量取得增量 $\Delta y = f(x_0 + \Delta x) - f(x_0)$；如果 $\Delta y$ 与 $\Delta x$ 之比当 $\Delta x \to 0$ 时的极限存在，那么称函数 $y = f(x)$ 在点 $x_0$ 处**可导**，并称这个极限为函数 $y = f(x)$ 在点 $x_0$ 处的**导数**，记为 $f^\prime(x_0)$，即
$$
f^\prime (x_0) = \lim\limits_{\Delta x \to 0}\frac{\Delta y}{\Delta x} = \lim\limits_{\Delta x \to 0}\frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x}
$$
也可记作 $y^\prime |_{x=x_0}$，$\frac{dy}{dx}|_{x=x_0}$ 或 $\frac{df(x)}{dx}|_{x=x_0}$

如果函数 $y = f(x)$ 在开区间 $I$ 内的每点处都可导，那么就称函数 $f(x)$ 在开区间 $I$ 内可导。这是，对于任一 $x\in I$，都对应这 $f(x)$ 的一个确定的导数值。这样就构成了一个新的函数，这个函数叫做原来函数 $y = f(x)$ 的**导函数**，记作 $y^\prime$，$f^\prime(x)$，$\frac{dy}{dx}$ 或 $\frac{df(x)}{dx}$

函数 $f(x)$ 在 $x_0$ 处的**左导数**和**右导数**，记作 $f^\prime_-(x_0)$ 及 $f^\prime_+(x_0)$
$$
f^\prime_-(x_0) = \lim\limits_{h\to 0^-}\frac{f(x_0 + h) - f(x_0)}{h} \\
f^\prime_+(x_0) = \lim\limits_{h\to 0^+}\frac{f(x_0 + h) - f(x_0)}{h}
$$
函数 $f(x)$ 在点 $x_0$ 处可导的充分必要条件是左导数 $f^\prime_-(x_0)$ 和右导数 $f^\prime_+(x_0)$ 都存在且相等。

如果函数 $f(x)$ 在开区间 $(a, b)$ 内可导，且 $f^\prime_+(a)$ 及 $f^\prime_-(b)$ 都存在，那么就说 $f(x)$ 在**闭区间 $[a, b]$ 上可导**。

## 性质
如果函数 $y = f(x)$ 在点 $x$ 处可导，那么函数在该点必连续。

## 求导法则
**定理 $1\quad$** 如果函数 $u = u(x)$ 及 $v = v(x)$ 都在点 $x$ 具有导数，那么它们的和、差、积、商（除分母为零的点外）都在点 $x$ 具有导数，且
1. $\left[u(x) \pm v(x)\right]^\prime = u^\prime(x) \pm v^\prime(x)$
2. $\left[u(x)v(x)\right]^\prime = u^\prime(x) v(x) + u(x)v^\prime(x)$
3. $\left[\frac{u(x)}{v(x)}\right]^\prime = \frac{u^\prime(x)v(x) - u(x)v^\prime(x)}{v^2(x)}\quad(v(x) \ne 0)$

**定理 $2\quad$** 如果函数 $x = f(y)$ 在区间 $I_y$ 内单调、可导且 $f^\prime(y) \ne 0$，那么它的反函数 $y = f^{-1}(x)$ 在区间 $I_x = \{x | x = f(y), y\in I_y\}$ 内也可导，且
$$
\left[f^{-1}(x)\right]^\prime = \frac{1}{f^\prime(y)} \quad 或 \quad \frac{dy}{dx} = \frac{1}{\frac{dx}{dy}}
$$

**定理 $3\quad$** 如果 $u = g(x)$ 在点 $x$ 可导，而 $y = f(u)$ 在点 $u = g(x)$ 可导，那么复合函数 $y = f\left[g(x)\right]$ 在点 $x$ 可导，且其导数为
$$
\frac{dy}{dx} = f^\prime(u) \cdot g^\prime(x) \quad 或 \quad \frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
$$

## 隐函数的导数

## 由参数方程所确定的函数的导数

# 微分
## 定义
设函数 $y = f(x)$ 在某区间内有定义，$x_0$ 及 $x_0 + \Delta x$ 在这区间内，如果函数的增量
$$
\Delta y = f(x_0 + \Delta x) - f(x_0)
$$
可表示为
$$
\Delta y = A\Delta x + o(\Delta x)
$$
其中 $A$ 是不依赖于 $\Delta x$ 的常数，那么称函数 $y = f(x)$ 在点 $x_0$ 是**可微**的，而 $A\Delta x$ 叫做函数 $y = f(x)$ 在点 $x_0$ 相应于自变量增量 $\Delta x$ 的微分，记作 $dy$，即
$$
dy = A\Delta x
$$
函数 $f(x)$ 在点 $x_0$ 可微的充分必要条件是函数 $f(x)$ 在点 $x_0$ 可导，且当 $f(x)$ 在点 $x_0$ 可微时，其微分一定是
$$
dy = f^\prime(x_0)\Delta x
$$

函数 $y =f(x)$ 在任意点 $x$ 的微分，称为**函数的微分**，记作 $dy$ 或 $df(x)$，即
$$
dy = f^\prime (x)\Delta x
$$
通常把自变量 $x$ 的增量 $\Delta x$ 称为**自变量的微分**，记作 $dx$，即 $dx = \Delta x$，于是函数 $y = f(x)$ 的微分又可记作
$$
dy = f^\prime (x)dx
$$
从而有
$$
\frac{dy}{dx} = f^\prime(x)
$$

## 微分法则
1. 基本初等函数的微分公式
2. 函数和、差、积、商的微分法则
3. 复合函数的微分法则

# 微分中值定理
## 费马引理
设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内有定义，并且在 $x_0$ 处可导，如果对任意的 $x \in U(x_0)$，有
$$
f(x) \le f(x_0) \quad （或f(x) \ge f(x_0)）
$$
那么 $f^\prime(x_0) = 0$。
通常称导数等于零的点为函数的驻点（或稳定点，临界点）。

## 罗尔定理
如果函数 $f(x)$ 满足
1. 在闭区间 $[a, b]$ 上连续
2. 在开区间 $(a, b)$ 内可导
3. 在区间端点处的函数值相等，即 $f(a) = f(b)$

那么在 $(a, b)$ 内至少有一点 $\xi$（$a < \xi < b$），使得 $f^\prime(\xi) = 0$。

## 拉格朗日中值定理
如果函数 $f(x)$ 满足
1. 在闭区间 $[a, b]$ 上连续
2. 在开区间 $(a, b)$ 内可导

那么在 $(a, b)$ 内至少有一点 $\xi$（$a < \xi < b$），使等式
$$
f(b) - f(a) = f^\prime (\xi)(b - a)
$$
成立

## 柯西中值定理
如果函数 $f(x)$ 及 $F(x)$ 满足
1. 在闭区间 $[a, b]$ 上连续
2. 在开区间 $(a, b)$ 内可导
3. 对任一 $x\in (a, b), F^\prime(x) \ne 0$

那么在 $(a, b)$ 内至少有一点 $\xi$，使等式
$$
\frac{f(b) - f(a)}{F(b) - F(a)} = \frac{f^\prime(\xi)}{F^\prime(\xi)}
$$
成立

## 推论
如果函数 $f(x)$ 在区间 $I$ 上连续，$I$ 内可导且导数恒为零，那么 $f(x)$ 在区间 $I$ 上是一个常数。

# 洛必达法则
如果当 $x\to a$（或 $x\to\infty$）时，两个函数 $f(x)$ 与 $F(x)$ 都趋于零或都趋于无穷大，那么极限 $\lim\limits_{x\to a \atop (x \to \infty)} \frac{f(x)}{F(x)}$
可能存在、也可能不存在。通常把这种极限叫做**未定式**，并分别简记为 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$。

## 定理 1 
设
1. 当 $x\to a$ 时，函数 $f(x)$ 及 $F(x)$ 都趋于零
2. 在点 $a$ 的某去心邻域内，$f^\prime(x)$ 及 $F^\prime(x)$ 都存在且 $F^\prime(x) \ne 0$
3. $\lim\limits_{x\to a}\frac{f^\prime(x)}{F^\prime(x)}$ 存在（或为无穷大）

则
$$
\lim\limits_{x\to a}\frac{f(x)}{F(x)} = \lim\limits_{x\to a}\frac{f^\prime(x)}{F^\prime(x)}
$$

## 定理 2
设
1. 当 $x\to \infty$ 时，函数 $f(x)$ 及 $F(x)$ 都趋于零
2. 当 $\left\vert x \right\vert > N$ 时 $f^\prime(x)$ 及 $F^\prime(x)$ 都存在且 $F^\prime(x) \ne 0$
3. $\lim\limits_{x\to a}\frac{f^\prime(x)}{F^\prime(x)}$ 存在（或为无穷大）

则
$$
\lim\limits_{x\to \infty}\frac{f(x)}{F(x)} = \lim\limits_{x\to \infty}\frac{f^\prime(x)}{F^\prime(x)}
$$

# 泰勒公式
## 泰勒中值定理 1
如果函数 $f(x)$ 在 $x_0$ 处具有 $n$ 阶导数，那么存在 $x_0$ 的一个邻域，对于该邻域内的任一 $x$，有
$$
f(x) = f(x_0) + f^\prime(x_0)(x - x_0)+ \frac{f''(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + R_n(x)
$$
其中
$$
R_n(x) = o((x - x_0)^n)
$$
称其为**佩亚诺余项**。

## 泰勒中值定理 2
如果函数 $f(x)$ 在 $x_0$ 的某个邻域 $U(x_0)$ 具有 $(n + 1)$ 阶导数，那么对任一 $x \in U(x_0)$，有
$$
f(x) = f(x_0) + f^\prime(x_0)(x - x_0)+ \frac{f''(x_0)}{2!}(x-x_0)^2+\cdots+\frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + R_n(x)
$$
其中
$$
R_n(x) = \frac{f^{n + 1}(\xi  )}{(n + 1)!}(x - x_0)^{n + 1}
$$
这里 $\xi$ 是 $x_0$ 与 $x$ 之间的某个值，称其为**拉格朗日余项**。