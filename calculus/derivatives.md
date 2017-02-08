# 导数

## 定义

考虑实函数$$y=f(x)$$，$$f$$可看作定义域到值域的一个伸缩形变。例如，在下图中，红色部分是一个等距平移，绿色部分是一个拉伸，蓝色部分是一个反向拉伸，紫色部分是一个压缩。为了研究函数$$f$$的形变情况，可以定义形变率。

![](/assets/derivatives1.png)

具体来说，定义实数域$$\mathbb R$$上的一个有序对$$(a,b)$$为一个**有向区间**（不必有$$a \lt b$$），$$\overline{ab}:=b-a$$为$$(a,b)$$的**有向长度**。那么，函数$$f$$在有向区间$$(a,b)$$的形变率$$k_f(a,b)=\dfrac{\overline{f(a)f(b)}}{\overline{ab}}$$。如果函数$$f$$是线性函数，即对任意$$(a,b)$$满足$$\overline{f(a)f(b)}=f(\overline{ab})$$，则$$k_f(a,b)=\dfrac{f(\overline{ab})}{\overline{ab}}=f(1)$$是常数，所以线性函数在每一点具有相同的形变率。显然，如果将函数$$f$$平移至$$g(x)=f(x)+c$$，则$$g(x)$$在每一个有向区间上的形变率不变。因此，仿射函数（线性函数的平移）在每一点也具有相同的形变率。

在上图中，函数$$f(x)$$在红、蓝、紫色区间内是仿射函数，每一点的形变率可以由有向区间长度比直接求出；而在绿色区间内，定义域上相同长度的有向子区间在不同位置被$$f$$拉伸成为值域上不同长度的有向子区间。为了计算函数$$f$$在一点$$x$$的形变率，我们在充分小的有向区间$$(x,x')$$内，用一个仿射函数$$\tilde f$$逼近函数$$f$$，用仿射函数$$\tilde f$$的形变率作为函数$$f$$在点$$x$$的形变率，即$$k_f(x):=k_{\tilde f}$$。

我们计算$$k_{\tilde f}$$，由于函数$$\tilde f$$的定义域$$(x,x')$$充分小，可考虑极限$$x'\to x$$，则$$k_{\tilde f}=\lim_{x'\to x}\dfrac{\overline{\tilde f(x)\tilde f(x')}}{\overline{xx'}}=\lim_{x'\to x}\dfrac{\tilde f(x')-\tilde f(x)}{x'-x}=\lim_{x'\to x}\dfrac{f(x')-f(x)}{x'-x}$$。等价地，如果扩展$$f$$到超实数域$$^*f$$，则$$k_{\bar f}=\mathop{st}\dfrac{^*f(^*x)-{}^*f(x)}{^*x-x}=\mathop{st}\dfrac{^*f(x+\varepsilon)-{}^*f(x)}{\varepsilon}$$。

我们称函数$$f$$在点$$x$$的变形率为**导数**，记作$$f'(x):=k_f(x)$$，导数是$$x$$的函数，也称$$f'$$是$$f$$的**导函数**。仿射函数$$\tilde f_x$$称为$$f$$在点$$x$$的**一阶逼近**，$$df_x=\overline{\tilde f(x)\tilde f(x+\varepsilon)}$$称为$$f$$在点$$x$$的**微分**。令恒等函数$$\iota(x)=x$$，则$$d\iota_x=dx=\varepsilon$$，则$$f'=\dfrac{df}{dx}$$，故导数也称为**微商**。

