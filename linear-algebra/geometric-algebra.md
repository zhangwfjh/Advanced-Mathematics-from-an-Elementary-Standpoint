# 几何代数

## 克利福德代数

上节中定义了两种向量乘法，点积和叉积，我们发现乘法只是一种可定义的操作。两个向量相乘可以是一个向量，也可以是一个数；乘法还可以不满足交换律。但是，乘法一定满足双线性，或者说，数与向量是兼容的。我们尝试定义一般的向量乘法$$*$$，只假设满足结合律和双线性。

### $$\mathcal{Cl}(\mathbb R^2)$$

我们首先考虑二维向量空间$$V=\mathbb R^2$$，取基向量$$\{e_1,e_2\}$$，则对任意两个向量$$a=a_1e_1+a_2e_2, b=b_1e_1+b_2e_2$$，我们将两个向量相乘得到$$a*b=(a_1e_1+a_2e_2)*(b_1e_1+b_2e_2)=a_1b_1e_1*e_1+a_1b_2e_1*e_2+a_2b_1e_2*e_1+a_2b_2e_2*e_2$$，注意这个等式用到了乘法的双线性性质。等式右边的式子太过于一般，并且不知道应该如何解释形如$$e_i*e_j$$的项，为了赋予乘法一定的几何意义，我们需要对进行进一步假设。

* $$e_1*e_1=e_2*e_2=1, e_1*e_2=e_2*e_1=0$$。在这种假设下，$$a*b=a_1b_1+a_2b_2=a\cdot b$$，我们得到了向量的点积。

* $$e_1*e_1=e_2*e_2=0, e_1*e_2=-e_2*e_1$$。则$$a*b=(a_1b_2-a_2b_1)e_1*e_2=a \times b$$，我们又得到了向量的叉积(二维叉积可看作三维叉积在第三分量上的投影)。

* $$e_1*e_1=e_2*e_2=1,e_1*e_2=-e_2*e_1$$。则$$a*b=:ab=a\cdot b+a\times b$$，将点积和叉积统一成了一个乘法，称作**几何积**。

* $$e_1*e_1=0, e_2*e_2=e_2, e_1*e_2=e_2*e_1=e_1$$。得到$$a*b=(a_1b_2+a_2b_1)e_1+(a_2b_2)e_2$$，如果将$$e_1,e_2$$的系数分别看作比例数的分子和分母，则该乘法表示了比例数的乘法。

* $$e_1*e_1=-e_2*e_2=e_1, e_1*e_2=e_2*e_1=e_2$$。我们有$$a*b=(a_1b_1-a_2b_2)e_1+(a_1b_2+a_2b_1)e_2$$，如果令$$e_1=1,e_2=i$$分别看作实单位和虚单位，则该向量乘法正是复数的乘法。

* $$e_1*e_1=1, e_2*e_2=0, e_1*e_2=e_2*e_1=e_2$$。则$$a*b=a_1b_1+(a_1b_2+a_2b_1)e_2$$，若将$$e_2$$看作无穷小量$$\epsilon$$，则该乘法又是对偶数乘法。

### $$\mathcal{Cl}(\mathbb R^3)$$

现在考虑$$V=\mathbb R^3$$，以及基向量$$\{e_1,e_2,e_3\}$$，类似计算两个向量$$a,b$$的乘法。

* $$e_i^2=0,e_ie_j+e_je_i=0$$，满足该性质的乘积称作**外积**，具体有$$a\wedge b:=a*b=(a_1b_2-a_2b_1)e_1*e_2+(a_2b_3-a_3b_2)e_2*e_3+(a_3b_1-a_1b_3)e_3*e_1$$。如果再令$$e_1*e_2=e_3,e_2*e_3=e_1,e_3*e_1=e_2$$，则等式右面的最后三项可以写为$$a\times b$$，故外积与叉积类似，可以表示两向量构成的平行四边形的面积。再计算$$a\wedge b\wedge c=(a_1b_2c_3+a_2b_3c_1+a_3b_1c_2-a_1b_3c_2-a_2b_1c_3-a_3b_2c_1)e_1*e_2*e_3$$。若令$$e_1*e_2*e_3=1$$，则又有$$\wedge b\wedge c=a\cdot(b\times c)$$是混合积，可以表示三向量构成的平行六面体体积。

* $$e_i^2=1,e_ie_j+e_je_i=0$$，满足这个性质的乘法称作**几何积**，具体有$$ab:=a*b=a\cdot b+a\wedge b$$，$$abc=(a\cdot b)c+(b\cdot c)a+(c\cdot a)b+a\wedge b\wedge c$$。

