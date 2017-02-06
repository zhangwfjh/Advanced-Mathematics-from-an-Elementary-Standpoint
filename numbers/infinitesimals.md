# 无穷小量

## 对偶数

考虑在实数域$$\mathbb R$$中加入一个正无穷小量$$\epsilon$$，满足$$\epsilon > 0 \wedge \epsilon^2 = 0$$。尽管在实数范围内，该方程有唯一解$$0$$，但并不妨碍新加入的**无穷小量**$$\epsilon\neq0$$。无穷小量还有以下性质：

* 正无穷小量小于任意正实数，负无穷小量大于任意负实数

**证明**：$$\displaystyle{forall r > 0: r-\epsilon=\frac{r^2-\epsilon^2}{r+\epsilon}=\frac{r^2}{r+\epsilon} > 0}$$

* 无穷小量的任意倍数仍然是无穷小，也就有，有限个无穷小量的和仍然是无穷小

**证明**：否则，存在倍数$$n$$和实数$$r$$，使得$$n\epsilon > r$$，即$$\epsilon > \frac rn$$，与$$\epsilon$$是无穷小矛盾。

* 正无穷小量的倒数大于任意实数，即正无穷大

**证明**：$$\displaystyle{forall r > 0: \frac1r > \varepsilon > 0}$$，因此$$\displaystyle{r < \frac1\epsilon}$$

类比复数的构造方法，可以构造对偶数域$$\mathbb R^\epsilon:=\mathbb R[\epsilon] \setminus (\epsilon^2)$$，所有的对偶数可以表示为$$a+b\epsilon$$。类似构造四则运算：

* $$(a+b\epsilon) \pm (c+d\epsilon)=(a \pm c)+(b \pm d)\epsilon$$
* $$(a+b\epsilon)(c+d\epsilon)=ac+(ad+bc)\epsilon$$
* $$\displaystyle{\frac{a+b\epsilon}{c+d\epsilon} = \frac{(a+b\epsilon)(c-d\epsilon)}{(c+d\epsilon})(c-d\epsilon)} = \frac{ac+(bc-ad)\epsilon-bd\epsilon^2}{c^2-\epsilon^2} = \frac ac - \frac{bc-ad}{c^2}\epsilon}$$

## 超实数

另外一种构造无穷小量的方法与构造实数的方法类似，通过柯西列来定义。考虑实数构成的柯西列$$\{a_n\}_0^\infty$$，如果实数数列的每一项都有$$a_n=r$$，则该柯西列定义为超实数$$r$$；如果$$\lim_{n\to\infty}a_n=0$$，则称该柯西列为超实数中的**无穷小量**。因此，任何一个超实数可以表示为一个实数和一个无穷小量的和，$${}^*r=r+\epsilon$$。记所有实数构成的柯西列为$$\mathscr C(\mathbb R)$$，两个柯西列等价$${a_n\}_0^\infty \sim {b_n\}_0^\infty$$当且仅当$${|a_n-b_n|\}_0^\infty$$是无穷小量，则超实数可写为$${}^*\mathbb R:=\mathscr C(\mathbb R)\setminus\sim$$。
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Standard_part_function_with_two_continua.svg/720px-Standard_part_function_with_two_continua.svg.png)

超实数中的无穷小量仍然具有以下性质，证明留给读者：

* 无穷小量小于任意正实数，大于任意负实数
* 无穷小量的任意倍数仍然是无穷小，也就有，有限个无穷小量的和仍然是无穷小
* 正无穷小量的倒数大于任意实数，即正无穷大

超实数有一个重要的运算，称为**标准部**，记作$$\mathop{sd}({}^*r):=\lim_{n\to\infty}a_n$$，定义为柯西列的极限。