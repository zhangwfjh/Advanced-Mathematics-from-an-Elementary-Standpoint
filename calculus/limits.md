# 极限

### 函数极限

考虑函数$$f(x)=\displaystyle{\frac{x^2-3x+2}{x^2-1}}$$，该函数在$$x=\pm 1$$处无定义。在$$x=-1$$处，函数$$f$$趋于无穷大；在$$x=-1$$处，函数$$f$$趋于$$-\frac12$$。
![](/assets/limits1.png)
如何讨论函数的这种现象呢？我们发现，尽管在$$x=\pm1$$处无定义，但在其附近却处处有定义，这让我们联想到无穷小量。如果将$$f$$扩展到超实数域$${}^*\mathbb R$$，记作$${}^*f$$，取无穷小量$$\epsilon=\{\frac1n\}_1^\infty$$，那么对于$$^*x=1+\epsilon$$，有$$^*f(^*x)=\displaystyle{\frac{(1+\epsilon)^2-3(1+\epsilon)+2}{(1+\epsilon)^2-1}}=\frac{\epsilon-1}{\epsilon+2}$$。故$$\mathop{st} {}^*f(^*x)=\displaystyle{\lim_{n\to\infty}\frac{\frac1n-1}{\frac1n+2}=-\frac12}$$。  
而对于$$^*x=-1+\epsilon$$，有$$^*f(^*x)=1-\displaystyle{\frac3\epsilon}$$，即$$\mathop{st} {}^*f(^*x)=\displaystyle{\lim_{n\to\infty}1-3n=-\infty}$$。如果我们取无穷小量$$\delta=\{-\frac1n\}_1^\infty$$，则$$\mathop{st}{}^*f(1+\delta)=-\frac12,\mathop{st}{}^*f(-1+\delta)=+\infty$$。我们还可以讨论$$^*f$$在$$x\to\infty$$时的表现，不难证明，$$\mathop{st}{}^*f(\frac1\epsilon)=\mathop{st}{}^*f(\frac1\delta)=1$$。

对于实数域上的偏函数$$f:\mathbb R \to \mathbb R$$，将$$f$$扩展到超实数域$$^*f:^*\mathbb R \to ^*\mathbb R$$，且令$$\epsilon$$为正无穷小量，则定义$$f$$在点$$p$$的**左极限**为$$f(p^-):=\lim_{x\to p^-}f(x):=\mathop{st}{}^*f(p-\epsilon)$$，**右极限**为$$f(p^+):=\lim_{x\to p^+}f(x):=\mathop{st}{}^*f(p+\epsilon)$$。如果左极限和右极限相等，则极限值称为$$f$$在点$$p$$处的**极限**，或者，$$\lim_{x\to p}f(x):=\mathop{st}{}^*f({}^*p)$$。

极限还有另一种解释，如果任意精度的“尺子”最终无法测量$$L$$与$$p$$附近函数值$$f(x)$$之间的距离，那么$$f(x)$$在$$x=p$$处的极限为$$L$$。用数学语言表达为：$$\forall \epsilon \gt 0, \exists \delta \gt 0, \forall x \in (p-\delta, p+\delta): |f(x)-L| \lt \epsilon$$。读者可以将此与柯西列极限作比较。

**注意** _极限不一定存在，甚至单边极限也不一定存在，例如Dirichlet函数_$$D(x)=\begin{cases}1,&x \in \mathbb Q\\ 0, & x \notin \mathbb Q\end{cases}$$_处处不存在极限。_

## 性质

令函数$$f,g$$在点$$p$$处极限存在，函数$$h$$在点$$q$$处极限存在，则函数的极限具有以下性质：

* $$\lim_{x\to p}(f(x)+c)=\lim_{x\to p}f(x)+c$$
* $$\lim_{x\to p}c\cdot f(x)=c\cdot\lim_{x\to p}f(x)$$
* $$\lim_{x\to p}f(x) \pm g(x) = \lim_{x\to p}f(x) \pm \lim_{x\to p}g(x)$$
* $$\lim_{x\to p}f(x)\cdot g(x) = \lim_{x\to p}f(x) \cdot \lim_{x\to p}g(x)$$
* $$\lim_{x\to p}\dfrac{f(x)}{g(x)} = \dfrac{\lim_{x\to p}f(x)}{\lim_{x\to p}g(x)}\qquad \big(\lim_{x\to p}g(x) \neq 0\big)$$
* 如果$$\lim_{x\to q}h(x)=p$$，则$$\lim_{x\to q}f(h(x))=\lim_{x\to p}f(x)$$

**证明**: 前五个性质直接从标准部定义得出。函数复合性质可从$${}^*(f\circ h)({}^*x)={}^*f({}^*h({}^*x))={}^*f({}^*p)$$得出。

## 常见极限

定义自然指数$$e^x:=\lim_{n\to\infty}\left(1+\dfrac xn\right)^n$$，自然对数$$\ln(x)$$是$$e^x$$的反函数。我们有

1. $$\lim_{x\to0}(1+ax)^\frac1x=e^a$$
2. $$\lim_{x\to0}\dfrac{(1+x)^a-1}{x}=a$$
3. $$\lim_{x\to0}\dfrac{e^{ax}-1}{x}=a$$
4. $$\lim_{x\to0}\dfrac{\ln(1+ax)}{x}=a$$
5. $$\lim_{x\to0}\dfrac{\cos ax-1}x=0$$
6. $$\lim_{x\to0}\dfrac{\sin ax}{x}=a$$

**证明**：性质1是定义的直接结果；利用牛顿二项式定理，因为$$(1+x)^a=\sum_{k=0}^\infty\binom{a}{k}x^k=1+ax+\sum_{k=2}^\infty\binom{a}{k}x^k$$，所以$$\lim_{x\to0}\dfrac{(1+x)^a-1}{x}=\mathop{st}\left(a+\sum_{k=1}^n\binom{a}{k+1}\epsilon^{k}\right)=a$$，性质2成立；性质3是性质2的推论；性质4只需对性质1取对数；性质5和6可对性质3应用欧拉公式。
## 连续性

如果函数$$f$$在点$$p$$处有定义且极限$$\lim_{x \to p}f(x)=f(p)$$，则称$$f$$在点$$p$$处**连续**。如果函数在定义域上每一点都连续，则称$$f$$为**连续函数**。