* $$e_i^2=-1,e_1*e_2*e_3=-1$$，根据假设，容易导出$$e_1*e_2=e_3,e_2*e_3=e_1,e_3*e_1=e_2$$以及$$e_ie_j+e_je_i=0$$，因此$$a*b=-a\cdot b + a\times b$$。实际上，满足这些关系的所有形如$$a_0+a_1e_1+a_2e_2+a_3e_3$$的数构成**四元数**$$\mathbb H$$。

以上例子通过定义基的乘法$$e_i*e_j$$赋予向量乘法不同的意义，但是，如果换一组基，或者说换一个坐标，则乘法将有不同的形式。为了使乘法的定义与基的选取无关，我们只需要对每一个向量$$v\in V$$定义形如$$v^2=v*v$$的项的值即可，因为$$e_i$$是基向量，则$$e_i^2$$已定义，而$$e_i*e_j=((e_i+e_j)^2-e_i^2-e_j^2)/2$$也能够定义。我们说，如果对于任意向量$$v\in V$$，定义了$$Q(v)=v^2$$，称作**二次型**，则二次型自然地导出向量空间上的乘法，我们称这个向量空间是一个**克利福德代数**，记作$$\mathcal{Cl}(V,Q)$$。因为乘法具有双线性，还要求有$$Q(kv)=(kv)\wedge(kv)=k^2v^2=k^2Q(v)$$。

## 外代数

### 外积

前面我们看到外积运算有非常显著的几何意义，因为它能直接给出平行体的面积或体积，我们现在着重讨论$$n$$维向量空间$$V=\mathbb R^n$$中的外积运算。具体来说，外积是一种双线性运算，满足：

* 双线性：$$(ka+lb)\wedge c = ka\wedge c+lb\wedge c$$对任意$$k,l\in\mathbb R$$成立
* 结合律：$$(a\wedge b)\wedge c = a \wedge (b\wedge c)$$
* 反交换律：$$a\wedge b = -b\wedge a$$，等价地，$$Q(a):=a\wedge a = 0$$

实际上，我们知道$$a,b,c\in V$$是向量空间中的向量，但我们并未说明什么是$$a\wedge b$$或者$$a\wedge b\wedge c$$，更别提把他们相加是什么。在三维空间中，$$a\wedge b$$可以用一个同时垂直于$$a,b$$的向量$$a\times b$$来表示，但是对于一般的高维空间，则不存在唯一的垂直于$$a,b$$的向量，或者说，存在无穷多个这样的向量。不过，我们不必纠结于究竟$$a\wedge b$$用什么数或者什么向量来表示，我们就将它视为独立的对象，称作**2-向量**。不难验证，所有的2-向量同样构成向量空间，记作$$\Lambda^2(V)$$。正如多项式中的变量$$x$$，复数中的虚单位$$i$$和对偶数中的无穷小量$$\epsilon$$，我们不把$$x,i,\epsilon$$用什么数来表示，它们就是它们本身，只要遵循一定的代数运算规则即可。

从几何上，我们依然可以赋予2-向量一个很好的解释。如果说向量$$a$$表示一种平移操作，那么2-向量$$a\wedge b$$表示一种从$$a$$向$$b$$的旋转。如果说向量$$a$$表示一条有向线段，则2-向量$$a\wedge b$$表示一个有向平行四边形。一般地，我们称$$a_1\wedge a_2\wedge\cdots\wedge a_r$$为**$$r$$-向量**，所有$$r$$-向量构成的向量空间记为$$\Lambda^r(V)$$，则有$$\Lambda^r(V)\wedge\Lambda^s(V)\subseteq\Lambda^{r+s}(V)$$。

![](https://upload.wikimedia.org/wikipedia/commons/2/21/N_vector_positive_png_version.png)

### 行列式

我们希望计算$$r$$个向量构成的平行体的体积，记为$$|a_1\wedge a_2\wedge\cdots\wedge a_r|$$。首先取一组基$$\{e_k\}_1^n$$满足$$e_i\cdot e_j=\delta_{ij}=\begin{cases}1&i=j\\0&i\neq j\end{cases}$$，称作**标准正交基**。则向量$$a_i$$在这组基下表示为$$a_i=\sum_{k=1}^na_{ik}e_k=(a_{i1},a_{i2},\ldots,a_{in})$$。如果将$$|a_1\wedge a_2\wedge\cdots\wedge a_r|$$用坐标展开，我们得到一组数$$\begin{vmatrix}a_{11}&a_{21}&\cdots & a_{r1}\\a_{12}&a_{22} & \cdots & a_{r2} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1n} & a_{2n} & \cdots & a_{rn}\end{vmatrix}$$。

