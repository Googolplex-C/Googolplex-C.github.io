---
title: 抽象代数 笔记 Ch01 Section03
date: 2019-02-23 14:57:10
author: Googolplex-C
img: 
top: 
cover: 
coverImg: 
password: 
toc: 
mathjax: 
summary: 
categories: 
tags:

export_on_save:
  html: true
html:
  embed_local_images: false
  embed_svg: true
  offline: false
  toc: true
---

接上一篇笔记 [抽象代数 笔记 Ch01 Section02 P2](../AbstractAlgebra-Note-Ch01-Section02-P2/AbstractAlgebra-Note-Ch01-Section02-P2.html)

<!-- more -->

### Chapter 1 群（续）

#### Section 3 子群与商群

邓老师：抽代课程的一个基本套路是，讲完一个代数体系的定义和性质之后，一般就开始讲子体系和商体系；原因有几点：

1. 就是要有足够多的例子，如果没有什么例子，学抽代很难展开；
2. 通过子体系和商体系来研究代数体系本身；

##### 定义 1.3.1 

设 $G$ 是群，$H \subseteq G$ 是**非空**子集，若 $H$ 在 $G$ 的运算下构成群，则称 $H$ 是 $G$ 的子群，记作 $H <G$ 

##### 例 1

考虑数域 $\mathbb{P}_1 \subseteq \mathbb{P}_2$ ，则 $\{\mathbb{P}_1,+\} < \{\mathbb{P}_1,+\}$；

另有，正实数集合是不包含 $0$ 的实数集合的子群，即：$\{\mathbb{R}^+, \cdot\} < \{\mathbb{R}^*, \cdot\}$

以及，$\{\{-1,1\},\cdot\} < \{\mathbb{R}^*,\cdot\}$

此外，我们断言：$\{\mathbb{R}^*,+\}$ 不是 $\{\mathbb{R}, \cdot\}$ 的子群，因为它们的运算不一样

##### 例 2

设 $\mathbb{V}$ 是线性空间，$\mathrm{dim} \mathbb{V} < \infty$，$S_{\mathbb{V}}$ 是 $\mathbb{V}$ 的全变换群，设 $\mathrm{GL}(\mathbb{V})$ 为所有可逆的线性变换组成的集合，有 $\mathrm{GL}(\mathbb{V}) < S_{\mathbb{V}}$ ，称其为 $\mathbb{V}$ 上的一般线性群；

记 $\mathrm{SL}(\mathbb{V})$ 为 $\mathbb{V}$ 中行列式为 $1$ 的线性变换的集合，则有 $\mathrm{SL}(\mathbb{V}) < \mathrm{GL}(\mathbb{V})$ ，称之为特殊线性群

假设 $\mathbb{V}/\mathbb{P}$ ，即线性空间是在数域上的，则 $\mathrm{GL}(n,\mathbb{P})$ 为所有可逆的 $n$ 阶矩阵组成的集合，也称为一般线性群；

同理 $\mathrm{SL}(n,\mathbb{P})$ 为 $\mathbb{V}$ 中行列式为 $1$ 的 $n$ 阶方阵的集合，也称为特殊线性群；

事实上，这两种版本的线性群是同构的；

##### 例 3

令 $m\mathbb{Z}=\{mn \mid  n \in \mathbb{Z}\}$，其中 $m \in \mathbb{N}$，于是 $m\mathbb{Z} < \mathbb{Z}$ （运算为加法）



$H$ 与 $G$ 的运算一致，可以推出：$G$ 的幺元 $e \in H$；

对于任意的 $h \in H$，其逆元 $h^{-1} \in H$

##### 定理 1.3.1 

设 $G$ 是群，$H \subseteq G$ 是非空子集，则以下三个命题等价：

1. $H <G$
2. $\forall a,b \in H,ab \in H, a^{-1}\in H$
3. $\forall a,b \in  H, ab^{-1} \in H$

*Proof*

由 1 推出 2，显然

由 2 推出 3，显然

由 3 推出 1：此时我们需要根据群的四条公理来证明：

$\forall a, b \in H,ab^{-1} \in H$，从而 $aa^{-1} \in H$ 即 $e \in H$，于是我们证明了幺元属于 $H$

