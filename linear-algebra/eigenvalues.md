# 特征值

## 不变子空间

依然考虑线性方程组$$Ax=v$$，我们将其重新写成

$$\begin{pmatrix}A_{LU}&A_{RU}\\A_{LD}&A_{RD}\end{pmatrix}\begin{pmatrix}x_U\\x_D\end{pmatrix}=\begin{pmatrix}v_U\\v_D\end{pmatrix}$$

通常，如果恰巧有$$A_{RU}=0,A_{LD}=0$$，我们能更快地解出方程。因为这时有$$A_{LU}x_U=v_U,A_{RD}x_D=v_D$$，可以分别解出$$x_U,x_D$$。这意味着存在向量子空间$$V_U,V_D$$，满足$$(x_U,0)\in V_U,(0,X_D)\in V_D$$，且$$AV_U\subseteq V_U,AV_D\subseteq V_D$$，我们称$$V_U,V_D$$是$$A$$的**不变子空间**。

## 特征值分解

我们尝试寻找$$A$$的一维向量子空间$$V_1\subseteq V$$，应有$$AV_1\subseteq V_1$$。取$$V_1$$的一个基向量$$\xi$$，因为$$A\xi$$也在$$V_1$$中，存在常数$$\lambda$$，满足$$A\xi=\lambda\xi$$。等价的，有$$(A-\lambda I)\xi=0$$，称作**特征方程**。根据克拉默法则，该方程存在非零解$$\xi$$当且仅当$$\det(A-\lambda I)=0$$。这是关于$$\lambda$$的$$n$$次多项式，称为**特征多项式**，特征多项式的根$$\lambda_1,\ldots,\lambda_n$$称为**特征值**，相对应的解$$\xi_k$$，满足$$A\xi_k=\lambda_k\xi_k$$，称为**特征向量**。于是，我们就找到了$$n$$个一维不变子空间的基，这些基构成的空间称为**特征子空间**。

我们将$$n$$个方程合起来写成矩阵形式，得到$$AX=X\Lambda$$，其中$$\Lambda=\mathop{diag}\{\lambda_1,\ldots,\lambda_n\}$$是特征值构成的对角矩阵，$$X=(\xi_1, \ldots, \xi_n)$$是特征向量构成的矩阵，如果$$X$$可逆，即每个特征子空间相互独立，则还可写成$$A=X\Lambda X^{-1}$$，称为矩阵$$A$$的**特征值分解**。如果矩阵$$A$$是对称的，则$$X\Lambda X^{-1}=A=A^T=X^{-T}\Lambda X^T$$，或者，$$(X^TX)\Lambda=\Lambda(X^TX)$$，因此$$X^TX=kI$$，适当调整$$X$$可以使得$$k=1$$，则有$$XX^T=X^TX=I$$，那么$$A=X\Lambda X^T$$。

## 性质

* $$A^n=(X\Lambda X^{-1})^n=X\Lambda (X^{-1}X)\Lambda (X^{-1}\cdots X)\Lambda X^{-1}=X\Lambda^n X^{-1}$$

* $$A^{-1}=X\Lambda^{-1}X^{-1}$$

* $$\det A=\det (X\Lambda X^{-1})=\det X\det \Lambda \det X^{-1}=\det \Lambda = \displaystyle{\prod_{k=1}^n}\lambda_k$$

* $$\mathop{tr} A =\mathop{tr}(X\Lambda X^{-1})=\mathop{tr}(XX^{-1}\Lambda) =\mathop{tr}\Lambda=\sum_{k=1}^n\lambda_k$$

## 应用

考虑线性分式变换$$f(x)=\dfrac{ax+b}{cx+d}$$，注意到$$f^2(x)=f\circ f(x)=\dfrac{(a^2+bc)x+(ab+bd)}{(ac+ad)x+(bc+d^2)}$$，类似有$$\begin{pmatrix}a&b\\c&d\end{pmatrix}^2=\begin{pmatrix}a^2+bc&ab+bd\\ac+cd&bc+d^2\end{pmatrix}$$，故$$f^n(x)$$可通过$$A^n$$计算。再考虑常系数线性数列$$f_n=a_1f_{n-1}+a_2f_{n-2}$$可写成矩阵形式$$\begin{pmatrix}f_{n}\\f_{n-1}\end{pmatrix}=\begin{pmatrix}a_1&a_2\\1&0\end{pmatrix}\begin{pmatrix}f_{n-1}\\f_{n-2}\end{pmatrix}$$，则$$\begin{pmatrix}f_{n}\\f_{n-1}\end{pmatrix}=\begin{pmatrix}a_1&a_2\\1&0\end{pmatrix}^{n-1}\begin{pmatrix}f_{1}\\f_{0}\end{pmatrix}$$。

回顾圆锥曲线的定义$$\mathcal C:=\{x \in \mathbb {RP}^2 \vert (x,Ax)=0,A^T=A\}$$，可以选取合适的射影变换$$P$$满足$$(Px,APx)=(x,P^TAPx)=(x,\Lambda x)=0$$，则$$A=P^{-T}\Lambda P^{-1}$$，调整$$P$$使得$$PP^T=P^TP=I$$，则$$A=P\Lambda P^T$$是矩阵$$A$$的特征值分解。进一步还可写作$$A=\sum_{k=1}^3\lambda_k\xi_k\xi^T_k$$。那么，$$x^TAx=\sum_{k=1}^3\lambda_kx^T\xi_k\xi_k^Tx=\sum_{k=1}^3\lambda_k(x^T\xi_k)^2$$，这是圆锥曲线的标准形式。并且，特征向量$$\xi_k$$是圆锥曲线的轴方向，特征值的绝对值$$|\lambda_k|$$与轴长成固定比例。