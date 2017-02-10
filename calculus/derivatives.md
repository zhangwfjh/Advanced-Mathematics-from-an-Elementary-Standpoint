# 导数

## 定义

考虑实函数$$y=f(x)$$，$$f$$可看作定义域到值域的一个伸缩形变。例如，在下图中，红色部分是一个等距平移，绿色部分是一个拉伸，蓝色部分是一个反向拉伸，紫色部分是一个压缩。为了研究函数$$f$$的形变情况，可以定义形变率。

![](/assets/derivatives1.png)

具体来说，定义实数域$$\mathbb R$$上的一个有序对$$(a,b)$$为一个**有向区间**（不必有$$a \lt b$$），$$\overline{ab}:=b-a$$为$$(a,b)$$的**有向长度**。那么，函数$$f$$在有向区间$$(a,b)$$的形变率$$k_f(a,b)=\dfrac{\overline{f(a)f(b)}}{\overline{ab}}$$。如果函数$$f$$是线性函数，即对任意$$(a,b)$$满足$$\overline{f(a)f(b)}=f(\overline{ab})$$，则$$k_f(a,b)=\dfrac{f(\overline{ab})}{\overline{ab}}=f(1)$$是常数，所以线性函数在每一点具有相同的形变率。显然，如果将函数$$f$$平移至$$g(x)=f(x)+c$$，则$$g(x)$$在每一个有向区间上的形变率不变。因此，仿射函数（线性函数的平移）在每一点也具有相同的形变率。

