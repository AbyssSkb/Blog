# 数列的极限
## 定义
设 $\{x_n\}$ 为一数列，如果存在常数 $a$，是对于任意给定的正数 $\epsilon$（不论它多么小），总存在正整数 $N$，使得当 $n > N$时，不等式
$$
\left\vert x_n - a \right\vert < \varepsilon
$$
都成立，那么就称常数 $a$ 是**数列** $\{x_n\}$ 的**极限**，或者称数列 $\{x_n\}$ **收敛于** $a$，记为
$$
\lim\limits_{n \to \infty }x_n = a
$$
或
$$
x_n \to a \quad (n \to \infty)
$$
如果不存在这样的常数 $a$，就说数列 $\{x_n\}$ 没有极限，或者说数列 $\{x_n\}$ 是**发散**的，习惯上也说 $\lim\limits_{n \to \infty}x_n$ 不存在。

数列极限 $\lim\limits_{n\to\infty}x_n = a$ 的定义可表达为
$$
\lim\limits_{n \to \infty}x_n = a \Leftrightarrow \forall \varepsilon > 0, \,
\exists \,正整数\,N，当\,n > N\,时，有\,\left\vert x_n - a\right\vert < \varepsilon
$$

## 性质
**定理 $1$（极限的唯一性）$\quad$** 如果数列 $\{x_n\}$ 收敛，那么它的极限唯一。

**定理 $2$（收敛数列的有界性）$\quad$** 如果数列 $\{x_n\}$ 收敛，那么数列 $\{x_n\}$ 一定有界。

**定理 $3$（收敛数列的保号性）$\quad$** 如果 $\lim\limits_{n \to \infty}x_n = a$，且 $a > 0$（或 $a < 0$），那么存在正整数 $N$，当 $n > N$ 时，都有 $x_n > 0$（或 $x_n < 0$）。

**推论$\quad$** 如果数列 $\{x_n\}$ 从某项起有 $x_n \ge 0$（或 $x_n \le 0$），且 $\lim\limits_{n\to\infty} x_n = a$，那么 $a \ge 0$（或 $a \le 0$）。

**定理 $4$（收敛数列与其子数列间的关系）$\quad$** 如果数列 $\{x_n\}$ 收敛于 $a$，那么它的任一子数列也收敛，且极限也是 $a$。

# 函数的极限
## 定义
**定义 $1\quad$** 设函数 $f(x)$ 在点 $x_0$ 的某一去心邻域内有定义。如果存在常数 $A$，对于任一给定的正数 $\varepsilon$（不论它多么小），总存在正数 $\delta$，使得当 $x$ 满足不等式 $0 < \left\vert x - x_0 \right\vert < \delta$ 时，对应的函数值 $f(x)$ 都满足不等式
$$
\left\vert f(x) < A \right\vert < \varepsilon
$$
那么常数 $A$ 就叫做**函数 $f(x)$ 当 $x\to x_0$ 时的极限**，记作
$$
\lim\limits_{x\to x_0}f(x) = A\ 或\ f(x) \to A\ (\ 当\ x \to x_0\ )
$$
定义 $1$ 可以简单的表述为
$$
\lim\limits_{x\to x_0}f(x) = A \Leftrightarrow \forall \varepsilon > 0, \exists \delta > 0, 当 0 < \left\vert x - x_0 \right\vert < \delta 时, 有 \left\vert f(x) - A \right\vert < \varepsilon
$$
在 $\lim\limits_{x\to x_0}f(x) = A$ 的定义中，把 $0 < \left\vert x - x_0 \right\vert < \delta$ 改为 $x_0 - \delta < x < x_0$，那么 $A$ 就叫做函数 $f(x)$ 当 $x \to x_0$ 时的**左极限**，记作
$$
\lim\limits_{x \to x^-_0}f(x) = A \quad 或 \quad f(x_0^-) = A
$$
类似的，把 $0 < \left\vert x - x_0\right\vert < \delta$ 改为 $x_0 < x < x_0 + \delta$，那么 $A$ 就叫做函数 $f(x)$ 当 $x \to x_0$ 时的**右极限**，记作
$$
\lim\limits_{x \to x^+_0}f(x) = A \quad 或 \quad f(x_0^+) = A
$$
函数 $f(x)$ 当 $x \to x_0$ 时极限存在的充分必要条件是左极限及右极限各自存在并且相等，即
$$
f(x_0^-) = f(x_0^+)
$$
**定义 $2\quad$** 设函数 $f(x)$ 当 $\left\vert x\right\vert$ 大于某一正数时有定义。如果存在常数 $A$，对于任意给定的正数 $\varepsilon$，总存在正数 $X$，使得当 $x$ 满足不等式 $\left\vert x\right\vert > X$ 时，对应的函数值 $f(x)$ 都满足不等式
$$
\left\vert f(x) - A \right\vert < \varepsilon
$$
那么常数 $A$ 就叫做**函数 $f(x)$ 当 $x \to \infty$ 时的极限**，记作
$$
\lim\limits_{x \to \infty} = A \quad 或 \quad f(x) \to A (当 x\to \infty)
$$
定义 $2$ 可简单地表达为
$$
\lim\limits_{x \to \infty} f(x) = A \Leftrightarrow \forall \varepsilon > 0, \exists X > 0, 当 \left\vert x \right\vert > X时，有 \left\vert f(x) - A \right\vert < \varepsilon
$$

