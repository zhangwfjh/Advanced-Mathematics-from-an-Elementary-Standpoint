# 矩阵

## 定义

我们称一组排成$$n\times m$$的数方阵为**矩阵**，记作：

$$A:=(a_{ij})=\begin{pmatrix}a_{11}&a_{12}&\cdots & a_{1m}\\a_{21}&a_{22} & \cdots & a_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nm}\end{pmatrix}$$

矩阵$$A$$的**转置**记作$$A^T:=(a^T_{ij})=(a_{ji})$$，如果$$n=1$$，则又称为**行向量**；$$m=1$$则又称为**列向量**。

## 矩阵运算

考虑第一节提到的线性方程组

$$\begin{cases}
k_1b_{11}+k_2b_{21}+\cdots+k_nb_{n1}=v_1 &(1) \\
k_1b_{12}+k_2b_{22}+\cdots+k_nb_{n2}=v_2 &(2)\\
\qquad\vdots \\
k_1b_{1n}+k_2b_{2n}+\cdots+k_nb_{nn}=v_n &(n)
\end{cases}$$

其中每个方程$$(m)$$可以写成点积形式$$k\cdot b^T_m=\sum_{i=1}^nk_ib_{im}=v_m$$，如果记基向量构成的向量$$B:=(b^T_1, b^T_2, \ldots, b^T_n)$$，则方程组还可写为$$kB=v$$。写回分量形式，

$$\begin{pmatrix}k_1&k_2&\cdots&k_n\end{pmatrix}\begin{pmatrix}b_{11}&b_{12}&\cdots & b_{1n}\\b_{21}&b_{22} & \cdots & b_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ b_{n1} & b_{n2} & \cdots & b_{nn}\end{pmatrix}=\begin{pmatrix}k\cdot b^T_1&k\cdot b^T_2&\cdots& k\cdot b^T_n\end{pmatrix}=\begin{pmatrix}v_1 & v_2 &\cdots& v_n\end{pmatrix}$$

该方程的几何解释为向量$$v$$在基$$B$$下的坐标是$$k$$，因为$$k_1b_1+k_2b_2+\cdots+k_nb_n=v$$。

自然地，我们将上面的运算定义为行向量与矩阵的乘积，即$$(kB)_m:=k\cdot b^T_m=\sum_{i=1}^nk_ib_{im}$$。类似地，两个矩阵$$A=(a_1~ a_2~\ldots~ a_m), B=(b_1^T,b_2^T,\ldots,b_n^T)$$的乘积定义为$$(AB)_{ij}:=a_i\cdot b^T_j=\sum_{k=1}^la_{ik}b_{kj}$$。

$$AB=\begin{pmatrix}-a_1-\\-a_2-\\\vdots\\-a_m-\end{pmatrix}\begin{pmatrix}|&|& &|\\b^T_1&b^T_2&\cdots&b^T_n\\|&|& &|\end{pmatrix}=\begin{pmatrix}a_1\cdot b^T_1&a_1\cdot b^T_2&\cdots & a_1\cdot b^T_n\\a_2\cdot b^T_1&a_2\cdot b^T_2 & \cdots & a_2\cdot b^T_n \\ \vdots & \vdots & \ddots & \vdots \\ a_m\cdot b^T_1 & a_m\cdot b^T_2 & \cdots & a_m\cdot b^T_n\end{pmatrix}$$

显然，矩阵乘法不满足交换律，但是满足结合律。

**注意** _不是任意两个矩阵都能相乘，只当前一个矩阵的列数等于后一个矩阵的行数时才可相乘。例如，如果_$$A$$_的大小为_$$m\times l$$_，_$$B$$_的大小为_$$l\times n$$_，则_$$AB$$_的大小为_$$m\times n$$_。_  
**注意** _如果将_$$L_A(B):=AB$$_看成是关于矩阵_$$B$$_的函数，则矩阵_$$A$$_相当于对_$$B$$_的每一列进行相同的**行变换**操作；如果将_$$R_B(A):=AB$$_看成是关于矩阵_$$A$$_的函数，则矩阵_$$B$$_相当于对_$$A$$_的每一行进行相同的**列变换**操作。_

我们还可以定义矩阵的加法和数乘：

* 如果矩阵$$A,B$$大小相同，则$$A+B:=(a_{ij}+b_{ij})$$
* $$kA:=(ka_{ij})$$

