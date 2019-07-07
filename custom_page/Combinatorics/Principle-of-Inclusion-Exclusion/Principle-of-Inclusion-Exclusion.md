---
title: 容斥原理
date: 2019-07-05 16 59 42
author: Googolplex-C
url: 
img: 
top: 
cover: 
coverImg: 
password: 
toc: 
mathjax: 
summary: <!--TODO-->
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

本文的主要内容并不完全是笔者的原创，除了笔者自己的笔记和注解之外，还有部分内容是 Richard P. Stanley 所写的那本经典书籍的翻译。这本关于组合数学的经典著作写得非常好，没有必要事事都另起炉灶。

### 前言

#### 筛法

在组合数学以及数论里面，筛法是非常重要且强大的一种数学方法。

粗略地说，筛法的**主要思路**就是：我们需要某一个集合 $S$ 的基数，但我们不直接去计算它的基数；而是先考虑一个更大的集合，计算这个集合的基数，然后删减掉某一些元素，从而通过这两部分的基数之差间接算出我们的目标集合 $S$ 的基数。

#### 筛法的变种形式

1. 先考虑一个目标基数的上界，然后减去多出来的部分，再补上可能存在 “减过头” 的部分……如此重复，直至最终得到的结果 “收敛” 至一个确定的数值——**这其实就是容斥原理的实质**

2. 更大的这个集合的元素可以通过某种自然的组合方式进行加权，使得那些不需要被计数的元素被消去。[^1]

### 容斥原理 (Principle of Inclusion-Exclusion)

#### Introduction

容斥原理，英文称 Principle of Inclusion-Exclusion / Inclusion-Exclusion Principle，简称 PIE，是计数组合学中一个非常基础的工具。

从宏观角度来看，这个定理的本质无非就是**计算一个特定矩阵的逆**，因此它本身就是线性代数中的一个次级结论。

这个定理的美妙之处不在于其命题本身，而在于它有许多意想不到的应用[^2]

#### PIE 的具体表述
##### PIE 一般形式

定理 1（PIE 一般形式）
:    设 $S$ 是一个 $n$ 元集合。令 $V$ 是一个定义在数域 $K$ 上的，维数为 $2_{}^{n}$ 的线性空间，该线性空间由所有从 $S$ 的幂集 $2_{}^{S}$ 到数域 $K$ 的映射构成。定义从 $V$ 到 $V$ 的映射如下：

:   $$
    \phi\ f(T)=\sum_{Y \supseteq T} f(Y) \qquad \text{for all }\ T \subseteq S
    \label{1}
    \tag{1.1}
    $$

:    那么，逆映射 $\phi^{-1}$ 存在，且其形式如下：
    $$
    \phi^{-1}f(T)= \sum_{Y \supseteq T} (-1)^{\lvert Y-T \rvert}f(Y) \qquad \text{for all }\ T \subseteq S
    \label{2}
    \tag{1.2}
    $$

###### 笔者注解
1. 线性空间的元素是什么？

    **Answer**: 线性空间 $V$ 的元素就是所有任意的函数 $f:2^{S} \rightarrow K$. 请注意，这里的意思是，一个函数**作为整体**看作一个元素，也即线性空间 $V$ 中的一个向量；
    
2. 这个线性空间 $V$ 的两种运算如何定义？

    **Answer**: 其实就是最常见的函数的加法和函数数乘。
    
    函数加法：假设有 $f, g \in V$，则定义 $f+g$ 为：
    
    $$
    (f+g)(A)=f(A)+g(A) \in K \qquad \text{for all }\ A \in 2^S
    $$

    于是 $f+g$ 也是从 $2^S$ 到 $K$ 的映射，从而 $f+g \in V$，函数加法是良定义的。

    函数数乘：假设有 $f \in V$， $c \in K$, 则定义 $cf$ 为：

    $$
    (cf)(A)=c \cdot f(A) \in K \qquad \text{for all }\ A \in 2^{S}
    $$
    显然函数数乘也是定义成功的。