## 性质
**定理 $1$（函数极限的唯一性）$\quad$** 如果 $\lim\limits_{x \to x_0} f(x)$ 存在，那么这极限唯一。

**定理 $2$（函数极限的局部有界性）$\quad$** 如果 $\lim\limits_{x \to x_0}f(x) = A$，那么存在常数 $M>0$ 和 $\delta > 0$，使得当 $0 < \left\vert x - x_0 \right\vert < \delta$ 时，有 $\left\vert f(x) \right\vert \le M$。

**定理 $3$（函数极限的局部保号性）$\quad$** 如果 $\lim\limits_{x \to x_0}f(x) = A$，且 $A > 0$（或 $A < 0$，那么存在常数 $\delta > 0$，使得当 $0 < \left\vert x - x_0 \right\vert < \delta$ 时，有 $f(x) > 0$（或 $f(x) < 0$）。

**定理 $3^\prime\quad$** 如果 $\lim\limits_{x \to x_0}f(x) = A(A \ne 0)$，那么就存在着 $x_0$ 的某一去心邻域 $\mathring{U}(x_0)$，当 $x \in \mathring{U}(x_0)$ 时，就有 $\left\vert f(x) \right\vert > \frac{\left\vert A\right\vert}{2}$。

**推论$\quad$** 如果在 $x_0$ 的某去心邻域内 $f(x) \ge 0$（或 $f(x) \le 0$），而且 $\lim\limits_{x\to x_0}f(x) = A$，那么 $A \ge 0$（或 $A \le 0$）。

**定理 $4$（函数极限与数列极限的关系）$\quad$** 如果极限 $\lim\limits_{x \to x_0}f(x)$ 存在，$\{x_n\}$ 为函数 $f(x)$ 的定义域内任一收敛于 $x_0$ 的数列，且满足：$x_n \ne x_0$（$n \in N_+$），那么相应的函数值数列 $\{f(x_n)\}$ 必收敛，且 $\lim\limits_{n \to \infty}f(x_n) = \lim\limits_{x \to x_0}f(x)$。

# 无穷小
## 定义
如果函数 $f(x)$ 当 $x \to x_0$（或 $x \to \infty$）时的极限为零，那么称函数 $f(x)$ 为当 $x \to x_0$（或 $x \to \infty$）时的无穷小。
## 性质
在自变量的同一变化过程 $x \to x_0$（或 $x \to \infty$）中，函数 $f(x)$ 具有极限 $A$ 的充分必要条件时 $f(x) = A + \alpha$，其中 $\alpha$ 是无穷小。
## 比较
如果 $\lim\frac{\beta}{\alpha} = 0$，那么就说 $\beta$ 是比 $\alpha$ **高阶的无穷小**，记作 $\beta = o(\alpha)$

如果 $\lim\frac{\beta}{\alpha} = \infty$，那么就说 $\beta$ 是比 $\alpha$ **低阶的无穷小**

如果 $\lim\frac{\beta}{\alpha} = c \ne 0$，那么就说 $\beta$ 与 $\alpha$ 是**同阶的无穷小**

如果 $\lim\frac{\beta}{\alpha^k} = c \ne 0, k > 0$，那么就说 $\beta$ 是关于 $\alpha$ 的 **$k$ 阶的无穷小**

如果 $\lim\frac{\beta}{\alpha} = 1$，那么就说 $\beta$ 与 $\alpha$ 是**等价无穷小**，记作 $\alpha \sim \beta$

**定理 $1\quad$** $\beta$ 与 $\alpha$ 是等价无穷小的充分必要条件为
$$
\beta = \alpha + o(\alpha)
$$

