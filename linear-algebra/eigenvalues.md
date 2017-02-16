# 特征值

## 定义

考虑矩阵方程$$Ax=\lambda x$$，其中$$A \in \mathbb R^{n\times n}, x \in \mathbb R^n, \lambda \in \mathbb R$$，该方程表示矩阵$$A$$将向量$$x$$伸缩$$\lambda$$倍。该方程还可以写为$$(A-\lambda I)x=0$$，称作**特征方程**。如果该方程有非零解$$\bar x$$，则对任意$$k\in\mathbb R$$都有$$k\bar x$$也是该方程的解，因此该方程的解存在且不唯一。根据克拉默法则，只有$$\det(A-\lambda I)=0$$，这是关于$$\lambda$$的$$n$$次多项式，称为**特征多项式**。

根据代数基本定理，特征多项式有$$n$$个复数解$$\lambda_1,\ldots,\lambda_n$$，称为**特征值**，相对应的解$$x_k$$，满足$$Ax_k=\lambda_kx_k$$，称为**特征向量**。将$$n$$个方程合起来写成矩阵形式，得到$$AX=X\Lambda$$，其中$$\Lambda=\mathop{diag}\{\lambda_1,\ldots,\lambda_n\}$$是特征值构成的对角矩阵，$$X=(x_1, \ldots, x_n)$$是特征向量构成的矩阵，如果$$X$$可逆，还可写成$$A=X\Lambda X^{-1}$$，称为矩阵$$A$$的特征值分解。