3. 为什么说 $V$ 是 $2^n$ 维的线性空间？

    **Answer**: 笔者在刚开始看这里的时候也是非常纳闷，只知道这个 $2_{}^{n}$ 肯定和 $S$ 的幂集有关系，但不知道为什么维数和幂集的基数就扯上了关系。

    其实这正好说明笔者当时还没有完全习惯和接受前两个问题中提到的事实：每一个形如 $f:2_{}^{S}\rightarrow K$ 的函数都是作为**一个整体**而视作空间 $V$ 的元素。

    另外，函数的加法只将 $f$ 的定义域中相同的元素的函数值进行**对应相加**，也就是说，$f$ 在 $A$ 处的映射值 $f(A)$ 只可能与另一个映射 $g$ 在 $A$ 处的映射值相加，断然不会与 $g$ 在 $B \in 2_{}^{S}(B \neq A)$ 处的映射值 $g(B)$ 发生任何加减乘除的关系。

    数乘运算同理。

    于是 $f$ 在 $A$ 处的值与其在 $B$ 处的值这两者在线性空间中定义的两种运算下保持着独立——这不正相当于向量的分量嘛！ 
    
    事实上，我们不妨将其归结成一个引理：

    引理1
    :    考虑由一切函数 $f:X \rightarrow K$ 构成的线性（函数）空间 $V$ ，其中 $X$ 是有限集，$K$ 是数域，那么 $V$ 的维数等于 $\lvert X \rvert$.

    引理1 证明
    :    设 $X=\{e_{1}^{}, e_{2}^{},\dots, e_{n}^{}\}$, 构造 $n$ 个函数 $f_{1}^{}$, $f_{2}^{}$, $\dots$, $f_{n}^{}$，使得：

    $$
    f_{i}^{}(e_{j}^{})=\begin{cases}
    1 \qquad i=j\\ 
    0 \qquad i \neq j
    \end{cases}
    \qquad \text{where }\ i,j \in [n]
    $$
    
    显然这 $n$ 个函数线性独立；

    另一方面，考虑任意一个 $V$ 中的函数 $F:X \rightarrow K$ ，我们都有

    $$
    F=F(e_{1}^{})f_{1}^{}+F(e_{2}^{})f_{2}^{}+\cdots+F(e_{n}^{})f_{n}^{}
    $$
    
    于是 $f_{1}^{}$, $f_{2}^{}$, $\dots$, $f_{n}^{}$ 是 $V$ 的一组基。从而命题得证。

    <p align="right">Q.E.D.</p>
    
    事实上，我们完全可以把 $V$ 中的函数 $f$ 表示成

    $$
    \begin{bmatrix}
    f(A_1) \\
    f(A_2) \\
    \cdots \\
    f(A_{2^n}) \\
    \end{bmatrix}
    \qquad
    \text{where }\ A_{i}^{} \in 2_{}^{S}
    $$
    
    一目了然，直观易懂。

4. $\phi$ 真的是 $V$ 上的线性变换吗？

    **Answer**: 真的是，自己验证一下就可以了。

    $$
    \begin{aligned}
    \phi(f+g)(T)&=\sum_{Y \supseteq T}^{}(f+g)(Y) \\
    &= \sum_{Y \supseteq T}^{}(f(Y)+g(Y)) \\
    &=\sum_{Y \supseteq T}^{}f(Y) + \sum_{Y \supseteq T}^{}g(Y) \\
    &=\phi\ f(T)+\phi\ g(T)
    \end{aligned}   
    $$

    数乘部分的验证更加简单，略。
    
5. 既然 $\phi: V \rightarrow V$ 是一个从 $V$ 到 $V$ 的线性变换，那么 $\phi$ 应该接受一个函数作为自变量啊，这个所谓 $\eqref{1}$ 里面的 $\phi\ f(T)$ 又是怎么回事？

    **Answer**: 看书要看完整！别忘了后面还有一个 $\text{for all }\ T \subseteq S$ ,意思就是：作为映射 $\phi$ 的输出 $\phi\ f$ ，其分量 $\phi\ f(T)$ 由原来的向量 $f$ 中所有满足 $Y \supseteq T$ 的分量 $f(Y)$ 经线性组合而成.

    值得注意的是，式$\eqref{1}$ 不就是矩阵的另一种表达方式嘛！
    
##### PIE 证明
构造映射 $\psi: V \rightarrow V$ 如下：

$$
\psi f(T)=\sum_{Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert}f(Y) \qquad \text{for all } T \subseteq S
$$

将 [定理1] 命题中的映射 $\phi$ 与该映射复合：

