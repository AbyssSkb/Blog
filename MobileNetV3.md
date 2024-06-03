# 轻量化卷积神经网络综述

## MobileNetV3

### 激活函数
MobileNetV3 使用了 $\mathrm{h\text{-}swish}$：
$$
\mathrm{h\text{-}swish}[x] = x\frac{\mathrm{ReLU6}(x+3)}{6}
$$

首先来看一下 $swish$：
$$
swish[x] = x \sigma(x)
$$
当 $x\to +\infty$ 时，$\sigma(x) \to 1$，$swish$ 退化成 $x$，当 $x\to -\infty$ 时，$\sigma(x) \to 0$，$swish$ 等于 $0$。不难看出，$swish$ 是 $\mathrm{ReLU}$ 的 `soft version`。

既然有了 $\mathrm{ReLU}$ ，那为啥还要发明 $swish$ 呢

为了避免神经网络在训练时出现梯度爆炸的问题，人们设计激活函数时会约束其导数的绝对值 $\vert\frac{dy}{dx}\vert \le 1$，而 $\mathrm{ReLU}$ 天生具有这一优势，但是其有一个弊端，$\mathrm{ReLU}$ 的导数并不连续，这将降低拟合的速度以及效果，因此诞生了 $swish$，其导数连续，在 $x = 0$ 附近制造了一个平缓区。

那为什么还要发明 $\mathrm{h\text{-}swish}$

$swish$ 中的 $\sigma$ 计算量大，导致延迟较大，而 $\mathrm{h\text{-}swish}$ 中的 $\frac{\mathrm{ReLU6}(x+3)}{6}$ 其实就是对 $\sigma$ 的分段近似拟合，从而减少计算量，降低延迟。

首先 $\mathrm{ReLU6}$ 是对 $\mathrm{ReLU}$ 的最大值加以限制的版本
$$
\mathrm{ReLU6}[x] = \min(6, \max(0, x))
$$

当 $x > 3$ 时，$\frac{\mathrm{ReLU6}(x+3)}{6} = 1$，此时 $\mathrm{h\text{-}swish}$ 退化成 $x$，当 $x < -3$ 时，$\mathrm{ReLU6}(x+3) = 0$，此时 $\mathrm{h\text{-}swish}$ 恒等于 $0$，这很类似 $\mathrm{ReLU}$

当 $-3 \le x \le 3$ 时，$\mathrm{h\text{-}swish}$ 等于 $\frac{x(x+3)}{6}$ 

### NAS (Network Architecture Search)
To be done.