把幺元 $e$ 代入 $a$，于是 $b^{-1} =eb^{-1} \in H$，于是我们证明了任意元素的逆元存在；

继续把 $b^{-1}$ 代入 $b$ 我们可以看到，$a(b^{-1})^{-1}=ab \in H$，从而我们证明了封闭性；

由于 $H$ 是 $G$ 的子集，而 $G$ 上的运算满足结合律，并且我们已经证明了封闭性，所以 $H$ 上结合律是自然成立的；

从而 $H$ 是子群

<p align="right">Q.E.D.</p>

##### 命题 1.3.2 

设 $H$ 是群 $G$ 的**有限**非空子集，则我们有：

$H <G$，当且仅当 $H$ 对运算封闭

*Proof*

必要性显然；

我们来证明充分性.

因为 $H$ 对运算封闭，且以 $G$ 的角度而言，结合律在 $G$ 上成立，从而结合律在 $H$ 上成立，从而 $H$ 是一个有限半群；

另外，因为 $H$ 是群 $G$ 的**有限**非空子集，从而消去律是自然成立的，从而由 命题 1.2.6 可知，$H$ 是群；

<p align="right">Q.E.D.</p>

注解：这个命题是上一个命题中的 2 的一个变形，原来的 “非空子集” 加强为 “有限非空子集”，而 $a^{-1} \in H$ 被弱化了；

##### 命题 1.3.3 子群的性质

若 $H_1 < G$ , $H_2 <G$，则 $H_1 \cap H_2 <G$

*Proof*

首先可见 $e \in H_1 \cap H_2$，所以 $H_1 \cap H_2$ 不是空集；

对于一切的 $a,b \in H_1 \cap H_2$，则 $a,b \in H_1$ 且 $a,b \in H_2$，由命题 1.3.2 可知

故 $ab^{-1} \in H_1$，且 $ab^{-1} \in H_2$，故 $ab^{-1} \in H_1 \cap H_2$，故 $H_1 \cap H_2 < G$

<p align="right">Q.E.D.</p>

思考题：

如果是 $H_1 \cup H_2$ 呢，它何时是 $G$ 的子群？



##### 定义 1.3.2 陪集

设 $G$ 是群，$H <G$，$a \in G$，定义 $aH=\{ah \mid h \in H\}$，以及 $Ha =\{ha \mid h \in H\}$ 分别是 $a$ 为代表元的 $H$ 的一个左陪集，以及 $a$ 为代表元的 $H$ 的一个右陪集

##### 定理 1.3.4

设 $G$ 是群，$H <G$，定义关系 $R$ 如下：$a\, R\, b \Leftrightarrow a^{-1}b \in H$，那么关系 $R$ 是等价关系. $a$ 所在的等价类 $\overline{a}=aH$，故 $a$ 的所有左陪集构成 $G$ 的一个分类.

*Proof*

$R$ 是关系：这是显然的，因为 $a^{-1}b$ 要么属于 $H$，要么不属于 $H$

$R$ 是等价关系，下面进行验证：

1. 自反性：$\forall a \notin G, a^{-1}a  = e\in H$，因为子群中必有幺元；
2. 对称性：若 $a\,R\,b$，即 $a^{-1}b \in H$，则 $(a^{-1}b)^{-1}=b^{-1}(a^{-1})^{-1}=b^{-1}a \in H$，从而 $b\,R\,a$
3. 传递性：若 $a\,R\,b$, $b\,R\,c$，则 $a^{-1}b \in H$, $b^{-1}c \in H$，因为 $H<G$，于是 $(a^{-1}b)(b^{-1}c) \in H$，于是 $a\,R\,c$

因此 $R$ 是等价关系

我们再来证明 $\overline{a}=aH$：

一方面，对于任何$h \in H$，我们有 $a^{-1}(ah)\in H$，因此 $a\,R\,ah$，即 $ah \in \overline{a}$，从而 $aH \subseteq \overline{a}$

另一方面，对于一切 $b \in \overline{a}$，$a\,R\,b$，即$a^{-1}b \in H$，故 $b=a(a^{-1}b) \in aH$，故而 $\overline{a} \subseteq aH$

<p align="right">Q.E.D.</p>

