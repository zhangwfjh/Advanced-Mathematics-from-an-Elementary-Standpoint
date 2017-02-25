# 向量

## 向量空间

考虑所有$$n$$元实数有序对构成的集合$$V:=\{a:=(a_1, a_2,\ldots,a_n)\vert a_i \in \mathbb R\}=\mathbb R^n$$，称为**向量空间**，向量空间中的每一个元素$$a$$称为$$n$$维**向量**。再定义向量空间上的加法和数乘，统称为**线性运算**，满足：

* $$a \pm b:=(a_1 \pm b_1, a_2 \pm b_2, \ldots, a_n \pm b_n)$$
* $$ka := (ka_1, ka_2, \ldots, ka_n)\quad(k \in \mathbb R)$$

显然，向量的加法满足交换律和结合律，且数乘对加法也满足分配律。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a6/Vector_add_scale.svg/400px-Vector_add_scale.svg.png)

第一章中提到，广义的说，数可以表示一个量，也可以表示一种操作。向量也是这样一种数，它代表空间中的一个平移操作，向量加法是两个平移的复合，数乘是平移量的放缩。两个平移的两种复合方式构成了平行四边形的四条边，是交换律的体现，称作**平行四边形法则**。

实际上，我们之前已经遇到过多种向量空间。例如实数域$$\mathbb R$$是一维向量空间，复数域$$\mathbb C$$是二维向量空间，$$n$$阶多项式构成$$n$$维空间，柯西数列$$\mathscr C$$构成了无穷维空间，实函数空间也是无穷维空间。读者请自行证明。

对于向量空间$$V$$的一个子集$$U \subseteq V$$，如果任意$$a,b \in U, k \in \mathbb R$$，满足$$a+b \in U, ka \in U$$，则称$$U$$为$$V$$的一个**向量子空间**。

## 基与坐标

取一族非零向量$$\mathscr B=\{b_1, b_2,\ldots,b_m\}\subseteq V$$，以及一组数$$k_1,k_2,\cdots,k_m$$，则向量$$v=\sum_{i=1}^mk_ib_i$$称作$$\mathscr B$$的一个**线性组合**。如果$$\mathscr B$$还满足任意向量$$b_k$$都不是$$\mathscr B$$的线性组合，则称$$\mathscr B$$为一个**线性无关族**。如果还有$$m=n$$，则称$$\mathscr B$$为向量空间$$V$$的一族**基**。

我们证明，给定向量空间$$V$$的一族基$$\mathscr B$$，则任意向量$$v \in V$$都是基向量的线性组合，并且存在唯一系数$$k_1,k_2,\ldots,k_n$$满足$$v=\sum_{i=1}^mk_ib_i$$，这组系数称为$$v$$在$$\mathscr B$$下的**坐标**。

**证明**： 只需计算$$v$$的坐标，即系数$$k$$，按向量的定义展开$$v=\sum_{i=1}^mk_ib_i$$，得到线性方程组，

$$\begin{cases}
k_1b_{11}+k_2b_{21}+\cdots+k_nb_{n1}=v_1 &(1) \\
k_1b_{12}+k_2b_{22}+\cdots+k_nb_{n2}=v_2 &(2)\\
\qquad\vdots \\
k_1b_{1n}+k_2b_{2n}+\cdots+k_nb_{nn}=v_n &(n)
\end{cases}$$

我们使用数学归纳法证明该方程存在唯一解。当$$n=1$$时，显然$$k_1=v_1/b_1$$是唯一解。我们假设$$b_{nn}\neq0$$，则将方程$$(m)$$减去方程$$(n)$$两边乘以$$b_{nm}/b_{nn}$$得到

$$\begin{cases}
k_1b_{11}'+k_2b_{21}'+\cdots+k_{n-1}b_{n-1,1}'=v_1-b_{n1}/b_{nn}v_n &(1') \\
k_1b_{12}'+k_2b_{22}'+\cdots+k_{n-1}b_{n-1,2}'=v_2-b_{n2}/b_{nn}v_n &(2')\\
\qquad\vdots \\
k_1b_{1,n-1}'+k_2b_{2,n-1}'+\cdots+k_{n-1}b_{n-1,n-1}'=v_{n-1}-b_{n,n-1}/b_{nn}v_n &(n-1')\\
k_1b_{1n}+k_2b_{2n}+\cdots+k_nb_{nn}=v_n &(n)
\end{cases}$$

