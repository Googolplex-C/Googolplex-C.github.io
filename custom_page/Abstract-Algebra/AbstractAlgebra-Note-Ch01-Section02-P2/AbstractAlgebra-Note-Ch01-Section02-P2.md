---
title: 抽象代数 笔记 Ch01 Section02 P2
date: 2019-02-21 16:19:59
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

接上一篇笔记 [抽象代数 笔记 Ch01 Section02](../AbstractAlgebra-Note-Ch01-Section02/AbstractAlgebra-Note-Ch01-Section02.html)

<!-- more -->

### Chapter 1 群（续）

#### Section 2 半群与群（续）

##### 定义 1.2.6 群的阶

设 $G$ 为群，$G$ 的阶指 $G$ 中元素的个数，记作 $\lvert G \rvert$

注解：

1. 这个定义和集合的基数定义是相容的；
2. 当 $ \lvert G \rvert < \infty$ 时，称 $G$ 是有限群，其运算可以用群表来表示；
3. 当 $ \lvert G \rvert = \infty$ 时，称 $G$ 是无限群；

##### 定义 1.2.7 元素的阶

设 $G$ 为群，且 $a\in G$，若对于任何 $n \in \mathbb{N}^+$，$a^n \neq e$，则称 $a$ 的阶为无穷. 若至少存在一个正整数 $m \in \mathbb{N}^+$ ，使得 $a^m=e$，定义 $a$ 的阶为 $\mathrm{min}(k \in \mathbb{N}\mid a^k=e)$，有时候也记作 $|a|$（但不常用）

注解：

1. $a$ 的阶为 $1$ ，当且仅当 $a=e$
2. $a$ 的阶和 $a^{-1}$ 的阶相等

##### 命题 1.2.7 

设 $G$ 是群，$a \in G$，则 $a$ 的阶为无穷，当且仅当：对于任意的 $m,n \in\mathbb{N} $，$a^m \neq a^n$.

*Proof*

若 $a$ 的阶无穷，反证 存在 $m,n \in\mathbb{N} $，$a^m = a^n$，不妨设 $m>n$，则 $a^{m-n}=e$，矛盾；

反之，若对于任意的 $m,n \in\mathbb{N} $，$a^m \neq a^n$. 不妨令 $n=0$ ，于是对于任意的 $m \in \mathbb{N}$，$a^m \neq e$.

<p align="right">Q.E.D. </p>


##### 命题 1.2.8 

设 $G$ 是群，$a \in G$， $a$ 的阶为 $d$，则有

1. $a^k=e$，当且仅当 $d \mid k$
2. $a^k=a^h$，当且仅当 $d \mid (h-k)$

*Proof*

我们只证 1 如下：

设 $k=dm$，其中 $m$ 是整数，于是 $a^k=a^{dm}=(a^d)^m=e^m=e$.

另一方面假设 $k=dq+r$，其中 $r \neq  0$ 是余数，从而 $r< d$，我们有 $a^k=a^{dq+r}=a^{dq}\cdot a^r=(a^d)^q\cdot a^r= e^q \cdot a^r =e \cdot a^r=a^r=e$，这与 $d$ 是 $a$ 的阶矛盾.

<p align="right">Q.E.D. </p> 

##### 命题 1.2.9

设 $G$ 是群，$a \in G$， $a$ 的阶为 $d$，则有：

1. $a^k$ 的阶为 $d/\mathrm{GCD}(d,k)$，其中 $k>0$
2. $a^k$ 的阶为 $d$，当且仅当 $\mathrm{GCD}(d,k)=1$

*Proof*

只需要证 1. 因为 2 可以从 1 直接推出.



不妨设 $a^k$ 的阶为 $q$，接下来我们需要证明 $q$ 和 $d/ \mathrm{GCD}(d,k)$ 是互相整除的，从而证明它们相等；

设 $d_1=d/\mathrm{GCD}(d,k)$， $k_1=k/\mathrm{GCD}(d,k)$

我们有 $(a^k)^q=e=a^{qk}$，故 $d \mid qk$，即 $d_1 \mid qk_1$，注意到 $d_1$ 和 $k_1$ 互素，因此 $d_1 \mid q$，即 $d/ \mathrm{GCD}(d,k)$ 整除 $q$.