由定理 1.3.4 可知，$\{aH\}$ 构成 $G$ 的分类，记作商集合 $G/R$ 或者 $G/H$，称为 $G$ 对子群 $H$ 的左商集，或者左陪集空间。

同理可类似地定义右陪集空间

##### 推论 1.3.5 
对于 $a,b \in G$, $aH=bH$ 当且仅当 $a^{-1}b \in H$

##### 定义 1.3.3 指数
设 $H<G$，则左商集的势 $\left|G/H \right|$ 称为 $H$ 在 $G$ 中的指数，记作 $[G:H]$

##### 注解
定义 1.3.2 至此的记号一般是针对乘法群的，在加法群中，左陪集记为 $a+H$，关系 $R$ 的定义写作：$aRb$ 当且仅当 $b-a \in H$

##### 例4
$[\mathbb{Z}:m\mathbb{Z}]=m$，其中 $m \in \mathbb{N}$；  
另有对于一切 $a \in \mathbb{Z}$，$a+m\mathbb{Z}=\{a+nm \mid n \in \mathbb{Z}\}$

##### 定理 1.3.6 Lagrange定理
设 $G$ 为有限群，且 $H<G$，则 $|G|= [G:H]\times |H|$

*Proof*

对于一切 $a \in G$，$H \rightarrow aH$ 这个映射是单射，另由消去律可知，这个映射是满射，从而 $|H|=|aH|$，设 $G$ 是 $[G:H]$ 个陪集的并，这些陪集并不相交，所以 $|G|=[G:H]\times |H|$

<p align="right">Q.E.D.</p>

##### 推论 1.3.7
设 $G$ 是有限群，$H<G$，$K<G$，且 $H \subseteq K$ （从而 $H < K$），则 $[G:H]=[G:K]\times[K:H]$

*Proof*

由于 $K<G$ 以及 $H <K$，由 Lagrange 定理可知 $|G|=[G:K]\times |K| = [G:K]\times[K:H] \times |H|$

同时因为 $H$ 是 $K$ 的子群，后者又同时是 $G$ 的子群，所以 $H$ 是 $G$ 的子群，由 Lagrange 定理可知 $|G| = [G:H] \times |H|$
。

于是消去 $|H|$ 可以得到，$[G:H]=[G:K]\times[K:H]$

<p align="right">Q.E.D.</p>

设 $H<G$，并有商集 $G/R$ 或者记作 $G/H$，如果我们要把商集加强为商集的话，我们还缺什么？没错，运算！
这就要求运算 $R$ 是同余关系。

我们继续引出下面的概念
##### 定义 1.3.4
设 $G$ 为群，$H<G$，称 $H$ 为 $G$ 的正规子群，若对于一切 $g \in G$，以及一切 $h \in H$，有 $ghg^{-1} \in H$，记为 $H \lhd G$

##### 例5
平凡子群必为正规子群；
所谓平凡子群，就是指 $\{e\}$ 以及 $G$ 自身

##### 例6
若 $G$ 为 Abel 群，则任何一个子群都是正规子群

##### 例7
$\mathrm{SL}(\mathbb{V}) \lhd \mathrm{GL}(\mathbb{V})$

证明也很简单，只需注意到 $|ABA^{-1}|=|A||B||A^{-1}|=|A||A^{-1}||B|=|B|$

##### 定理 1.3.8 判定正规子群的方法

设 $H <G$，则下列条件等价

1. $H \lhd G$
2. $\forall g \in G, gH=Hg$
3. $\forall g_1,g_2 \in G,g_1H\cdot g_2H=g_1g_2H$，其中点表示笛卡尔积：$g_1H\cdot g_2H=\{g_1h_1g_2h_2 \mid h_1,h_2 \in H\}$

*Proof*

由命题1 证明 命题2：

对于任何的 $g \in G$, $h \in H$, $ghg^{-1} \in H$，记 $ghg^{-1}$ 为 $h_1$，即 $gh= h_1g \in Hg$，故 $Hg \subseteq gH$。同理也可证 $gH \subseteq Hg$

由命题2 证 命题3：

