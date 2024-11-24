---
title: 波动光学
date: 2024-11-24 8:00:00
tags: [Physics]
---
# 波动光学

## 相干光

光波相干的条件：

1. 频率相同
2. 相位差恒定
3. 振动方向相同

**注意**：两个普通光源或同一普通光源的不同部分所发出的光是不相干的

那么如何获得相干光呢？

1. **振幅分割法**：薄膜干涉、牛顿环、迈克耳孙干涉仪
2. **波阵面分割法**：杨氏双缝干涉实验、劳埃德镜

## 干涉

### 杨氏双缝干涉实验

![杨氏双缝干涉实验](https://img-blog.csdnimg.cn/img_convert/6b4addd92a3b2ea4b1c8b2f3a08b3f74.png)

光程差：$\delta = d\sin\theta \approx \frac{d}{D}x$

当 $\delta$ 满足 $\delta = \pm k\lambda,\quad k = 0,1,2,\cdots$ 时，对应的条纹为明条纹。$k = 0$ 对应的条纹称为中央明纹。$k=1,2,\cdots$ 对应的明条纹分别叫第一级、第二级……明条纹。

### 劳埃德镜

![劳埃德镜](https://pic3.zhimg.com/v2-d4b284c403082c00aa591e42e974a182_b.jpg)

**半波损失**：光由光速较大的介质（光疏）射向光速较小的介质（光密）时，反射光相位突变 $\pi$

### 薄膜干涉

![薄膜干涉](https://pic2.zhimg.com/v2-b6381fa73eb96fd43dbc088dc31f0831_r.jpg)

**两束反射相干光的光程差**：$\delta = 2e\sqrt{n_2^2-n_1^2\sin^2i}+\frac{\lambda}{2}$

**两束透射相干光的光程差**：$\delta = 2e\sqrt{n_2^2 - n_1^2\sin^2i}$

### 增透膜和增反膜

**增透膜**：对某一特定波长 $\lambda$，**反射干涉相消**，透过相长。

**增反膜**：对某一特定波长，**反射干涉加强**，使反射率大大加强，透射率相应减少。

### 等倾干涉

![等倾干涉](https://p5.itc.cn/q_70/images03/20200619/d70e187840a649858f6f565ffe18117d.png)

- 光程差取决于**入射角**
- 倾角 $i$ 相同的光线对应同一级干涉条纹
- 膜变厚，条纹更密集；膜变薄，条纹更稀疏

### **劈尖干涉**（等厚干涉）

![劈尖干涉](https://appwk.baidu.com/naapi/doc/view?ih=810&o=jpg_6&iw=1080&ix=0&iy=0&aimw=1080&rn=1&doc_id=0c97c61fa76e58fafab00375&pn=6&sign=ec3b42c4fb823b1adb8b63faf78dee0d&type=1&app_ver=2.9.8.2&ua=bd_800_800_IncredibleS_2.9.8.2_2.3.7&bid=1&app_ua=IncredibleS&uid=&cuid=&fr=3&Bdi_bear=WIFI&from=3_10000&bduss=&pid=1&screen=800_800&sys_ver=2.3.7)

- 相同膜厚 $e_k$ 对应于同一级条纹

- $e=0$ 的棱边处是暗纹，这是**半波损失**的一例证

- 任意相邻明（暗）纹间距为 $l$
  $$
  l = \frac{\lambda}{2n\sin\theta}
  $$

### 牛顿环

![牛顿环](https://gss0.baidu.com/9vo3dSag_xI4khGko9WTAnF6hhy/zhidao/pic/item/4610b912c8fcc3ceb2c6b7a49c45d688d43f2026.jpg)

**光程差**：$\delta = 2nd + \frac{\lambda}{2}$
$$
r \approx \sqrt{2Rd} = \sqrt{\left(\delta - \frac{\lambda}{2}\right)\frac{R}{n}}
$$

**明环半径**：$r=\sqrt{(k-\frac{1}{2})\frac{R\lambda}{n}},\quad k=1,2,\cdots$

**暗环半径**：$r=\sqrt{\frac{kR\lambda}{n}},\quad k = 0,1,2,\cdots$

**干涉图样**：内疏外密、中心为暗点的圆环

### 迈克耳孙干涉仪

![迈克耳孙干涉仪](https://phylab.nuaa.edu.cn/_upload/article/images/71/c2/30fa32244d7c95c79a464dcd4671/b018aa85-7ae5-4d52-ba88-1f5598493c7b_d.png)

测出视场中移过的条纹数目 $\Delta n$，就可以算出 $M_1$ 移动的距离：
$$
\Delta d = \Delta n\frac{\lambda}{2}
$$


## 衍射

### 夫琅禾费单缝衍射

![夫琅禾费单缝衍射](https://img-blog.csdnimg.cn/20210518234018923.png#pic_center)

**暗条纹中心**：$b\sin\theta = \pm k\lambda,\quad k=1,2,\cdots$

**明条纹中心**：$b\sin\theta = \pm (2k+1)\frac{\lambda}{2},\quad k=1,2,3,\cdots$

**中央明纹宽度**：$\Delta x_0=2\frac{\lambda f}{b}$

**其他任何两条相邻暗条纹（明条纹）宽度**：$\Delta x=\frac{\lambda f}{b}$

### 夫琅禾费圆孔衍射

![夫琅禾费圆孔衍射](https://image3.slideserve.com/6156606/slide21-l.jpg)
$$
2\theta = \frac{d}{f} = 2.44\frac{\lambda}{D}
$$

**最小分辨角**：$\theta_0 = 1.22\frac{\lambda}{D}$

**分辨本领**：$\frac{1}{\theta_0}$

提高分辨本领的方法：增大透光孔径 $D$ 或减小波长 $\lambda$

### 衍射光栅

**光栅常量**：$d = b + b'$

**光栅衍射明条纹的条件**：$d\sin\theta = \pm k\lambda,\quad k=0,1,2,\cdots$

$k=0$ 的明纹称为**中央明纹**，$k=1,2,\cdots$ 的明纹分别叫第一级、第二级、……明纹。

光栅中的狭缝条数越多，明纹就越亮越窄。

**光栅衍射暗条纹的条件**：$d\sin\theta=\pm\frac{k'}{N}\lambda,\quad k'=1,2,\cdot,(N-1),(N+1),(N+2),\cdots,(2N-1),\cdots$

**次明纹**：两相邻暗纹之间的明纹，光强远小于主明纹。

**缺级现象**
$$
(b+b')\sin\theta = \pm k\lambda,\quad k=0,1,2,\cdots\\
b\sin\theta = \pm k'\lambda,\quad k=1,2,\cdots
$$
两式相除
$$
\frac{b+b'}{b} = \frac{k}{k'}
$$

## 偏振

### 马吕斯定律

强度为 $I_0$ 的偏振光检偏器后，出射光的强度为 $I_0\cos^2\alpha$，其中 $\alpha$ 为起偏器和检偏器的夹角。

用该定律可以证明，强度为 $I_0$ 的自然光通过**起偏器**后，出射光的光强为 $\frac{1}{2}I_0$

### 反射光和折射光的偏振

理论和实验都表明，当自然光入射到折射率分别为 $n_1$ 和 $n_2$ 的两种介质的分界面上时，反射光和折射光都是部分偏振光。其中反射光是垂直入射面的振动较强的部分偏振光，而折射光是平行入射面的振动较强的部分偏振光。

当入射角 $i_B$ 满足
$$
\tan i_B = \frac{n_2}{n_1}
$$
时，反射光为**完全**偏振光，且振动面垂直入射面，折射光为**部分**偏振光。此时，反射光和折射光互相垂直，把 $i_B$ 称为**起偏角**。



