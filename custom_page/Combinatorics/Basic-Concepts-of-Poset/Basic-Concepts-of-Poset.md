---
title: 偏序集的基本概念
date: 2019-07-17 20 49 13
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
### 前言
在计数组合学中，偏序集扮演着重要的具有统一性的角色；

有两方面的组合学内容与其密切相关：

1. 莫比乌斯反演的相关理论本质上就是容斥原理在偏序集上的推广；

2. 二项式偏序集给不同的类型的生成函数提供了统一的讨论背景；

除此之外，组合学中还有许多别的有趣的内容与偏序集相关，偏序集也具有广泛的应用。

### 偏序集定义

#### 序关系的三大公理

序的三大公理
:    称一个定义在集合 $P$ 上的关系 $\leq_{P}^{}$ 为**序关系**，当且仅当该关系满足：

    1. 自反性：对于一切 $t \in P$, $t \leq_{P}^{} t$ 

    2. 反对称性：对于任意元素 $s, t \in P$, 若 $s \leq_{P}^{} t, t \leq_{P}^{} s$, 则有 $s = t$

    3. 传递性：若有 $s \leq_{P}^{}t$, 且 $t \leq_{P}^{}u$, 则有 $s \leq_{P}^{}u$

**记号约定**：

1. 记 $t \geq_{P}^{}s$ 表示 $s \leq_{P}^{}t$
2. 记 $s <_{P}^{} t$ 表示 $s \leq_{P}^{}t$ 且 $s \neq t$
3. 记 $t >_{P}^{}s$ 表示 $s <_{P}^{}t$
4. 若 $s \leq_{P}^{} t$ 或者 $t \leq_{P}^{}s$ 则称 $s$ 和 $t$ 是**可比较的**
5. 记 $s \parallel t$ 表示它们不可比较

偏序集
:    一个集合 $P$ 上定义了偏序关系 $\leq_{P}^{}$, 那么这个序结构 $\{P, \leq_{P}^{}\}$ 就是一个偏序集，或者简写为 $P$

**注解**:

1. 之所以序关系要写成 $\leq_{P}^{}$，原因是为了避免与传统数域上的小于等于关系的符号相混淆；此外，下标也能告诉我们，这个序关系是定义在某个特定的集合 $P$ 上的；

2. 所谓 “偏序” 的意思就是，这个集合上的某一对元素或许是可以比较的，或许是不可比较的——请注意序关系的定义只说明其是一个比较不平凡的关系，没有对元素序偶之间是否满足关系作出任何规定


#### 偏序集的例子

1. 记 $n \in \mathbb{N}_{}^{+}$, 设集合 $[n]=\{k \mid 1 \leq k \leq n\}$, 在其上定义序关系为经典意义下的 “大于小于关系”，则 $\boldsymbol{n}=\{[n],\leq\}$ 为偏序集；

2. 考虑集合 $S$ 的幂集，幂集中的元素（也即是 $S$ 的子集）在包含关系下构成偏序集；

3. 记 $n \in \mathbb{N}_{}^{+}$，考虑 $n$ 的一切正整数因子构成的集合 $D_n$ ，其在整除关系下构成偏序集；

4. 记 $n \in \mathbb{N}_{}^{+}$，考虑所有对于 $n$ 的分划构成的集合 $\prod_{n}^{}$, 若分划 $\pi$ 的每一个 block 都在另一个分划 $\sigma$ 的某个 block 中，那么记关系 $\pi \leq \sigma$, 集合 $\prod_{n}^{}$ 在此关系下构成偏序集；

5. 令 $B_{n}^{}(q)$ 为一切 $n$ 维线性空间构成的子空间 $F_{q}^{n}$, 其在包含关系下构成偏序集；

### 偏序集相关概念与性质

#### 同构
（偏序集的）同构
:    称偏序集 $P$ 和 $Q$ 是同构的，当且仅当它们之间存在一个双射 $\phi$，其自身与逆映射都具有保序性：
$$
s \leq_{P}^{} t \quad \text{in} \  P \Leftrightarrow \phi(s) \leq_{Q}^{} \phi(t) \quad \text{in} \ Q
$$
    记作 $P \cong Q$



#### 子偏序集
在定义子偏序集的时候，我们需要更加仔细。在此，我们定义两种具有不同意义的偏序集。

弱子偏序集 (weak suposet)
:    设 $P$ 是个偏序集，而有 $Q$ 是前者的子集，并且在 $Q$ 上定义序关系，满足：

    若在集合 $Q$ 中有 $s \leq t$, 则在 $P$ 中亦有 $s \leq t$

    则称 $Q$ 是 $P$ 的弱子偏序集。
  