因此，所有$$m\times n$$的矩阵构成了$$mn$$维的向量空间。我们还可以对$$n\times n$$的所有矩阵定义内积$$(A,B):=\sum_{k=1}^n(AB)_{kk}$$使构成内积空间，或者定义李括号$$[A,B]:=AB-BA$$构成李代数。读者可以自行验证以上定义满足内积和李代数的性质。

如果$$n\times n$$的矩阵满足$$a_{ij}=0$$对于所有$$i\neq j$$都成立，则称$$A$$为**对角矩阵**。如果对角矩阵的每一项都等于$$k$$，则称为**数量矩阵**。再如果$$k=1$$，则称为**单位矩阵**。数量矩阵满足：

$$\begin{pmatrix}k&0&\cdots&0\\0&k&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&k\end{pmatrix}\begin{pmatrix}a_{11}&a_{12}&\cdots & a_{1m}\\a_{21}&a_{22} & \cdots & a_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nm}\end{pmatrix}=\begin{pmatrix}ka_{11}&ka_{12}&\cdots & ka_{1m}\\ka_{21}&ka_{22} & \cdots & ka_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ ka_{n1} & ka_{n2} & \cdots & ka_{nm}\end{pmatrix}=k\begin{pmatrix}a_{11}&a_{12}&\cdots & a_{1m}\\a_{21}&a_{22} & \cdots & a_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nm}\end{pmatrix}$$

单位矩阵从另一个角度扮演着恒等变换$$I$$的角色。如果两个矩阵$$A,B$$满足$$AB=BA=I$$，则称$$A,B$$**互逆**，且记$$B=A^{-1}$$。对于线性方程组$$kB=v$$来说，如果$$A=B^{-1}$$，则$$vA=(kB)B^{-1}=kI=k$$是方程的解。

不难证明，矩阵的逆和转置具有以下性质:

* $$(A^T)^T=A, (AB)^T=B^TA^T$$
* $$(AB)^T=B^TA^T, (AB)^{-1}=B^{-1}A^{-1}$$

## 矩阵函数

### 秩

考虑矩阵$$A:=\begin{pmatrix}a_1& a_2& \ldots& a_n\end{pmatrix}$$，行向量$$a_1, a_2, \ldots, a_n$$的所有线性组合构成一个向量子空间，称为**行空间**，该空间的维数称作矩阵$$A$$的**行秩**。类似地，矩阵$$B:=(b^T_1, b^T_2, \ldots, b^T_n)$$的列向量的有限性组合构成一个向量子空间，称为**列空间**，该空间的维数称作矩阵$$B$$的**列秩**。对于任意矩阵，行秩等于列秩，统称为**秩**，记作$$\mathop{rk}A$$。

**证明**： ？

矩阵的秩有以下性质：

* $$\mathop{rk}A=\mathop{rk}A^T=\mathop{rk}AA^T=\mathop{rk}A^TA$$
* $$\mathop{rk}(A+B) \leq \mathop{rk}A + \mathop{rk}B$$
* $$\mathop{rk}AB \leq \min\{\mathop{rk}A,\mathop{rk}B\}$$

### 行列式

上节中，我们已经定义了$$n \times n$$的矩阵行列式，我们将它记作$$\det A:=\sum_{k_1, k_2, \cdots, k_n=1}^n\varepsilon_{k_1k_2\cdots k_n}~a_{1k_1}a_{2k_2}\cdots a_{nk_n}$$。行列式具有以下性质：

1. $$\det I = 1$$
2. $$\det A = \det A^T$$
3. $$\det A^{-1} = (\det A)^{-1}$$
4. $$\det AB = \det A \det B$$
5. $$\det kA = k^n\det A$$

我们只证明性质4，其余性质是上节的直接推论。

**证明**：令矩阵$$A,B$$分别按照行、列展开有$$A=(a_1~a_2~\cdots~a_n), B=(b_1^T,b_2^T,\cdots,b_n^T)$$，则矩阵$$A$$的可以看做是向量$$\{a_i\}_1^n$$在基$$\{b^T_i\}_1^n$$下的坐标表示，因此$$\det AB=|\sum_{k_1=1}^na_{1k_1}b_{k_1}\wedge\cdots\wedge\sum_{k_n=1}^na_{nk_n}b_{k_n}|$$，根据行列式的多线性和反交换性，有$$\det AB=\sum_{k_1,\cdots, k_n=1}^n\varepsilon_{k_1\cdots k_n}~a_{1k_1}\cdots a_{nk_n}|b_1\wedge\cdots\wedge b_n|$$，比较行列式定义，这正是$$\det A|b_1\wedge\cdots\wedge b_n|$$，亦是$$\det A\det B$$。

