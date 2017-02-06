# 复数

## 复数的构造

考虑方程$$x^2=-1$$，该方程在实数域上没有解，并且无法用任何实数逼近，我们不得不采用新的方法构造出使该方程有解的数。假设这个构造出的新数$$i$$满足方程$$i^2=-1$$，称$$i$$为**虚数单位**。我们希望探索$$i$$具有什么性质。

纯形式地，我们构造关于$$i$$的多项式$$P(i)=\sum_{k=0}^\infty a_ki^k:=a_0+a_1i+a_2i^2+\cdots,(a_i\in\mathbb R)$$，这个多项式中包含了实数与虚数单位的加法和乘法运算。根据$$i^2=-1$$，不难得出:$$i^{4k}=1,i^{4k+1}=i,i^{4k+2}=-1,i^{4k+3}=\frac1i=-i, (k\in\mathbb N)$$。因此$$P(i)$$可以化简成$$z=a+bi$$的形式，我们称这种形式的数为**复数**，记作$$\mathbb C$$，其中，$$a=:\Re z$$称作**实部**，$$b=:\Im z$$称作**虚部**。如果记关于$$i$$的所有多项式构成的集合为$$\mathbb R[i]$$，以$$i^2=-1$$为等价关系$$\sim$$，则复数域还可记为$$\mathbb C:=\mathbb R[i]\setminus\sim=\mathbb R[i]\setminus(i^2+1)$$。

**注意** _我们采用的复数的构造方法与比例数和实数的构造方法不同，复数的构造引入了一个假想的、虚拟的数，而比例数和实数的构造是通过已有的数实现。_

## 算数运算

假设有复数$$a+bi,c+di$$，并且仍然假设具有交换律、结合律和分配律，则自然有四则运算：

* $$(a+bi) \pm (c+di) = (a+c)+(b+d)i$$
* $$(a+bi)(c+di) = ac+adi+bci+bdi^2 = (ac-bd)+(ad+bc)i$$
* $$\displaystyle{\frac{a+bi}{c+di}=\frac{(a+bi)(c-di)}{(c+di)(c-di)}=\frac{ac+bd}{c^2+d^2}+\frac{bc-ad}{c^2+d^2}i}$$

除了以上操作，复数还有一个常用的运算，叫做共轭：

* $$\overline{a \pm bi}=a \mp bi$$

根据复数的运算法则，与比例数相似，复数还可以定义为满足这些运算法则的有序实数对$$(a,b):=a+bi$$，即$$\mathbb C=\mathbb R^2$$。这是复数的另一构造方法。

## 复数的几何意义

### 复数的三角形式

因为复数可以表示为有序实数对，可以认为复数是平面上一点。因此还可以定义与$$0$$的长度和角度，分别称为**模长**$$|z|=\sqrt{a^2+b^2}=\sqrt{z \bar z}$$和**幅角**$$\arg z=\arctan \frac ba +k\pi~(\arg z \in (-\pi,\pi])$$。写成三角形式：$$z=r(\cos\varphi+i\sin\varphi)=:r\mathop{cis}\varphi$$。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/Complex_number_illustration_modarg.svg/440px-Complex_number_illustration_modarg.svg.png)

假设复数$$z=a+bi=(a,b)=r\mathop{cis}\varphi,w=c+di=(c,d)=s\mathop{cis}\theta$$，根据四则运算

* $$z \pm w=(a,b)\pm(c,d)=(a\pm c,b\pm d)=w \pm z$$

复数的加减法几何上就是向量的加减法；

* $$zw=r\mathop{cis}\varphi\cdot s\mathop{cis}\theta=rs(\cos\varphi+i\sin\varphi)(\cos\theta+i\sin\theta)$$$$=rs((\cos\varphi\cos\theta-\sin\varphi\sin\theta)+i(\cos\varphi\sin\theta+\sin\varphi\cos\theta))$$$$=rs(\cos(\varphi+\theta)+i\sin(\varphi+\theta))=rs\mathop{cis}(\varphi+\theta)$$
* $$z/w=\frac rs\mathop{cis}(\varphi-\theta)$$

复数的乘除法长度上是长度相乘除，角度上是角度相加减。因此，通过复数除法，我们可以计算两个向量的；

* $$\bar z=\overline{(a,\pm b)}=(a,\mp b)$$

复数的共轭运算是关于实轴的反射。

### 复数的指数形式

注意到复数的乘法，从幅角上看，相当于幅角的加法，这与指数函数类似。实际上，$$\mathop{cis}\varphi=e^{i\varphi}$$，这是著名的**欧拉公式**。注意指数上是虚数，否则将与长度乘法不兼容。特别地，令$$\varphi=\pi/2$$，我们有$$e^{i\pi/2}=i$$，因此虚单位$$i$$还可以看作是逆时针旋转$$\pi/2$$；如果令$$\varphi=\pi$$，我们还有$$e^{i\pi}=\mathop{cis}\pi=\cos\pi=-1$$，或者$$e^{i\pi}+1=0$$。

我们做如下计算：$$\mathop{cis}n\theta=e^{in\theta}=(e^{i\theta})^n=(\mathop{cis}\theta)^n$$，这是著名的**棣莫弗公式**。棣莫弗公式让我们可以很容易的计算正余弦函数的倍角公式。例如$$\mathop{cis}2\theta=(\mathop{cis}\theta)^2=\cos^2\theta-\sin^2\theta+2i\cos\theta\sin\theta$$，故$$\cos2\theta=\Re\mathop{cis}2\theta=\cos^2\theta-\sin^2\theta,\sin2\theta=\Im\mathop{cis}2\theta=2\cos\theta\sin\theta$$。

复数的出现不仅解决了形如$$x^2=-1$$的方程无实数解的问题，也启发了我们数不一定是一个量，还可以是一种操作（例如旋转），数可以是多个量的结合体（例如长度和角度）。