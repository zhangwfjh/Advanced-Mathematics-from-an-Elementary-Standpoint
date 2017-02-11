# 向量

## 向量空间

考虑所有$$n$$元实数有序对构成的集合$$V:=\{\boldsymbol a:=(a_1, a_2,\ldots,a_n)\vert a_i \in \mathbb R\}$$，称为**向量空间$$V$$**，向量空间中的每一个元素$$\vec a$$称为$$n$$维**向量**。再定义向量空间上的加法和数乘，统称为**线性运算**，满足：
* $$\vec a \pm \vec b:=(a_1 \pm b_1, a_2 \pm b_2, \ldots, a_n \pm b_n)$$
* $$k \vec a := (ka_1, ka_2, \ldots, ka_n)\quad(k \in \mathbb R)$$

显然，向量的加法满足交换律和结合律，且数乘对加法也满足分配律。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a6/Vector_add_scale.svg/400px-Vector_add_scale.svg.png)

第一章中提到，广义的说，数可以表示一个量，也可以表示一种操作。向量也是这样一种数，它代表空间中的一个平移操作，向量加法是两个平移的复合，数乘是平移量的放缩。两个平移的两种复合方式构成了平行四边形的四条边，是交换律的体现，称作**平行四边形法则**。

实际上，我们之前已经遇到过多种向量空间。例如实数域$$\mathbb R$$是一维向量空间，复数域$$\mathbb C$$是二维向量空间，$$n$$阶多项式构成$$n$$维空间，柯西数列$$\mathscr C$$构成了无穷维空间，实函数空间也是无穷维空间。读者请自行证明。

##