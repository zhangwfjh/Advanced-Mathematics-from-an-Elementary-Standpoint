# 泰勒级数

## 一阶逼近

我们计算上一节中的一阶逼近函数$$\tilde f$$。已知$$\tilde f$$是斜率为$$f'$$仿射函数，且过$$(x,f(x))$$点，不难得到$$\tilde f(a)-f(a)=f'(a)(x-a)$$，或者$$\tilde f(x)=f(a)+f'(a)(x-a)$$。

**注意** _$$f'(a)$$表示导函数$$f'(x)$$在点$$x=a$$处的值，而不是$$f(a)$$的导数$$\big(f(a)\big)'=0$$。_

考虑一阶逼近的误差，称为**一阶余项**$$R_1(x):=f(x)-\tilde f(x)=f(x)-f(a)-f'(a)(x-a)$$。计算$$\lim_{x\to a}\dfrac{R_1(x)}{x-a}=0$$，因此在$$x=a$$附近，一阶逼近$$\tilde f$$的相对误差为0，记作$$R_1(x)\approx_10$$。或者，$$f(x)=\tilde f(x)+R_1(x)\approx_1\tilde f(x)$$。

## 高阶逼近

现考虑用二次函数$$\tilde f(x)=p(x-a)^2+q(x-a)+r$$对函数$$f$$在点$$a$$附近进行逼近，则有方程组$$\begin{cases}\tilde f(a) = f(a)=r\\ \tilde f'(a)=f'(a)=q\\ \tilde f''(a)=f''(a)=2p\end{cases}$$，因此$$\tilde f(x)=f(a)+f'(a)(x-a)+\frac12f''(a)(x-a)^2$$。定义**二阶余项**为逼近误差$$R_2(x)=f(x)-\tilde f(x)$$，有$$\lim_{x\to a}\dfrac{R_2(x)}{(x-a)^2}=0$$，记作$$R_2(x)\approx_20$$。或者$$f(x)\approx_2\tilde f(x)$$。我们发现，在$$x=a$$附近，$$|R_2(x)| \leq |R_1(x)|$$，因此二阶逼近比一阶逼近更精确。

![](https://upload.wikimedia.org/wikipedia/commons/6/62/Exp_series.gif)

一般的，我们对$$f$$有$$n$$阶逼近$$\tilde f(x)=f(a)+f'(a)(x-a)+\frac12f''(a)(x-a)^2+\cdots+\frac1{n!}f^{(n)}(a)(x-a)^n$$，称为函数$$f$$在点$$a$$处的**$$n$$阶泰勒展开**，满足**$$n$$阶余项**$$R_n(x)=f(x)-\tilde f(x)$$有$$\lim_{x\to a}\dfrac{R_n(x)}{(x-a)^n}=0$$。

当$$n\to\infty$$时，定义$$\tilde f(x)=\sum_{n=0}^\infty\dfrac{f^{(n)}(a)}{n!}(x-a)^n$$为函数$$f$$在点$$x=a$$处的**泰勒级数**，此时逼近误差$$R_\infty(x)\to0$$，即$$f(x)=\sum_{n=0}^\infty\dfrac{f^{(n)}(a)}{n!}(x-a)^n$$。如果$$a=0$$，则也称为**麦克劳林级数**。

**注意** _一般来说，泰勒级数只说明了在一点附近与原函数值相等，而在较远处可能有非常大的误差！_

## 常见展开

1. $$e^x=\sum_{n=0}^\infty\dfrac{x^n}{n!}=1+x+\dfrac{x^2}2+\dfrac{x^3}{6}+\cdots$$
2. $$\ln(1+x)=\sum_{n=0}^\infty(-1)^n\dfrac{x^n}{n}=x-\dfrac{x^2}2+\dfrac{x^3}{3}+\cdots$$
3. $$(1+x)^a=\sum_{n=0}^\infty{a \choose n}x^n=1+ax+\dfrac{a(a-1)}2x^2+\dfrac{a(a-1)(a-2)}{6}x^3+\cdots$$
4. $$\sin x=\sum_{n=0}^\infty\dfrac{(-1)^n}{(2n+1)!}x^{2n+1}=x-\dfrac{x^3}{6}+\dfrac{x^3}{120}+\cdots$$
5. $$\cos x=\sum_{n=0}^\infty\dfrac{(-1)^n}{(2n)!}x^{2n}=1-\dfrac{x^2}{2}+\dfrac{x^4}{24}+\cdots$$

证明留给读者。

## 几何意义

注意到$$f'(x)=\dfrac{df}{dx}=\dfrac{d}{dx}f(x)$$，不妨认为$$D:=\dfrac{d}{dx}$$是一个关于函数$$f(x)$$的函数，称作**微分算子**，即$$Df:=f'$$。则利用麦克劳林级数有$$f(a)=\sum_{n=0}^\infty\dfrac{f^{(n)}(0)}{n!}a^n=\sum_{n=0}^\infty\dfrac{(aD)^n}{n!}f(0)=e^{aD}f(0)$$。类似的，根据泰勒级数还有$$f(x)=e^{aD}f(x-a)$$。因此，我们认为$$S_a:=e^{aD}$$是是函数$$f(x)$$的**平移算子**，即对任意$$a \in \mathbb R$$，$$S_x$$将函数$$f(x)$$平移至$$f(x+a)=S_af(x)$$。

如果我们知道导数$$f^{(n)}$$在点$$x$$的值，则泰勒展开可以通过从$$f(x)$$计算$$f(x')$$