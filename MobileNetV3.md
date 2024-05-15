# 轻量化卷积神经网络综述

## MobileNetV3

### 激活函数
MobileNetV3 使用了 $\mathrm{h\text{-}swish}$，我们来看看这个激活函数：
$$
\mathrm{h\text{-}swish}[x] = x\frac{\mathrm{ReLU6}(x+3)}{6}
$$

而 $\mathrm{ReLU6}$ 其实就是对 $\mathrm{ReLU}$ 的最大值加了限制
$$
\mathrm{ReLU6}[x] = \min(6, \max(0, x))
$$

所以当 $x > 3$ 时，$\frac{\mathrm{ReLU6}(x+3)}{6} = 1$，此时 $\mathrm{h\text{-}swish}$ 退化成 $\mathrm{ReLU}$，当 $x < -3$ 时，$\mathrm{ReLU6}(x+3) = 0$，此时 $\mathrm{h\text{-}swish}$ 恒等于 $0$

如果把 $\mathrm{ReLU}$ 理解为两条线拼接在一起，那么 $\mathrm{h\text{-}swish}$ 就是在这两条线之间添加了一段弧线，使其过渡的更加平滑。