反之，我们考虑 $(a^k)^{d_1}$，我们有 $a^{kd_1}=a^{k_1\cdot \mathrm{GCD}(d,k) \cdot d_1}=(a^{d})^{k_1}=e$，因为 $a^k$ 的阶为 $q$，故 $q \mid d_1$.

于是我们知道 $q = d/\mathrm{GCD}(d,k)$

<p align="right">Q.E.D. </p> 

##### 命题 1.2.10

设 $G$ 是群，$a,b \in G$，$a$ 的阶是 $m$，$b$ 的阶是 $n$，且 $ab=ba$，$\mathrm{GCD}(m,n)=1$，则 $ab$ 的阶为 $mn$.

思考题：

1. 若 $a,b$ 的阶有限，不假设 $ab=ba$，能否推出：$ab$ 的阶有限；
2. 若不假设 $\mathrm{GCD}(m,n)=1$，结论是什么？

*Proof*

设 $ab$ 的阶是 $q$，于是 $(ab)^{mn}=a^{mn}b^{mn}=e\cdot e =e$，由命题1.2.8 可知，$q \mid mn$

另一方面，考虑 $b^{qm}=a^{qm}b^{qm}=(ab)^{qm}=((ab)^q)^m=e^m=e$，所以由命题 1.2.8 可知，$n \mid qm$，注意到 $\mathrm{GCD}(m,n)=1$，所以 $n \mid q$；对于 $a^{qn}$ 可以类似地得到 $m \mid q$，即有 $mn \mid q$.

综合可知，$q=mn$.

<p align="right">Q.E.D. </p> 

##### 思考题

1. 按照邓老师的提示：$ab$ 的阶应该可能是无限的；因此我们必须考虑一个无限群；

   同时，还不满足交换律——我只能想到矩阵集与其上乘法构成的群……

   然后我就不会做了，如何构造具体的反例呢？

   然后，经过上网查找之后（所以这不是笔者想到的），我们有
   $$
   A=\begin{bmatrix}
   0 & -1 \\
   1 & 0
   \end{bmatrix}
   ,
   B=\begin{bmatrix}
   0 & 1 \\
   -1 & -1
   \end{bmatrix}
   $$
   它们的阶分别是 $4$ 和 $3$，但它们的乘积
   $$
   AB=\begin{bmatrix}
   1 & 1 \\
   0 & 1
   \end{bmatrix}
   $$
   阶为无穷；

   （好吧，我认输……）2 2234

2. 笔者猜想，此时结论应为：$ab$ 的阶为 $\mathrm{LCM}(m,n)$.

   *试证如下*：

   设 $p=\mathrm{LCM}(m,n)$，并设 $q$ 是 $ab$ 的阶，再设 $m_1=p/m$，$n_1=p/n$，仿照课堂的思路，我们尝试证明 $p,q$ 互相整除，从而相等；

   首先，考虑 $(ab)^p= a^pb^p=(a^m)^{m_1}(b^n)^{n_1}=e \cdot e=e$，所以由命题1.2.8 可知，$q \mid p$；

   另一方面，考虑 $a^{qn}=a^{qn}b^{qn}=(ab)^{qn}=e$，于是由命题 1.2.8 可知，$m \mid qn$ 即 $m_1 \mid qn_1$，注意到 $m_1,n_1$ 互素，因此 $m_1 \mid q$；同理可得 $n_1 \mid q$.



   	（然后做到这里我就卡住了……）

   	然后有一位网友给出了这样的反例构造：

​	考虑群 $\{Z18,+\}$，$3$ 的阶是 $6$，$6$ 的阶是 $3$，但 $3+6=9$ 的阶是 $2 \neq \mathrm{LCM}(6,3)$……

​	所以，我的猜想又错了. 啪啪啪，打脸……

### 后记

在做思考题第2问的时候，笔者求助了笔者加入的一个 “数学分析交流群” 的各位朋友，最终解决了这一问题；

谢谢 TA 们热情的参与，讨论和思考！**谢谢北场哥哥、想做名词党同学、zhy同学的讨论，谢谢海伦小姐姐同学给出的结论修正，以及——皮卡同学的idea（想到的反例）**，这种讨论着学习的感觉真好！