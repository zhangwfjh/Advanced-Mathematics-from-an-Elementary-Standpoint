# 泰勒级数

## 一阶逼近

我们计算上一节中的一阶逼近函数$$\tilde f$$。已知$$\tilde f$$是斜率为$$f'$$仿射函数，且过$$(x,f(x))$$点，不难得到$$\tilde f(a)-f(a)=f'(a)(x-a)$$，或者$$\tilde f(x)=f(a)+f'(a)(x-a)$$。

考虑一阶逼近的误差，称为**一阶余项**$$R_1(x):=f(x)-\tilde f(x)=f(x)-f(a)-f'(a)(x-a)$$。计算$$\lim_{x\to a}\dfrac{R_1(x)}{x-a}=0$$，因此在$$x=a$$附近，一阶逼近$$\tilde f$$的相对误差为0，记作$$R_1(x)\approx_10$$。或者，$$f(x)=\tilde f(x)+R_1(x)\approx_1\tilde f(x)$$。

## 二阶逼近



## 泰勒展开

计算$$\lim_{x\to a}\dfrac{R_1(x)}{(x-a)^2}$$

如果$$f'(x)$$依然可导，还可计算其一阶逼近$$f'(x)\approx_1\tilde f'(x)=f'(a)+f''(a)(x-a)$$。类似定义$$f$$的**二阶余项**$$R_2(x):=f(x)-\tilde{\tilde f}(a)=f(x)-f(a)-f'(a)(x-a)-f''(a)(x-a)^2$$，仍然有$$\lim_{x\to a}\dfrac{R_2(x)}{(x-a)^2}=0$$，记作$$R_2(x)\approx_20$$。或者$$f(x)\approx_2\tilde{\tilde f}(x)$$

## 常见展开

## 应用