$$
\begin{aligned}
\psi \phi\,f(T)&=\sum_{Y \supseteq T}^{}(-1)^{\lvert Y-T \rvert} \phi\,f(Y) \\
&=\sum_{Y \supseteq T}^{}(-1)^{\lvert Y-T \rvert}(\sum_{Z \supseteq Y}^{}f(Z)) \\
&\overset{*}{=} \sum_{Z \supseteq T}^{}(\sum_{Z \supseteq Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert})f(Z)
\end{aligned}
$$

不妨记 $\vert Z-T \rvert =m$, $\lvert Y-T \rvert=i$,  并固定集合 $Z, T$. 于是，$\sum_{Z \supseteq Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert} = \sum_{i=0}^{m}(-1)^i \binom{m}{i}=\delta_{0m}^{}$

而$\delta_{0m}^{}=1$ 当且仅当 $m=0$，若 $m \neq 0$, 则 $\delta_{0m}^{}=0$, 于是我们有

$$
\sum_{Z \supseteq T}^{}(\sum_{Z \supseteq Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert})f(Z)=f(T)
$$

从而说明，映射 $\psi=\phi_{}^{-1}$ , 命题得证。
<p align="right">Q.E.D.</p>

###### 笔者注解

以上是 Stanley 著作中的原始证明，笔者将其翻译至此。

在这个证明中，最容易让人摸不着头脑的地方在于等式(*) 处，笔者在此写一下注解。

$$
\sum_{Y \supseteq T}^{}(-1)^{\lvert Y-T \rvert}(\sum_{Z \supseteq Y}^{}f(Z))
$$

一式的含义是：

- 我们先固定集合 $T$, 然后遍历所有的满足 $Y \supseteq T$ 的集合 $Y$ 

    - 对于某个特定的 $Y$ （此时我们再固定集合 $Y$ ），我们继续考虑遍历所有满足 $Z \supseteq Y$ 的集合 $Z$ 

所以逻辑上来讲，这里实际上好比一个两层的嵌套循环，固定 $T$ ，遍历 $Y$ ；固定 $Y$ ，遍历 $Z$.

等式(*) 的推导思路本质上其实是**交换求和顺序**，当然从程序员的角度可以说是循环层级交换（其实叫什么名字都没什么区别啦，意会到即可）：

- 我们先固定集合 $T$，再考虑遍历所有满足满足 $Z \supseteq T$ 的集合 $Z$ （之所以可以这样做，是因为上式中的集合 $Z$ 其实就是遍历了所有包含集合 $T$ 的集合）：

    - 固定某个特定的集合 $Z$ ，考虑 $f(Z)$ 每次出现在上式中的系数，累加在一起就是 $\sum_{Z \supseteq Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert}$ 

于是后面的推导就很顺理成章了，等号(*) 的左式到右式体现了 “组合证明” 的内涵：对于同一个对象，通过两种不同的视角和方法对其计数。笔者认为此处是这个证明的点睛之处。

##### 另一种表述
定理 2（从一般到特殊：PIE的另一种表述）
:    设 $S$ 是一个集合，集合的元素是若干条 “性质”，另有一个给定的集合 $A$ ， $A$ 中的每一个元素可能满足 $S$ 中的部分或全部性质。此外我们设从 $A$ 到数域 $K$ 存在一个权重函数：$\omega:A \rightarrow K$。

:    对于 $S$ 的任意子集 $T$, 记函数 $f_{=}^{}(T)$ 是这样的一个函数：
    $$
    f_{=}^{}(T)=\sum \omega(x)
    $$

:    其中 $x$ 遍历 $A$ 中所有**恰好**具有集合 $T$ 中性质的元素，即 $x$ 具有所有 $T$ 中的性质，但是对于任何不在 $T$ 中的性质， $x$ 都不满足。

:    再记 $f_{\geq}^{}(T)$ 是一个这样的函数：
    $$
    f_{\geq}^{}(T)=\sum_{Y \supseteq T}f_{=}^{}(Y)
    $$

:    这个函数表示的含义其实就是 $A$ 中所有**至少**具有集合 $T$ 中性质的元素的权值之和。

:    根据[定理1]，如果我们已知每一个 $S$ 的子集在映射 $f_{\geq}^{}$ 下的值，那么我们有
    $$
    f_{=}^{}(T)=\sum_{Y \supseteq T}^{}(-1)_{}^{\lvert Y-T \rvert}f_{\geq}^{}(Y)
    $$
    
:    特别地，我们有
    $$
    f_{=}^{}(\varnothing)=\sum_{Y \subseteq S}^{}(-1)_{}^{\lvert Y \rvert}f_{\geq}^{}(Y)
    $$

