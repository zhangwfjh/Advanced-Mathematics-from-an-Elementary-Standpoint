# 比例数

## 等价关系

定义集合$$S$$上的等价关系$$\sim$$为$$S\times S$$上的一个子集$$R$$，满足：

* 自反性：$$x\sim x$$
* 对称性：$$x \sim y \Rightarrow y \sim x$$
* 传递性：$$x \sim y \wedge y \sim z \Rightarrow x \sim z$$

其中：$$x \sim y$$表示$$(x,y)\in R\subset S\times S$$。例如，整数相等$$=$$是一个等价关系，自然数同余$$\equiv$$也是等价关系，但整数比较$$<$$或者集合包含$$\subset$$不是等价关系。

对于集合$$S$$中的每个元素$$x$$，称所有与$$x$$等价的元素构成的集合为$$x$$的等价类，记作$$[x]$$。$$S$$中所有的等价类构成的集合称为商集，记作$$S \setminus \sim = \{ [x] \vert x\in S\}$$。集合上的等价关系唯一确定一个商集。

## 定义

比例数，顾名思义，是由两个数的比构成的数。具体来说，任取两个整数$$p,q\in\mathbb Z$$满足$$q\neq0$$，则有序数对$$(p,q)$$ 为一比例数，也记作$$p:q$$ 或$$\frac pq$$。一个比例数有无穷多种表示，我们认为两个比例数$$\frac pq,\frac rs$$ 相等，当且仅当$$ps=qr$$，这是一个等价关系$$\sim$$。所有这样的有序数对构成的集合称作比例数域$$\mathbb Q$$，即$$\mathbb Q:=\mathbb Z \times \mathbb Z^+ \setminus \sim$$。

**注意** _比例数域中的每一个元素是一个等价类。例如：如果_$$[r]\in\mathbb Q$$，则对任意非零整数_$$s$$_，有_$$\frac{rs}s\in[r]$$_。

**注意** _比例数域中的元素与它的代表元无关。例如：_$$\frac{rs}s=\frac{rt}t$$_表示同一个元素_$$[r]$$_。 _

## 算数运算

对于任意两个比例数$$\frac pq,\frac rs$$，我们可以定义加减法$$\pm$$、乘法$$\times$$和除法$$\div$$：

* $$\frac pq\pm\frac rs := \frac{ps \pm qr}{qs}$$
* $$\frac pq\times \frac rs := \frac{pr}{qs}$$
* $$\frac pq \div \frac rs := \frac pq \times \frac sr$$ (若$$r\neq0$$)

需要证明以上定义是良好的，即运算结果与代表元无关。我们只对加法进行证明，其余留给读者。

证明：令$$\frac{p_1}{q_1} \sim \frac{p_2}{q_2}, \frac{r_1}{s_1} \sim \frac{r_2
}{s_2}$$，则根据定义，有$$p_1q_2=p_2q_1, r_1s_2=r_2s_1$$，那么，
$$\frac{p_1}{q_1}+\frac{r_1}{s_1}=\frac{p_1s_1+q_1r_1}{q_1s_1}=\frac{p_1q_2s_1s_2+q_1q_2r_1s_2}{(q_1s_1)(q_2s_2)}=\frac{p_2q_1s_1s_2+q_1q_2r_2s_1}{(q_1s_1)(q_2s_2)}=\frac{p_2s_2+q_2r_2}{q_2s_2}=\frac{p_2}{q_2}+\frac{r_2}{s_2}$$

比例数的运算满足以下性质：

* 加法交换律、乘法交换律：$$x+y=y+x, xy=yx$$
* 加法结合律、乘法结合律: $$(x+y)+z=x+(y+z), (xy)z=x(yz)$$
* 乘法对加法的分配律：$$x(y+z)=xy+xz$$

## 序

为了比较大小，比例数还可以定义序。对于任意两个比例数$$\frac pq,\frac rs(q,s>0)$$，定义$$\frac pq < \frac rs$$当且仅当$$ps < qr$$。读者可以证明该定义也是良好的。

我们说比例数具有全序性，因为任意两个比例数都可以作比较，或者说比例数可以被分布在一根数轴上。

比例数还具有稠密性，任意接近的两个比例数$$\frac pq,\frac rs$$中，存在任意多个比例数$$t$$满足$$\frac pq\leq t\leq\frac rs$$，例如$$t=\frac pq \oplus \frac rs：=\frac{p+r}{q+s}$$。