在上图中，函数$$f(x)$$在红、蓝、紫色区间内是仿射函数，每一点的形变率可以由有向区间长度比直接求出；而在绿色区间内，定义域上相同长度的有向子区间在不同位置被$$f$$拉伸成为值域上不同长度的有向子区间。为了计算函数$$f$$在一点$$x$$的形变率，我们在充分小的有向区间$$(x,x')$$内，用一个仿射函数$$\tilde f$$逼近函数$$f$$，用仿射函数$$\tilde f$$的形变率作为函数$$f$$在点$$x$$的形变率，即$$k_f(x):=k_{\tilde f}$$。

我们计算$$k_{\tilde f}$$，由于函数$$\tilde f$$的定义域$$(x,x')$$充分小，可考虑极限$$x'\to x$$，则$$k_{\tilde f}=\lim_{x'\to x}\dfrac{\overline{\tilde f(x)\tilde f(x')}}{\overline{xx'}}=\lim_{x'\to x}\dfrac{\tilde f(x')-\tilde f(x)}{x'-x}=\lim_{x'\to x}\dfrac{f(x')-f(x)}{x'-x}$$。等价地，如果扩展$$f$$到超实数域$$^*f$$，则$$k_{\tilde f}=\mathop{st}\dfrac{^*f(^*x)-{}^*f(x)}{^*x-x}=\mathop{st}\dfrac{^*f(x+\varepsilon)-{}^*f(x)}{\varepsilon}$$。

我们称函数$$f$$在点$$x$$的变形率为**导数**，记作$$f'(x):=k_f(x)$$，导数是$$x$$的函数，也称$$f'$$是$$f$$的**导函数**。仿射函数$$\tilde f_x$$称为$$f$$在点$$x$$的**一阶逼近**，$$df_x=\overline{\tilde f(x)\tilde f(x+\varepsilon)}$$称为$$f$$在点$$x$$的**微分**。令恒等函数$$\iota(x)=x$$，则$$d\iota_x=dx=\varepsilon$$，$$f'=\dfrac{df}{dx}$$，故导数也称为**微商**。

请注意，导数是一种极限，故不一定存在，例如绝对值函数$$|x|$$在原点没有导数。如果函数$$f$$在点$$x$$处的导数存在，则称$$f$$在点$$x$$处**可导**，如果函数$$f'$$处处可导，则称$$f$$是**可导函数**。

如果$$g(x)=f'(x)$$可导，还可计算$$g'(x)=f''(x)$$，称$$f$$的**二阶导数**。类似可定义函数$$f$$的**$$n$$阶导数**，记作$$f^{(n)}:=(f^{(n-1)})'$$。

## 性质

假设可导函数$$f,g$$的导数是$$f',g'$$，$$a,b$$是常数，则有：

1. $$(af \pm bg)' = af' \pm bg'$$
2. $$(fg)' = f'g + fg'$$
3. $$\left(\dfrac fg\right)'=\dfrac{f'g-fg'}{g^2} \quad (g \neq 0)$$
4. $$(f(g))'=f'(g) \cdot g'$$
5. $$\dfrac{f'}{g'}=\dfrac{df}{dg}$$
6. 若$$f$$是$$g$$的反函数，即$$f(g(x))=x$$，则$$g'=\dfrac{1}{f'(g)}$$

**证明**: 性质1是极限的直接结果；性质2利用$$f(x')g(x')-f(x)g(x)=f(x')\big((g(x')-g(x)\big)+g(x)\big(f(x')-f(x)\big)$$即可；性质3只需证$$\left(\dfrac1g\right)'=-\dfrac{g'}{g^2}$$；注意到等式$$df(g)=\dfrac{df(g)}{dg}dg=f'(g)dg$$，性质4立即成立。

特别地，对于$$n$$个可导函数$$f_1, f_2, \ldots f_n$$，根据性质4,$$df_1(f_2(\cdots(f_n)))=\dfrac{df_1}{df_2}df_2(\cdots(f_n))=\cdots=\dfrac{df_1}{df_2}\dfrac{df_2}{df_3}\cdots\dfrac{df_{n-1}}{df_n}df_n$$，因此性质4也称为**链式法则**。性质5、6是性质4的推论。

## 常见导数

1. $$(e^x)'=e^x$$
2. $$(\ln x)'=\frac1x$$
3. $$(x^a)'=ax^{a-1}$$
4. $$(\sin x)' = \cos x$$
5. $$(\cos x)' = -\sin x$$
6. 若$$P(x)=a_0+a_1x+\cdots+a_nx^n$$，则$$P^{(n)}(x)=n!$$
7. $$(\arcsin x)'=\dfrac{1}{\sqrt{1-x^2}}$$
8. $$(\arctan x)'=\dfrac{1}{1+x^2}$$

证明留给读者。

## 应用

### 切线斜率

考虑函数$$y=f(x)$$过点$$(x,f(x)), (x',f(x'))$$的割线$$l$$，$$l$$的斜率为$$k_l=\dfrac{f(x')-f(x)}{x'-x}$$，割线$$l$$在点$$x$$的一阶逼近是$$f$$在点$$x$$的切线，故$$f'(x)$$描述了函数$$f$$在点$$x$$处切线的斜率。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/Secant-calculus.svg/500px-Secant-calculus.svg.png)![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Tangent-calculus.svg/500px-Tangent-calculus.svg.png)

### 单调性与极值

考虑函数$$f$$的形变率，如果$$f'(x) \gt 0$$，则$$f$$在点$$x$$处正向拉伸，即$$f$$单调递增；如果$$f'(x) \lt 0$$，则$$f$$在点$$x$$处反向拉伸，即$$f$$单调递减；如果$$f'(x) = 0$$，则$$f$$在$$x$$附近值不变，取得极大或极小值。特别地，如果$$f'(x)=0$$对所有实数恒成立，则$$f$$是常数。

## 运动分解

令$$z=re^{i\theta}$$，根据链式法则，计算得$$dz=d(re^{i\theta})=e^{i\theta}dr+r(de^{i\theta})=e^{i\theta}dr+ire^{i\theta}d\theta=e^{i\theta}dr+izd\theta$$。如果$$\theta=0$$，则$$dz=dr$$退化实导数；如果$$r$$是常数，则$$dr=0$$，$$dz=ire^{i\theta}d\theta=re^{i(\theta+\pi/2)}d\theta$$，因此$$\dfrac{\partial(re^{i\theta})}{\partial\theta}=re^{i(\theta+\pi/2)}$$，即$$z$$对$$\theta$$的**偏导数**(即固定其余变量不变的导数)，是$$z$$逆时针旋转$$\pi/2$$，两个复数相互垂直。

假设平面上的运动用复数$$z=z(t)$$来表示，其中$$t$$是时间参数，则$$z'(t)=\dfrac{dz}{dt}$$表示该运动在$$t$$时刻的速度。我们有$$z'(t)=e^{i\theta}r'+re^{i(\theta+\pi/2)}\theta'$$，其中$$e^{i\theta}r'$$表示该运动的**径向速度**，大小为$$r'$$；而$$re^{i(\theta+\pi/2)}\theta'$$表示运动的**环向速度**，大小为$$r\theta'$$。这是平面运动的极分解。

![](/assets/derivatives2.png)

进一步我们还可以考虑加速度$$z''$$，不难计算$$z''=e^{i\theta}r''+re^{i(\theta+\pi/2)}\theta''-re^{i\theta}{\theta'}^2+2re^{i(\theta+\pi/2)}r'\theta'$$。其中$$e^{i\theta}r''$$是**径向加速度**，大小为$$r''$$；$$re^{i(\theta+\pi/2)}\theta''$$是**环向加速度**，大小为$$r\theta''$$；$$-re^{i\theta}{\theta'}^2$$是**向心加速度**，与径向相反，大小为$$r{\theta'}^2$$；$$2re^{i(\theta+\pi/2)}r'\theta'$$是**惯性加速度**，与环向一致，大小为$$2rr'\theta'$$。