行列式还可用于线性方程的求解，考虑线性方程组$$k_1b_1+k_2b_2+\cdots+k_nb_n=v$$，记$$b_{-m}=b_1\wedge\cdots\wedge\hat {b_m}\wedge\cdots\wedge b_n$$，其中，$$\hat {b_m}$$表示忽略该项，则有$$b_i\wedge b_{-m}=\delta_{im}b_m\wedge b_{-m}$$，将方程两边同时乘以$$b_{-m}$$，得到$$v\wedge b_{-m}=k_mb_m\wedge b_{-m}$$。此时方程两边均是$$n$$-向量，故系数$$k_m$$是两有向平行体的体积比，即$$k_m=|v\wedge b_{-m}|/|b_m\wedge b_{-m}|$$。通过调整顺序，还可写为$$k_m=\dfrac{\begin{vmatrix}|& &|& &|\\b^T_1&\cdots&v^T&\cdots&b^T_n\\|& &|& &|\end{vmatrix}}{\begin{vmatrix}|& &|& &|\\b^T_1&\cdots&b^T_m&\cdots&b^T_n\\|& &|& &|\end{vmatrix}}$$，这种解方程的方法称做**克拉默法则**。

### 迹

定义矩阵的对角线和为矩阵的**迹**，记作$$\mathop{tr} A:=\sum_{k=1}^nA_{kk}$$。不难证明，矩阵的迹满足：

* $$\mathop{tr}(A+B) = \mathop{tr} A + \mathop{tr} B$$        
* $$k\mathop{tr} A = \mathop{tr} (kA)$$ 对任意常数$$k\in\mathbb R$$成立        
* $$\mathop{tr} AB = \mathop{tr} BA$$

## 矩阵表示

考虑两个向量空间之间的映射$$L:V\to W$$，如果满足对任意$$u,v \in V, a,b \in \mathbb R$$满足$$L(au+bv)=aL(u)+bL(v)$$，则称$$L$$是从$$V$$到$$W$$的**线性变换**。给定$$V$$和$$W$$中的基$$\{e_i\}_1^n,\{f_j\}_1^m$$，则存在矩阵$$M$$使得$$L(e_i)=\sum_{j=1}^mM_{ij}f_j$$，我们称矩阵$$M$$是$$L$$的**矩阵表示**。我们来看几个例子。

* 复数：将复数$$z=a+bi$$看成二维向量$$z=(a,b)$$，则复数乘法$$(a,b)(c,d)=(ac-bd,ad+bc)$$是从$$\mathbb C$$到$$\mathbb C$$的线性变换，对应的矩阵表示为$$M_z=\begin{pmatrix}a&-b\\b&a\end{pmatrix}$$。特别地，单位复数$$z=\mathop{cis}\theta$$表示二维旋转，可用矩阵表示为$$\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}$$。

* 对偶数：对偶数$$a+b\epsilon$$也可看作二维向量$$(a,b)$$，对偶数乘法$$(a,b)(c,d)=(ac,ad+bc)$$也是从$$\mathbb R^\epsilon$$到自身的线性变换，对应的矩阵表示为$$\begin{pmatrix}a&0\\b&a\end{pmatrix}$$。

* 多项式：$$n$$阶一元多项式$$P(x)=a_0+a_1x+\cdots+a_nx^n$$可看作$$(n+1)$$-维向量$$p=(a_0,a_1,\cdots,a_n)$$，对$$x$$的导数是从$$\mathbb R^{n+1}$$到$$\mathbb R^{n}$$的线性运算，导数对应的矩阵表示$$D=\begin{pmatrix}0&1&0&\cdots&0\\0&0&2&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&0&\cdots&n\end{pmatrix}_{n\times(n+1)}$$，不难验证，$$Dp=(a_1,2a_2,\ldots,na_n)$$。类似地，积分也是从$$\mathbb R^{n+1}$$到$$\mathbb R^{n+2}$$的线性运算，对应的矩阵表示为$$S=\begin{pmatrix}0&0&\cdots&0\\1&0&\cdots&0\\0&\dfrac12&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&\dfrac1n\end{pmatrix}_{(n+2)\times(n+1)}$$，且$$Sp=(0,a_0,\frac12a_1,\ldots,\frac1{n+1}a_n)$$。