$\forall h_1, h_2 \in H, h_1g_2 \in Hg_2 = g_2H$，存在 $h_1' \in H$，使得 $h_1g_2=g_2h_1'$，故 $g_1h_1g_2h_2=g_1g_2h_1'h_2 \in g_1g_2H$，故 $g_1Hg_2H \subset g_1g_2H$

又对于任意的 $h \in H$, $g_1g_2h= g_1eg_2h \in g_1Hg_2H$，固有 $g_1g_2H \subseteq g_1Hg_2H$

由命题3 证 命题1：
已知 $H<G$，$\forall g \in G, h \in H, ghg^{-1}=ghg^{-1}e \in gH\cdot g^{-1}H$，由命题 3 可知，$gH\cdot g^{-1}H= gg^{-1}H=H$，故 $H \lhd G$

<p align="right">Q.E.D.</p>

邓老师语录：证明正规子群最多还是使用定义本身

##### 定理 1.3.9
设 $H<G$，则等价关系 $R: a\,R\,b \Leftrightarrow a^{-1}b \in H$ 是 $G$ 的同余关系，当且仅当 $H \lhd G$，这时候，$G/H$ 对于诱导的运算构成一个群，称为 $G$ 对于 $H$ 的商群，极为 $G/H$

*Proof*

若 $H \lhd G$，则对于任意的 $a_1, a_2,b_1,b_2 \in G$，且满足 $a_1\,R\,b_1, a_2\,R\,b_2$，即 $a_1^{-1}b^{-1} \in H$，有 $(a_1a_2)^{-1}b_1b_2=a_2^{-1}a_1^{-1}b_1b_2=a_2^{-1}(a_1^{-1}b_1)a_2(a_2^{-1}b_2)$

注意到 $H \lhd G$，且 $a_1^{-1}b_1$ 和 $a_2^{-1}b_2$ 属于 $H$，所以 $a_2^{-1}(a_1^{-1}b_1)a_2 \in H$，故 $(a_1a_2)^{-1}b_1b_2 \in H$，故 $R$ 为同余关系

反之，若 $R$ 为同余关系，则 $\forall g \in G,\forall h \in H$，我们注意到 $g^{-1}gh=h \in H$, 因此 $g R gh$，并有 $g R g^{-1}$，故 $e^{-1}(ghg^{-1})\in H$ 即 $ghg^{-1} \in H$，从而 $H$ 是正规子群。

接下来我们可以进一步说明 $G/H$ 是商群：

设 $H \lhd G$，因为 $R$ 为同余关系，即 $G/R=G/H$ 有诱导运算，定义为 $g_1H \cdot g_2H=g_1g_2H$。
我们来逐一验证群的公理：

1. 结合律：
  $$
  (g_1H\cdot g_2H)\cdot g_3H=(g_1g_2H)\cdot g_3H= g_1g_2g_3H
  $$
  另一方面，我们有
  $$
  g_1H\cdot (g_2H\cdot g_3H)=g_1H\cdot (g_2g_3H)= g_1g_2g_3H
  $$
于是，结合律成立

2. 幺元
  我们知道，对于所有的 $g \in G$，$eH\cdot gH= e\cdot gH= gH$，因此左幺元为 $eH$，右幺元同理可证

3. 逆元
  对于一切的 $g \in G$，$g^{-1}HgH=g^{-1}gH=eH$，因此 $gH$ 的左逆为 $g^{-1}H$，右逆同理可证

因此我们可以得知，$G/H$ 是商群。

<p align="right">Q.E.D.</p>

##### 例8
对于任何的群，$\{e\}$ 和其自身是他自己的正规子群，$G/\{e\}=G$，基数为 $|G|$；$G/G=\{G\}$，基数为 $1$

##### 例9
$\{\mathbb{Z},+\}$ 为 Abel 群， 其中 $m \in \mathbb{N}$，且有 $m\mathbb{Z} \lhd \mathbb{Z}$，$\mathbb{Z}/m\mathbb{Z}=\{\overline{0},\overline{2},\dots,\overline{m-1},\}$ 为商群，记为 $\mathbb{Z}/m\mathbb{Z}$，称为模 $m$ 的剩余类加群；

其运算定义为
$$
\overline{r_1}+\overline{r_2}=\overline{(r_1+r_2)\ mod\ m}
$$