其中$$b_{ml}'=b_{ml}-b_{mn}b_{nl}/b_{nn}$$。假设线性方程组$$(1')\sim(n-1')$$有唯一解$$k_1,k_2,\ldots,k_{n-1}$$，那么，对于$$n$$维向量空间，不难解出$$k_n=(v_n-(k_1b_{n1}+k_2b_{n2}+\cdots+k_{n-1}b_{n,n-1}))/b_{nn}$$。因此方程$$(1)\sim(n)$$存在唯一解。这种线性方程组的归纳解法称为**高斯消元法**。

这个命题还告诉了我们基向量的个数就是向量空间的维数。$$v=(v_1,v_2,\ldots,v_n)$$可以看作是向量$$v$$在基$$\{e_i\}_1^n$$下的坐标，其中$$e_i$$的第$$i$$个分量为$$1$$，其余分量为$$0$$。因此，向量也可以看作是$$n$$维空间中的一个点。

**注意** _向量本身与坐标是无关的，选择不同的基，同一个向量将有不同的坐标表示。有时，我们选取合适的基来简化坐标运算。_

## 向量乘积

### 内积

定义向量的**点积**$$a\cdot b:=\left< a, b\right>:=\sum_{k=1}^na_kb_k$$。（请注意，向量的点积是一个数，而非向量，所以点积严格来说并不能称作乘法。）特别地，如果$$b=a$$，则有$$a \cdot a=:a^2=\sum_{k=1}^na_k^2$$，根据勾股定理，$$a^2$$表示点$$a$$到原点$$O$$距离的平方，我们记$$|a|:=\sqrt{a^2}$$为向量$$a$$的**模长**，也称**范数**。根据余弦定理，如果向量有三角形$$a=b+c$$，则$$(a-b)^2=c^2=a^2+b^2-2|a||b|\cos\angle ab$$，或者$$a \cdot b= |a||b|\cos\angle ab$$。即，点积$$a\cdot b$$表示两向量$$a,b$$的模长乘以它们夹角的余弦。特别地，如果$$a\perp b$$，则有$$a\cdot b=|a||b|\cos(\pm\pi/2)=0$$。

因为$$0\leq\cos\angle ab\leq 1$$，我们得到**柯西不等式**$$a\cdot b\leq |a||b|$$，写成分量形式为$$\sum_{k=1}^na_kb_k\leq\sqrt{(\sum_{k=1}^na_k^2)(\sum_{k=1}^nb_k^2)}$$。

不难证明，点积满足以下性质：

* 对称性：$$(a,b) = (b,a)$$
* 双线性：对于常数$$k$$，$$(ka,b)=k(a,b)=(a,kb)$$；对于向量$$c$$，$$(a+c,b)=(a,b)+(c,b)$$
* 正定性：$$(a,a)\geq 0$$，$$(a,a)=0$$当且仅当$$a=0$$

一般的，凡是满足以上三条性质的运算称为**内积**，定义了内积的向量空间称为**内积空间**。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Inner-product-angle.png/600px-Inner-product-angle.png)

### 叉积

对于三维空间，还可以定义向量的**叉积**$$a\times b:=[a,b]=(a_2b_3-a_3b_2,a_3b_1-a_1b_3,a_1b_2-a_2b_1)$$。请注意，$$a\times b=-b\times a$$，即向量的叉积不满足交换律，而满足**反交换律**。若令$$b=a$$，则$$a \times a=-a\times a=0$$，因此两向量叉积等于$$0$$当且仅当两向量共线。通过繁琐的代数计算，我们还有$$a\times(b\times c)=(a \cdot c)b-(a\cdot b)c$$，所以$$(a\times b)\times c \neq a\times(b\times c)$$，即叉积亦不满足结合律。

通过计算，我们有$$a\cdot(b\times a)=b\cdot(b\times a)=0$$，所以$$a\times b\perp a,b$$。以及，$$(a\times b)^2=a^2b^2-(a\cdot b)^2=(|a||b|\sin\angle ab)^2$$，所以$$a\times b$$的模长是以$$a,b$$为边的平行四边形的面积。如果还有向量$$c$$，则不难看出**混合积**$$a\cdot(b\times c)$$表示向量$$a,b,c$$围成的平行六面体的体积，且有$$a\cdot(b\times c)=b\cdot(c\times a)=c\cdot(a\times b)$$。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Cross_product_parallelogram.svg/440px-Cross_product_parallelogram.svg.png)

可以验证叉积满足以下性质：

* 反对称性：$$[a,b]=-[b,a]$$，等价地，$$[a,a]=0$$
* 双线性：对于常数$$k$$，$$[ka,b]=k[a,b]=[a,kb]$$；对于向量$$c$$，$$[a+c,b]=[a,b]+[c,b]$$
* 雅克比等式：$$[a,[b,c]]+[b,[c,a]]+[c,[a,b]]=0$$

一般的，凡是满足以上三条性质的运算称为**李括号**，定义了李括号的向量空间称为**李代数**。

**注意** _**双线性**是两种乘法，内积和李括号，都满足一个重要的性质，也是所有乘法均满足的性质。_