**定理 $2\quad$** 设 $\alpha \sim \tilde\alpha$，$\beta \sim \tilde\beta$，且 $\lim\limits\frac{\tilde\beta}{\tilde\alpha}$ 存在，则
$$
\lim\limits\frac{\beta}{\alpha} = \lim\limits\frac{\tilde\beta}{\tilde\alpha}
$$
# 无穷大
## 定义
设函数 $f(x)$ 在 $x_0$ 的某一去心邻域内有定义（或 $\left\vert x \right\vert$ 大于某一正数时有定义）。如果对于任意给定的正数 $M$（不论它有多大），总存在正数 $\delta$（或正数 $X$），只要 $x$ 适合不等式 $0 < \left\vert x - x_0 \right\vert < \delta$（或 $\left\vert x \right\vert > X$），对应的函数值 $f(x)$ 总满足不等式
$$
\left\vert f(x) \right\vert > M
$$
那么称函数 $f(x)$ 是当 $x \to x_0$（或 $x \to \infty$）时的无穷大。

## 性质
在自变量的同一变化过程中，如果 $f(x)$ 为无穷大，那么 $\frac{1}{f(x)}$ 为无穷小；反之，如果 $f(x)$ 为无穷小，且 $f(x) \ne 0$，那么 $\frac{1}{f(x)}$ 为无穷大。

# 极限运算法则
**定理 $1\quad$** 有限个无穷小的和是无穷小

**定理 $2\quad$** 有界函数与无穷小的乘积是无穷小

**推论 $1\quad$** 常数与无穷小的乘积是无穷小

**推论 $2\quad$** 有限个无穷小的乘积是无穷小

**定理 $3\quad$** 如果 $\lim f(x)=A, \lim g(x) = B$，那么

1. $\lim\left[f(x) \pm g(x) \right] = \lim f(x) \pm \lim g(x) = A \pm B$
2. $\lim\left[f(x) \cdot g(x) \right] = \lim f(x) \cdot \lim g(x) = A \cdot B$
3. 若又有 $B \ne 0$，则

$$
\lim \frac{f(x)}{g(x)} = \frac{\lim f(x)}{\lim g(x)} = \frac{A}{B}
$$

**定理 $4\quad$** 设有数列 $\{x_n\}$ 和 $\{y_n\}$。如果
$$
\lim\limits_{n\to\infty}x_n = A,\quad \lim\limits_{n\to\infty}y_n = B
$$
那么
1. $\lim\limits_{n\to\infty}(x_n\pm y_n) = A \pm B$
2. $\lim\limits_{n\to\infty}(x_n \cdot y_n) = A \cdot B$
3. 当 $y_n \ne 0$（$n = 1, 2, \cdots$）且 $B \ne 0$ 时，$\lim\limits_{n\to\infty}\frac{x_n}{y_n} = \frac{A}{B}$

**定理 $5\quad$** 如果 $\varphi(x) \ge \psi(x)$，而 $\lim\limits \varphi(x) = A$，$\lim\limits \psi(x) = B$，那么 $A \ge B$。 

**定理 $6$（复合函数的极限运算法则）$\quad$** 设函数 $y = f\left[g(x)\right]$ 是由函数 $u = g(x)$ 与函数 $y = f(u)$ 复合而成，$f\left[g(x)\right]$ 在点 $x_0$ 的某去心邻域内有定义，若 $\lim\limits_{x\to x_0}g(x) = u_0$，$\lim\limits_{u \to u_0}f(u) = A$，且存在 $\delta_0 > 0$，当 $x \in \mathring{U}(x_0, \delta_0)$ 时，有 $g(x) \ne u_0$，则
$$
\lim\limits_{x \to x_0}f\left[g(x)\right] = \lim\limits_{u\to u_0}f(u) = A
$$

# 极限存在准则
**准则 $\mathrm{I}\quad$** 如果数列 $\{x_n\}$，$\{y_n\}$ 及 $\{z_n\}$ 满足下列条件：
1. 从某项起，即 $\exists n_0 \in \N_+$，当 $n > n_0$ 时，有
$$
y_n \le x_n \le z_n
$$
2. $\lim\limits_{n \to \infty}y_n = a, \lim\limits_{n\to\infty}z_n = a$

那么数列 $\{x_n\}$ 的极限存在，且 $\lim\limits_{n\to\infty}x_n = a$

**准则 $\mathrm{I}^\prime\quad$** 如果
1. 当 $x \in \mathring{U}(x_0, r)$（或 $\left\vert x \right\vert > M$）时，

$$
g(x) \le f(x) \le h(x)
$$

2. $\lim\limits_{x\to x_0 \atop (x \to \infty)}g(x) = A, \lim\limits_{x\to x_0 \atop (x\to\infty)}h(x) = A$

那么 $\lim\limits_{x\to x_0 \atop (x\to \infty)}f(x)$ 存在，且等于 $A$。

准则 $\mathrm{I}$ 及准则 $\mathrm{I}^\prime$ 称为**夹逼准则**。

**准则 $\mathrm{II}\quad$** 单调有界数列必有极限。 