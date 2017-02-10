# 积分

## 反导数

考虑微分运算的逆操作，如果存在函数$$F$$满足$$f=F'$$，则称$$F$$是$$f$$的**反导数**，也称**原函数**或**不定积分**，记作$$F(x)=\int f(x)~dx$$，或者$$F:=\int f$$。显然，反导数不是唯一的，对于任意常数$$C$$，都有$$F'=(F+C)'$$，因此，如果$$F$$是$$f$$的反导数，则$$F+C$$也是$$f$$的反导数。注意，不是所有函数都有反导数，例如之前提到的Dirchelet函数，反导数存在的函数称作**可积函数**。

## 常见不定积分

1. $$\int e^x~dx = e^x+C$$
2. $$\int \ln x~dx = \dfrac1x + C$$
3. $$\int x^a~dx = \dfrac{1}{a+1}x^{a+1}+C \quad (a \neq -1)$$
4. $$\int \sin x~dx =-\cos x +C$$
5. $$\int \cos x~dx = \sin x +C$$
6. $$\int \arcsin x~dx = \dfrac{1}{\sqrt{1-x^2}}+C$$
7. $$\int \arctan x~dx = \dfrac{1}{1+x^2}+C$$

## 黎曼积分

我们尝试计算函数$$f$$的反导数$$F$$。回忆导数的定义，$$F'(x_0)=\lim_{x_1\to x_0}\dfrac{F(x_1)-F(x_0)}{x_1-x_0}$$，类似有$$F'(x_{k-1})=\lim_{x_k\to x_{k-1}}\dfrac{F(x_k)-F(x_{k-1})}{x_k-x_{k-1}}$$。如果令$$x_k=x_{k-1}+\varepsilon$$，并将$$n$$个定义式相加则有，$$\sum_{k=0}^{n-1}F'(x_k)=\lim_{\varepsilon\to0}\sum_{k=0}^{n-1}\dfrac{F(x_k)-F(x_{k-1})}{\varepsilon}=\lim_{\varepsilon\to0}\dfrac{F(x_n)-F(x_{0})}{\varepsilon}$$。通过简单代数计算，我们得到$$F(x_n)=F(x_0)+\lim_{\varepsilon\to0}\sum_{k=0}^nf(x_0+k\varepsilon)\varepsilon$$。令$$x=x_n$$，则$$x=x_0+n\varepsilon$$，或者$$n=\dfrac{x-x_0}{\varepsilon}\to\infty$$。于是$$F(x)=F(x_0)+\lim_{\varepsilon\to0}\sum_{k=0}^{(x-x_0)/\varepsilon}f(x_0+k\varepsilon)\varepsilon$$。因为$$F(x_0)$$是常数，因此反导数与$$x_0$$无关，得到$$f$$的原函数$$F(x):=\int f(x)~dx=\lim_{\varepsilon\to0}\sum_{k=0}^{x/\varepsilon}f(k\varepsilon)\varepsilon$$。其中，等式右边的和式称为**黎曼和**。

我们称$$\int_a^b f(x)~dx:=F(b)-F(a)$$为函数$$f$$在区间$$[a,b]$$上的**定积分**。

## 性质

令$$f,g$$是实数域上的可积函数，$$a,b,c$$是常数，则

1. $$\int af \pm bg = a\int f \pm b\int g$$
2. $$\int_a^b f = -\int_b^a f$$
3. $$\int_a^c f = \int_a^b f + \int_b^c f$$
4. $$\int_a^b f'g = (fg)(b)-(fg)(a)-\int_a^b fg'$$

性质4也称**分部积分公式**，证明留给读者。

## 几何意义

考虑黎曼和$$\sum_{k=0}^{n-1}f(x_k)\varepsilon$$，满足$$x_0=a,x_n=b,x_{k+1}=x_k+\varepsilon$$，则$$f(x_k)\varepsilon$$计算了以$$(x_k,x_{k+1})$$为底，$$f(x_k)$$为高的矩形面积，而黎曼和是所有矩形面积的和。因此，定积分表示了函数$$f$$在$$[a,b]$$内下的有向面积。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Integral_example.svg/600px-Integral_example.svg.png)

## 微积分基本定理

考虑定义在闭区间$$[a,b]$$上的连续函数$$f$$，定义$$F(x):=\int_a^xf(t)~dt$$，则函数$$F$$在开区间$$(a,b)$$上连续可导，且满足$$F'=f$$。这是**微积分基本定理**。

作为该定理的一个应用，注意到$$f(x)=f(a)+\int_a^xf'(t)~dt$$，根据分部积分公式，$$\int_a^xf'(t)~dt=\int_a^xt'f'(t)~dt=xf'(x)-af'(a)-\int_a^xtf''(t)~dt$$。再对$$f'(x)$$应用该定理得$$f'(x)=f'(a)+\int_a^xf''(t)~dt$$。将三个方程合并得到$$f(x)=f(a)+f'(a)(x-a)+\int_a^x(x-t)f''(t)~dt$$，这是泰勒二阶展开公式，二阶余项$$R_2(x)=\int_a^x(x-t)f''(t)~dt$$。继续运用分部积分公式和微积分基本定理可得一般的泰勒展开式。