###### 笔者注解

在繁复的推导中，可能容易迷失大方向。比如许多人可能会问的一个问题是：为什么要搞这么复杂，这个定理到底是要干什么的？

简单地说，定理2 想要求的东西就是某个 $T \subseteq S$ 在映射下 $f_{=}^{}$ 的像 $f_{=}^{}(T)$；之所以不直接暴力计数的原因在于，这个数值可能非常不好计算；但是相对而言，$f_{\geq}^{}(T)$ 更好计算。而容斥原理告诉我们，我们是有办法通过后者算出前者的，这就是它要干的事情。

##### 常见表述

定理 3
:    令 $A_1$, $A_2$, $\dots$, $A_n$ 是有限集 $A$ 的子集。对于 $[n]$ 的每个子集 $T$, 我们定义
    $$
    A_T=\bigcap_{i\in T}A_i 
    $$
:    注意当 $T=\varnothing$ 时，$A_T=A$；并对于一切 $0 \leq k \leq n$，令
    $$
    S_k=\sum_{\vert T \rvert =k}^{}\lvert A_T \rvert
    $$

:    不妨以这样的视角来看待 $A$ 的子集：$A_1$, $A_2$, $\dots$, $A_n$ 相当于定义了 $n$ 条性质，这 $n$ 条性质组成了**定理2**中的集合 $S$, 而本定理中的集合 $A$ 仍等同于定理2中的集合 $A$；从组合意义上说， $\lvert A_T \rvert$ 代表的是就是在集合 $A$ 中**至少**满足集合 $T$ 中指代的那些性质的元素的个数（相当于定理2中的 $f_{\geq}^{}(T)$）,而集合 $\overline{A_{1}^{}}\cap \overline{A_{2}^{}} \cap \cdots \overline{A_{n}^{}}$ 表示的即为所有不满足任何一条性质的元素的集合，相当于定理2中的 $f_{=}^{}(\varnothing)$. 根据定理2我们有
    $$
    \lvert \overline{A_1}\cap \overline{A_2} \cap \cdots \overline{A_n} \rvert = S_0 - S_1 + S_2 - \cdots + (-1)^n S_n
    $$
    
:    其中 $S_0=\lvert A_{\varnothing}\rvert = \lvert A \rvert$.

#### PIE 的对偶形式
##### 一般形式
定理 4（PIE 一般形式的对偶形式）
:    设 $S$ 是一个 $n$ 元集合。令 $V$ 是一个定义在数域 $K$ 上的，维数为 $2_{}^{n}$ 的线性空间，该线性空间由所有从 $S$ 的幂集 $2_{}^{S}$ 到数域 $K$ 的映射构成。定义从 $V$ 到 $V$ 的映射如下：

:   $$
    \widetilde{\phi}\ f(T)=\sum_{Y \subseteq T} f(Y) \qquad \text{for all }\ T \subseteq S
    $$

:    那么，逆映射 $\phi^{-1}$ 存在，且其形式如下：
    $$
    \widetilde{\phi^{-1}}f(T)= \sum_{Y \subseteq T} (-1)^{\lvert T-Y \rvert}f(Y) \qquad \text{for all }\ T \subseteq S
    $$

##### 对偶形式的证明
构造映射 $\widetilde{\psi}: V \rightarrow V$ 如下：

$$
\widetilde{\psi} f(T)=\sum_{Y \subseteq T}^{}(-1)_{}^{\lvert T-Y \rvert}f(Y) \qquad \text{for all } T \subseteq S
$$

将 [定理1] 命题中的映射 $\widetilde{\phi}$ 与该映射复合：

$$
\begin{aligned}
\widetilde{\psi} \widetilde{\phi}\,f(T)&=\sum_{Y \subseteq T}^{}(-1)^{\lvert T-Y \rvert} \widetilde{\phi}\,f(Y) \\
&=\sum_{Y \subseteq T}^{}(-1)^{\lvert T-Y \rvert}(\sum_{Z \subseteq Y}^{}f(Z)) \\
&\overset{*}{=} \sum_{Z \subseteq T}^{}(\sum_{Z \subseteq Y \subseteq T}^{}(-1)_{}^{\lvert T-Y \rvert})f(Z)
\end{aligned}
$$

