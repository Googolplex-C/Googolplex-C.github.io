---
title: 'Problem of Longest Monotonic- Subsequence'
date: 2019-02-17 21:44:26
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

#### Title

设一个实数序列的长度为 $n$，序列中最大非递减子序列的长度为 $a$，最大非递增子序列长度为 $d$，试证：$a \cdot d \geq n$.

<!-- more -->

#### *Proof*

##### Version 1

不妨设该序列为
$$
S_1, \ S_2, \ S_3,\ \cdots, \ S_{n-1},\ S_n
$$
构造一个新的整数列 $\{m_k\}_{k=1}^n$：$m_k$ 是将原序列 $\{S\}$ 前 $k-1$ 项去掉后，以 $S_k$ 为首的剩余项构成的序列中最大非递减子序列的长度.

由题意可知，原序列 $\{S\}$ 中最大非递减子序列的长度为 $a$，所以序列 $\{m_k\}$ 的取值范围为 $[a]$，共 $a$ 种可能. 而序列 $\{m_k\}$ 本身有 $n$ 项——由抽屉原理可知，序列 $\{m_k\}$ 中必定有 $\lceil \frac{n}{a} \rceil$ 项取得相同的数值. 不妨设它们取得的值为 $p$ .

令 $x=\lceil \frac{n}{a} \rceil$，我们将序列 $\{m_k\}$ 中这些取值为 $p$ 的项写成子序列
$$
m_{k_1}, \ m_{k_2}, \ m_{k_3}, \ \cdots, \ m_{k_x}
$$
注意到，对于任意满足 $1\leq i < j \leq x$ 的指标 $i$ , $j$，项 $m_{k_i}$ 和 $m_{k_j}$ 所各自对应的原序列中的项 $S_{k_i}$ 和 $S_{k_j}$ 满足
$$
S_{k_i} > S_{k_j}
$$
假设不然，即 $S_{k_i} \leq S_{k_j}$，则在原序列去掉前 $k_j-1$ 项后，以 $S_{k_j}$ 开头的部分序列中的最大非递减子序列与项 $S_{k_i}$ 合并后，仍是原序列的一个非递增子序列，如此一来， $m_{k_i}=m_{k_j}$ 显然不再成立，而只能有 $m_{k_i} >m_{k_j}$. 

于是，$m_{k_1}, \ m_{k_2}, \ m_{k_3}, \ \cdots, \ m_{k_x}$的下标对应的原序列中的项 $S_{k_1}, \ S_{k_2}, \ S_{k_3}, \ \cdots, \ S_{k_x}$ 构成了一个严格递减（同时自然是非递增的）子序列，长度恰为 $x=\lceil \frac{n}{a} \rceil$.

又，原序列中最大非递增子序列的长度为 $d$，自然有 $d \geq x = \lceil \frac{n}{a} \rceil$ 成立，于是我们有
$$
a\cdot d \geq a\cdot x=a \cdot \lceil \frac{n}{a}\rceil \geq a \cdot \frac{n}{a}=n
$$
命题得证.

<p align="right">Q.E.D.</p>

##### Version 2

在之前一片博文 [Mirsky's and Dilworth's theorem](../Mirsky's-and-Dilworth's-theorem/Mirsky's-and-Dilworth's-theorem.html) 中，我们已经介绍了偏序集上的 *Mirsky* 定理和 *Dilworth* 定理，这两个优美的定理足以用来本问题的结论. 下面试证之.

构造有序对集合 $T=\{(k,S_k)\ |\ 1 \leq k \leq n\}$ ，显然 $T$ 中的元素与原序列 $\{S\}$ 的项是可以（按照下标）一一对应的；

在集合 $T$ 上定义关系 $\leq_A$ ：
$$
(i,S_i) \leq_A (j,S_j)\quad \mathrm{iff}\quad i<j\ \text{且}\ S_i \leq S_j
$$
显然关系 $\leq_A$ 是序关系，读者自证不难 .

重要是我们不难注意到，**原序列中的一切非递减子序列在 $T$ 中都对应着一条链，同时原序列的一切递减（从而非递增）子序列在 $T$ 中都对应一个反链. **

根据题设，可以马上推知，偏序集 $T$ 的高为 $a$，由 *Mirsky* 定理可知，$T$ 可以恰好分划为 $a$ 个反链，那么根据抽屉原理，必定有一个反链的基数至少为 $\lceil \frac{n}{a} \rceil$ ，也即，必定对应原序列中存在的一条长度至少为 $\lceil \frac{n}{a} \rceil$ 的递减子序列. 自然地，我们有
$$
a\cdot d \geq a \cdot \lceil \frac{n}{a}\rceil \geq a \cdot \frac{n}{a}=n
$$
命题得证.

<p align="right">Q.E.D.</p>

#### Other Forms

该命题有着一些较弱的表述形式，比如：

一个长为 $mn+1$ 的序列，要么具有长度至少为 $m+1$ 的非递增子序列，要么具有长度至少为 $n+1$ 的非递减子序列.

这个命题其实就是 *Erdős–Szekeres theorem*（或至少是这个定理的其中一种表述形式），它几乎会出现在所有的面向本科的组合数学教材中.

#### Note

1. 不要把两种版本的证明看作是两种不同的证明方法，它们本质是相同的，只不过第二种方法使用了 *Mirsky* 定理（或者 *Dilworth* 定理），但这两种定理本身的证明是不太容易的——在数学中，高级知识能简洁地解决问题，很大程度上是因为这些较高级知识 “封装” 了各种巧妙的初等技巧；

2. 在做第二种证明的时候，千万**注意**：我们并不是直接在原来的序列 $\{S\}$ 上应用偏序集的那两个定理，而是经过多一层构造，并在新构造的集合 $T$ 上定义新的偏序关系 $\leq_A$；这和原来的实数上的序关系 $\leq$ 已经不一样了；

    ——如果思路在这里没有转换过来，那么就很难找到思路：因为  $(S, \leq)$ 本身已经是全序集了，直接套定理将什么也推不出，lol.