加细 (refinement)
:    若集合 $Q$ 是 $P$ 的弱子偏序集，且有 $P=Q$, 那么称 $P$ 是 $Q$ 的一个加细(refienement)

    **注意**：顺序不要搞错，$Q$ 是子偏序集，但 $P$ 才是加细！

导出子偏序集 (induced subposet)
:    设 $P$ 是个偏序集，而有 $Q$ 是前者的子集，并且在 $Q$ 上定义序关系，满足：

    在集合 $Q$ 中有 $s \leq t$, 当且仅当在 $P$ 中有 $s \leq t$

    则称 $Q$ 是 $P$ 的导出子偏序集。

    **注**：对于有限偏序集 $P$，其导出子偏序集的数目为 $2_{}^{\lvert P \rvert}$

子偏序集 (subposet)
:    **默认指代：导出子偏序集**

导出序 (induced order)
:    若 $P$ 是偏序集，偏序集 $Q$ 是偏序集 $P$ 的导出子偏序集，那么称 $Q$ 具有导出序



#### 区间与覆盖
闭区间 (closed interval)
:    设 $P$ 是偏序集，有 $s,t \in P$ 且 $s \leq t$，记 $[s,t]$ 是 $P$ 的闭区间，使得
$$
[s,t]=\{u \in P \mid s \leq u \leq t\}
$$

    **注**：
    1. 空集 $\varnothing$ 不是闭区间
    2. $[s,s]=\{s\}$

开区间 (open interval)
:    设 $P$ 是偏序集，有 $s,t \in P$ 且 $s \leq t$，记 $(s,t)$ 是 $P$ 的开区间，使得
$$
(s,t)=\{u \in P \mid s < u < t\}
$$

    **注**：
    1. 空集 $\varnothing$ 是开区间
    2. $(s,s)=\varnothing$

局部有限偏序集 (locally finite poset)
:    若偏序集 $P$ 的每个区间都是有限集，那么称其为局部有限偏序集

凸子偏序集
:    设 $P$ 是偏序集，$Q$ 是其子偏序集，称后者为凸子偏序集，当且仅当：
$$
(\forall s,u,t \in P)\quad s <_{P}^{} t <_P u \ \wedge s,u \in Q \rightarrow t \in Q
$$

覆盖关系
:    设 $s,t \in P$, 若有 $s < t$ 且不存在元素 $u \in P$ 使得 $s < u < t$, 则称 $s$ 被 $t$ 覆盖，或称 $t$ 覆盖 $s$， 记作 $s \lessdot t$ 或者 $t \gtrdot s$

    **注**:
    
    1. $s \lessdot t$ 当且仅当 $s < t \ \wedge [s,t]={s,t}$

    2. 局部有限偏序集完全由其覆盖关系确定；



#### Hasse 图
Hasse Graph
:    设 $P$ 是个偏序集，定义一个图：其结点都是 $P$ 中的元素，边是元素间的覆盖关系（即从存在覆盖关系的两个元素间通过边相连接），并且若 $s < t$，则 $s$ 在图中位于 $t$ 的下方。这样的图称为此偏序集 $P$ 的 Hasse 图。

**辨析**

1. 请注意，Hasse 图中各边表示的是 覆盖关系，而不是所有的序关系，所以以下的图是冗余的：

```viz{align=center}
graph G{
    graph[rankdir=BT];

    a[shape="point"]
    b[shape="point"]
    c[shape="point"]
    d[shape="point"]

    a -- b
    a -- c
    b -- d
    c -- d
    a -- d[constraint=false]
}
```

2. 应该修正成这个样子：

```viz{align=center}
graph G{
    graph[rankdir=BT];

    a[shape="point"]
    b[shape="point"]
    c[shape="point"]
    d[shape="point"]

    a -- b 
    a -- c
    b -- d
    c -- d
}
```


#### 序关系下的一些特殊元
##### 最大元与最小元
最小元(minimum element)
:    若元素 $a \in P$, $P$ 是偏序集，且满足
$$
(\forall s \in P), \ a \leq s
$$

    则称 $a$ 是 $P$ 的最小元，也可以记作 $\widehat{0}$

最大元(maximum element)
:    若元素 $a \in P$, $P$ 是偏序集，且满足
$$
(\forall s \in P), \ a \geq s
$$

    则称 $a$ 是 $P$ 的最大元，也可以记作 $\widehat{1}$

##### 极大元与极小元
极小元(minimal element)
:    若元素 $a \in P$, $P$ 是偏序集，且满足
$$
\neg\ (\exists s \in P), \ \text{s.t.}\ s < a
$$

    则称 $a$ 是 $P$ 的极小元

