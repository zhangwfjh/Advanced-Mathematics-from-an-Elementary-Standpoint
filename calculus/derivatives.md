# 导数

## 定义

实数域$$\mathbb R$$上的一个有序对$$(a,b)$$称为一个**有向区间**（不要求有$$a \lt b$$）。对子集$$X \subseteq \mathbb R$$上任意一点$$x\in X$$，称有向区间集合$$T_xX:=\{(x,x') \vert x' \in \mathbb R\}$$为$$X$$在点$$x$$处的**切集**，$$TX:=\bigcup_{x \in X}T_xX$$为$$X$$的切集。定义$$(a,b)$$的**有向长度**$$\overline{ab}:=b-a$$，因为任意$$(x,x') \in T_xX$$，存在唯一实数$$v_x = \overline{xx'}$$，反之亦然，故也有$$T_xX=\{v_x|v_x \in \mathbb R\}$$。

考虑线性函数$$l:X\to Y$$满足$$x\mapsto kx$$。函数$$l$$是子集$$X$$到$$Y$$的均匀伸缩。可以计算$$l$$在$$x \in X$$处的伸缩比$$l'(x)=\dfrac{\overline{l(x)l(x')}}{\overline{xx'}}=\dfrac{kx'-kx}{x'-x}=k$$。显然，$$x$$处的伸缩比$$l'(x)$$应该与$$x'$$的选择无关。

![](/assets/derivatives1.png)

自然地，函数$$l$$导出切集上的函数$$l_*:TX \to TY$$满足$$(x,x')\mapsto (kx,kx')$$以及$$l_{x*}:T_xX\to T_{l(x)}Y$$满足$$v_x\mapsto v_{l(x)}:=kv_x$$。因此，$$x$$处的伸缩比还可定义为$$l'(x):=\dfrac{v_{l(x)}}{v_x}=\dfrac{kv_x}{v_x}=k$$，或者$$l'(x)=l_{x*}$$。

对于一般的实函数$$f:X\to Y$$，也可以看做是子集$$X$$到$$Y$$的伸缩，只不过不是均匀的。因此在计算点$$x$$处的伸缩比$$f'(x)$$时，需要选取