不妨记 $\vert T-Z \rvert =m$, $\lvert T-Y \rvert=i$,  并固定集合 $Z, T$. 于是，$\sum_{Z \subseteq Y \subseteq T}^{}(-1)_{}^{\lvert T-Y \rvert} = \sum_{i=0}^{m}(-1)^i \binom{m}{i}=\delta_{0m}^{}$

而$\delta_{0m}^{}=1$ 当且仅当 $m=0$，若 $m \neq 0$, 则 $\delta_{0m}^{}=0$, 于是我们有

$$
\sum_{Z \subseteq T}^{}(\sum_{Z \subseteq Y \subseteq T}^{}(-1)_{}^{\lvert T-Y \rvert})f(Z)=f(T)
$$

从而说明，映射 $\psi=\phi_{}^{-1}$ , 命题得证。
<p align="right">Q.E.D.</p>

##### 对应的等价表述或推论
定理 5
:    设 $S$ 是一个集合，集合的元素是若干条 “性质”，另有一个给定的集合 $A$ ， $A$ 中的每一个元素可能满足 $S$ 中的部分或全部性质。此外我们设从 $A$ 到数域 $K$ 存在一个权重函数：$\omega:A \rightarrow K$。

:    对于 $S$ 的任意子集 $T$, 记函数 $f_{=}^{}(T)$ 是这样的一个函数：
    $$
    f_{=}^{}(T)=\sum \omega(x)
    $$

:    其中 $x$ 遍历 $A$ 中所有**恰好**具有集合 $T$ 中性质的元素，即 $x$ 具有所有 $T$ 中的性质，但是对于任何不在 $T$ 中的性质， $x$ 都不满足。

:    再记 $f_{\leq}^{}(T)$ 是一个这样的函数：
    $$
    f_{\leq}^{}(T)=\sum_{Y \subseteq T}f_{=}^{}(Y)
    $$

:    这个函数表示的含义其实就是 $A$ 中所有**至多**具有集合 $T$ 中性质的元素的权值之和。

:    根据[定理1]，如果我们已知每一个 $S$ 的子集在映射 $f_{\geq}^{}$ 下的值，那么我们有
    $$
    f_{=}^{}(T)=\sum_{Y \subseteq T}^{}(-1)_{}^{\lvert T-Y \rvert}f_{\leq}^{}(Y)
    $$
    
:    特别地，我们有
    $$
    f_{=}^{}(S)=\sum_{Y \subseteq S}^{}(-1)_{}^{\lvert S-Y \rvert}f_{\leq}^{}(Y)
    $$


定理 6
:    令 $A_1$, $A_2$, $\dots$, $A_n$ 是有限集 $A$ 的子集。对于 $[n]$ 的每个子集 $T$, 我们定义
    $$
    A_T=\bigcap_{i\notin T}A_i 
    $$
:    注意当 $T=[n]$ 时，$A_T=A$；并对于一切 $0 \leq k \leq n$，令
    $$
    S_k=\sum_{\vert T \rvert =k}^{}\lvert A_T \rvert
    $$

:    不妨以这样的视角来看待 $A$ 的子集：$A_1$, $A_2$, $\dots$, $A_n$ 相当于定义了 $n$ 条性质，这 $n$ 条性质组成了**定理5**中的集合 $S$, 而本定理中的集合 $A$ 仍等同于定理5中的集合 $A$；从组合意义上说， $\lvert A_T \rvert$ 代表的是就是在集合 $A$ 中**至多**不满足集合 $T$ 中指代的那些性质的元素的个数（相当于定理5中的 $f_{\leq}^{}(T)$）,而集合 $\overline{A_{1}^{}}\cap \overline{A_{2}^{}} \cap \cdots \overline{A_{n}^{}}$ 表示的即为所有不满足任何一条性质的元素的集合，相当于定理5中的 $f_{=}^{}(S)$. 根据定理5我们有
    $$
    \lvert \overline{A_1}\cap \overline{A_2} \cap \cdots \overline{A_n} \rvert = S_n - S_{n-1} + S_{n-2} - \cdots + (-1)^n S_0
    $$
    
:    其中 $S_n=\lvert A_{[n]}\rvert = \lvert A \rvert$.
    


































[^1]: 笔者注：原作者这里是什么意思我自己也不是非常清楚；
[^2]: 笔者注：抽屉原理也是类似的，原理的表述本身非常显然，显然到许多人根本不会去注意它，但是却可以和非常多的奇技淫巧结合得到许多意想不到的结论——组合数学的魅力或许就在于此吧；