极大元(maximal element)
:    若元素 $a \in P$, $P$ 是偏序集，且满足
$$
\neg\ (\exists s \in P), \ \text{s.t.}\ s > a
$$

    则称 $a$ 是 $P$ 的极大元

##### 极大与最大的区别
其实非常简单

- “极大” 的意思，是 “没有别的谁比他大”

- “最大” 的意思，是 “比其他任何人都更大”

- 最大元必定是极大元，但反之不一定；

- “某个极大元不是最大元“ 的原因是，有些元素和该极大元不可比

- 不过在全序集中， “最大” 和 “极大” 就是等价的

#### 链
##### 概念定义
链 / 全序集 / 线序集 (chain / totally ordered set / linear ordered set)
:    设 $P$ 是偏序集，若 $P$ 中的任何两个元素都可比，则称 $P$ 为 链

（某个）偏序集的链 (chain of a certain poset)
:    设 $P$ 是偏序集，称 $C$ 是 $P$ 的链，当且仅当 $C$ 是 $P$ 的子偏序集，且 $C$ 本身是一个链；

极大链 (maximal chain)
:    设 $C$ 是 $P$ 的链，若不存在$P$ 的某个链使得 $C$ 能被其包含，那么 $C$ 是个极大链

饱和链 (saturated chain)
:    称偏序集 $P$ 的链 $C$ 是饱和的，当且仅当：不存在某个 $u \in P-C$, 使得
    - 对于某元素 $s, t \in C$, 有 $s <_{P}^{} u <_{P}^{} t$,；
    - 使得 $C \cup \{u\}$ 仍是链

链的长度 (length / rank of the chain)
:    记链的长度为 $\ell(C):=\lvert C \rvert -1$

偏序集的长度 (length / rank of the chain)
:    记偏序集的长度为 $\ell(P):= \max \{\ell(C) \mid C \text{ is a chain of }P\}$

闭区间的长度 (length / rank of the 从closed interval)
:    闭区间本质上也是一个偏序集，套用上一个定义即可。



**命题1**

极大链一定是饱和链，但反之不必然

*Proof*

  非常简单，如果极大链 $C$ 不是饱和链，也就是存在某个元素  $u \in P-C$, 使得 $C \cup \{u\}$ 仍是链，那么 $C \subseteq C \cup \{u\}$, 产生矛盾。

  另一方面，去掉极大链的最大元，那么剩下来的偏序集任构成一个饱和链，但是这个子链显然已经不是极大链。

  <p align="right">Q.E.D.</p>
  
有秩偏序集 (graded poset)
:    设 $P$ 是偏序集，若 $P$ 的任何一条极大链都具有相同的长度 $
n$，则称 $P$ 是秩为 $n$ 的有秩偏序集。

**命题2**

若 $P$ 是有秩偏序集，其秩为 $n$，那么可以递归地定义函数：$\rho: P \rightarrow [n]$ 如下

$$
\rho(s)= \begin{cases}
0  &\text{if } s \text{ is a minimal element in P} \\
\rho(t)+1 &\text{if } s \gtrdot t
\end{cases}
$$

此函数是良定义的。

本来想证明一下的，可是发现事情太多，人生好短，这个命题也不难，只是叙述比较麻烦，所以就算了吧

秩
:    有秩偏序集中的元素 $s$, 其 在命题2 中定义的映射下的数值 $\rho(s)$ 即为它的秩

多重链
:    偏序集 $P$ 的多重链是一个多重集，并且其 underlying set 是 $P$ 的链

    **注解**

    其实，多重链可以直观地表示成如下的形式

    $$
    s_1 \leq s_2 \leq \cdots \leq s_n
    $$
    
#### 反链
反链 (antichain / Sperner family / clutter)
:    设 $P$ 是偏序集，$A$ 是 $P$ 的子集，若 $A$ 中任意两个元素都是不可比的，那么称 $A$ 是一个反链。

序理想 (order ideal / semi-ideal / down-set / decreasing subset)
:    a subset $I$ such that if $t \in I$ and $s \leq t$, then $s \in I$.

对偶序理想 (up-set / increasing subset / filter)
:    a subset $I$ such that if $t \in I$ and $s \geq t$, then $s \in I$.

**命题3**

偏序集的反链和序理想存在着微妙的一一对应关系。
反链可以视作序理想的极大元的集合，即有
$$
I=\{s \in P \mid s \leq t \ \text{ for some } t \in A\}
$$



**记法约定**

若反链 $A$ 和序理想 $I$ 满足命题3 中的关系，那么我们称 **$A$ 生成了 $I$**；

并且若 $A$ 显式地记为 $\{t_1, t_2, \dots, t_n\}$, 那么其生成的序理想 $I$ 记为 $<t_1, t_2, \dots, t_n>$