外积最大的好处就是，它能直接计算$$r$$-向量的**有向体积**。根据定义，$$a \wedge b = (\sum_{i=1}^na_ie_i)\wedge(\sum_{j=1}^nb_je_j)=\sum_{i\neq j}^na_ib_je_i\wedge e_j=\sum_{i\lt j}^n(a_ib_j-a_jb_i)e_i\wedge e_j$$，这将两个向量$$a,b$$构成的有向平行四边形分解成两两垂直的基向量构成的有向平行四边形的$$2$$-向量和。而且$$e_i\wedge e_j$$的系数$$a_ib_j$$正是该分量的面积，由于$$e_j\wedge e_i$$与$$e_i\wedge e_j$$表示相同的平行四边形，只是方向不同，如果选择$$e_i\wedge e_j~(i\lt j)$$为正方向，则$$e_j\wedge e_i$$的面积应为负，即$$-a_jb_i$$，总的来说，在这个平行四边形上的正面积应为$$a_ib_j-a_jb_i$$。如果考虑两向量在$$e_i\wedge e_j$$上的投影$$a^{\{i,j\}},b^{\{i,j\}}$$，则有$$|a^{\{i,j\}}\wedge b^{\{i,j\}}|=\begin{vmatrix}a_i&b_i\\a_j&b_j\end{vmatrix}=a_ib_j-a_jb_i$$。根据勾股定理，$$|a\wedge b|^2=\sum_{i\lt j}^n|a^{\{i,j\}}\wedge b^{\{i,j\}}|^2$$。类似地，我们可以导出$$|a_1\wedge a_2\wedge\cdots\wedge a_r|^2=\sum_{i_1 \lt i_2 \lt \cdots \lt i_r}\begin{vmatrix}a_{1i_1}&a_{2i_1}&\cdots & a_{ri_1}\\a_{1i_2}&a_{2i_2} & \cdots & a_{ri_2} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1i_r} & a_{2i_r} & \cdots & a_{ri_r}\end{vmatrix}^2$$。我们发现，$$r$$行$$r$$列的数组$$\begin{vmatrix}a_{11}&a_{21}&\cdots & a_{r1}\\a_{12}&a_{22} & \cdots & a_{r2} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1r} & a_{2r} & \cdots & a_{rr}\end{vmatrix}$$扮演了重要的作用，它是$$r$$-向量在某个$$r$$维向量子空间中的分量，即$$r$$维有向平行体的有向体积，我们将它定义为**$$r$$阶行列式**。

为了计算$$r$$阶行列式，注意到$$r$$维有向平行体可以分解成$$r!$$个$$r$$-向量$$e_{i_1}\wedge e_{i_2}\wedge\cdots\wedge e_{i_r}$$的有向体积和。对于每个$$e_{i_1}\wedge e_{i_2}\wedge\cdots\wedge e_{i_r}$$，它的面积是$$a_{1i_1}a_{2i_2}\cdots a_{ri_r}$$。又因为每个$$e_{i_1}\wedge e_{i_2}\wedge\cdots\wedge e_{i_r}$$都表示同一个平行体，即$$e_{1}\wedge e_{2}\wedge\cdots\wedge e_{r}$$，只是方向不同。为了确定方向带来的面积符号的变化，只需计算$$e_{i_1}\wedge e_{i_2}\wedge\cdots\wedge e_{i_r}=se_{1}\wedge e_{2}\wedge\cdots\wedge e_{r}$$，其中$$s=\pm1$$。我们发现，如果将$$\sigma:(i_1,i_2,\ldots,i_r)$$通过交换相邻两个数得到$$(1,2,\ldots,r)$$的次数为偶数，则$$s=1$$；若为奇数，则$$s=-1$$，我们将$$s$$也记作$$\mathop{sgn}\sigma$$。因此，我们得到$$r$$阶行列式计算公式$$\begin{vmatrix}a_{11}&a_{21}&\cdots & a_{r1}\\a_{12}&a_{22} & \cdots & a_{r2} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1r} & a_{2r} & \cdots & a_{rr}\end{vmatrix}=\sum_{i_1 \lt i_2 \lt \cdots \lt i_r}s~a_{1i_1}a_{2i_2}\cdots a_{ri_r}=:\sum_\sigma \mathop{sgn}\sigma~a_{1\sigma_1}a_{2\sigma_2}\cdots a_{r\sigma_r}$$