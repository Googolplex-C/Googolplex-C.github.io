---
title: Combinatorics Exercise 001
date: 2019-01-01 00:00:00
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

已知 $n$ 个黑盒子中装有若干个可相互区分的元素，从这些盒子中取出所有元素装进 $n+1$ 个白盒子中，并使得所有白盒子非空. 试证明：存在两个元素，其中每一个元素原先所在的黑盒子元素数目大于其现处的白盒子元素数目. 

<!-- more -->  

##### *Proof*

记元素的总数目为 $N$，注意到由于所有的白盒子非空，因此 $N \geq n+1$ . 记白盒子为 $A_i$ ，其中 $1 \leq i \leq n+1$ . 记黑盒子为 $B_i$ ，其中 $1 \leq i \leq n$ .记盒子 $A$, $B$ 的元素数目为 $\lvert A \rvert$ , $\lvert B \rvert$.

不失其一般性，假定白盒子和黑盒子分别根据其元素数目按照非递增顺序排列，于是可知：
$$
\lvert A_1 \rvert \geq \lvert A_2 \rvert \geq \lvert A_3 \rvert \geq \cdots \geq \lvert A_{n+1} \rvert > 0
\label{one}
$$

$$
\lvert B_1 \rvert \geq \lvert B_2 \rvert \geq \lvert B_3 \rvert \geq \cdots \geq \lvert B_{n} \rvert
\label{two}
$$

分别定义有限长的集合列 $\{R\}_{k=1}^{n+1}$ , $\{S\}_{k=1}^{n}$ 如下：
$$
\begin{gather}
R_k = \bigcup_{i=1}^k A_i \qquad \text{where} \quad 1 \leq k \leq n+1\\
S_k = \bigcup_{i=1}^k B_i \qquad \text{where} \quad 1 \leq k \leq n
\label{three}
\end{gather}
$$
注意到 $A_i \cap A_j = \varnothing$, $B_i \cap B_j = \varnothing$ （其中 $i \neq j$  ），因此有：
$$
\begin{gather}
\lvert R_k \rvert = \sum_{i=1}^k \, \lvert A_i \rvert \qquad \text{where} \quad 1 \leq k \leq n+1\\
\lvert S_k \rvert = \sum_{i=1}^k \, \lvert B_i \rvert \qquad \text{where} \quad 1 \leq k \leq n
\label{four}
\end{gather}
$$
不难得知：
$$
0 < \lvert R_1 \rvert < \lvert R_2 \rvert < \cdots < \lvert R_n \rvert < \lvert R_{n+1} \rvert  
\label{five_1}
$$

$$
0 < \lvert S_1 \rvert \leq \lvert S_2 \rvert \leq \cdots \leq \lvert S_n \rvert
\label{five_2}
$$

注意到，因为白盒子全部非空，所以集合序列 $\{R\}$ 严格递增.

对 $\{R\}$ , $\{S\}$ 两个集合序列根据其基数大小按照非递减顺序进行归并排序，并且规定：

- 若存在 $i, j$ 使得$\lvert R_i \rvert = \lvert S_j \rvert$ ，则在归并得到的新序列中令 $S_j$ 排在 $R_i$ 之前.

易知按此方式构造得到的新序列唯一，且序列的最后一项为 $R_{n+1}$ ，倒数第二项为 $S_n$ .

1. 若第一项为 $R_1$：

    于是归并得到的序列具有如下的形式：
    $$
    R_1, \  \cdots, \  S_n, \  R_{n+1}
    \label{six}
    $$

    由约束条件和$\{R\}$ , $\{S\}$ 的定义可知：
    $$
    \lvert S_1 \rvert = \lvert B_1 \rvert > \rvert R_1 \rvert= \lvert A_1 \rvert  >0
    \label{seven}
    $$

    进而
    $$
    \lvert S_1 \rvert = \lvert B_1 \rvert \geq 2
    \label{eight}
    $$

    即 $B_1$ 中至少有两个元素，显见这两个元素满足本题所欲证命题所述性质.

2. 若第一项为 $S_1$：

    于是归并得到的新序列具有如下的形式：
    $$
    S_1, \  \cdots, \  S_n, \  R_{n+1}
    \label{nine}
    $$

    注意到序列中省略号部分为 $n$ 个来自序列 $\{R\}$ 的项以及  $n-2$ 个来自序列 $\{ S \}$ 的项. 
    由抽屉原理可知，存在 $0 \leq i \leq n-1, \ 0 \leq j \leq n-1$ 及 $p \geq 1$ 使得：
    $$
    \lvert S_i \rvert \leq \underbrace{\lvert R_j \rvert < \cdots < \lvert R_{j+p} \rvert}_{\text{存在至少}\,2\,\text{项}(p\geq1)} < \lvert S_{i+1} \rvert
    \label{ten}
    $$

    即存在**至少 $2$ 个**来自序列 $\{R\}$ 的项，夹在来自序列 $\{S \}$ 的相邻的某两项之间.  
    固定下标 $i,j,p$ ，进而有：
    $$
    \begin{align}
    &\lvert B_{i+1} \rvert = \lvert S_{i+1} \rvert - \lvert S_{i} \rvert \\
    &> \lvert R_{j+p} \rvert - \lvert R_{j} \rvert 
    = \sum_{k=1}^{p}\lvert A_{j+k} \rvert \\
    &\geq \lvert A_{j+1} \rvert
    \label{eleven}
    \end{align}
    $$

    于是：
    $$
    \lvert B_1 \rvert \geq \cdots \geq \lvert B_{i+1} \rvert > \lvert A_{j+1} \rvert \geq \cdots \geq \lvert A_{n+1} \rvert >0
    \label{twelve}
    $$

    另外，可知：
    $$
    \lvert S_{i+1} \rvert \geq \lvert R_{j} \rvert + 2
    \label{thirteen}
    $$

    从而
    $$
    \lvert S_{i+1} \rvert + (N - \lvert R_j \rvert) \geq N+2 \quad \Longrightarrow \quad \left| \bigcup_{k=j+1}^{n+1} A_k\right| +\left| \bigcup_{l=1}^{i+1} B_l\right| \geq N+2
    \label{fourteen}
    $$

    注意到 $\left| (\bigcup_{k=j+1}^{n+1} A_k) \ \bigcup \ (\bigcup_{l=1}^{i+1} B_l) \right| \leq N$ 必然成立，由容斥原理可知：
    $$
    \left| (\bigcup_{k=j+1}^{n+1} A_k) \ \bigcap \ (\bigcup_{l=1}^{i+1} B_l) \right| \geq 2
    \label{fifteen}
    $$

    直观而言，前 $i+1$ 个黑盒子的元素总数比前 $j$ 个白盒子的元素总数多 $2$ ，因此在重新装配的过程中，在前 $i+1$ 个黑盒子中存在至少两个元素，它们必将被 “抽补” 到第 $j+1$ 个白盒子及其（在序列 $\{A \}$ 中）之后的盒子中去；而这前 $i+1$ 个黑盒子中元素数最小的盒子的元素数 $\lvert B_{i+1} \rvert$ 比白盒子中具有最大元素数的白盒子的元素数目 $\lvert A_{j+1} \rvert$都大，于是这两个元素满足欲证命题所述性质.

综上所述，命题成立.	

<p align="right"> Q.E.D. </p>

##### Note
以上是笔者在 2015 年三月的时候想到的原始版本，原证明的核心部分进行了一次分类讨论，但实际上，情形 1 和情形 2 的数量关系以及其结论推导的影响是等同的，因此可以将这两种情形合并在一起，而无需进行分类讨论。

下面是改进后的证明：

对 $\{R\}$ , $\{S\}$ 两个集合序列根据其基数大小按照非递减顺序进行归并排序，并且规定：

- 在 $\{R\}$ , $\{S\}$ 中分别添加两项 $R_0$, $S_0$，其中 $R_0=S_0=0$ .
- 若存在 $i, j$ 使得$\lvert R_i \rvert = \lvert S_j \rvert$ ，则在归并得到的新序列中令 $S_j$ 排在 $R_i$ 之前.

易知按此方式构造得到的新序列唯一，且第一项为 $S_0$, 第二项为 $R_0$；序列的最后一项为 $R_{n+1}$, 倒数第二项为 $S_n$, 如下所示：

$$
S_0, \ R_0 \cdots, \  S_n, \  R_{n+1}
\label{sixteen}
$$

注意到序列中 $S_0$ 和 $S_n$ 中间包含了 $n+1$ 个来自序列 $\{R\}$ 的项以及  $n-1$ 个来自序列 $\{ S \}$ 的项. 
由抽屉原理可知，存在 $0 \leq i \leq n-1, \ 0 \leq j \leq n-1$ 及 $p \geq 1$ 使得：
$$
\lvert S_i \rvert \leq \underbrace{\lvert R_j \rvert < \cdots < \lvert R_{j+p} \rvert}_{\text{存在至少}\,2\,\text{项}(p\geq1)} < \lvert S_{i+1} \rvert
\label{seventeen}
$$

即存在**至少 $2$ 个**来自序列 $\{R\}$ 的项，夹在来自序列 $\{S \}$ 的相邻的某两项之间.  
固定下标 $i,j,p$ ，进而有：
$$
\begin{align}
&\lvert B_{i+1} \rvert = \lvert S_{i+1} \rvert - \lvert S_{i} \rvert \\
&> \lvert R_{j+p} \rvert - \lvert R_{j} \rvert 
= \sum_{k=1}^{p}\lvert A_{j+k} \rvert \\
&\geq \lvert A_{j+1} \rvert
\label{eighteen}
\end{align}
$$

于是：
$$
\cdots \geq \lvert B_{i+1} \rvert > \lvert A_{j+1} \rvert \geq \cdots  >0
\label{nineteen}
$$

另外，可知：
$$
\lvert S_{i+1} \rvert \geq \lvert R_{j} \rvert + 2
\label{twenty}
$$

从而
$$
\lvert S_{i+1} \rvert + (N - \lvert R_j \rvert) \geq N+2 \quad \Longrightarrow \quad \left| \bigcup_{k=j+1}^{n+1} A_k\right| +\left| \bigcup_{l=1}^{i+1} B_l\right| \geq N+2
\label{twenty-one}
$$

注意到 $\left| (\bigcup_{k=j+1}^{n+1} A_k) \ \bigcup \ (\bigcup_{l=1}^{i+1} B_l) \right| \leq N$ 必然成立，由容斥原理可知：
$$
\left| (\bigcup_{k=j+1}^{n+1} A_k) \ \bigcap \ (\bigcup_{l=1}^{i+1} B_l) \right| \geq 2
\label{twenty-two}
$$

直观而言，前 $i+1$ 个黑盒子的元素总数比前 $j$ 个白盒子的元素总数多 $2$ ，因此在重新装配的过程中，在前 $i+1$ 个黑盒子中存在至少两个元素，它们必将被 “抽补” 到第 $j+1$ 个白盒子及其（在序列 $\{A \}$ 中）之后的盒子中去；而这前 $i+1$ 个黑盒子中元素数最小的盒子的元素数 $\lvert B_{i+1} \rvert$ 比白盒子中具有最大元素数的白盒子的元素数目 $\lvert A_{j+1} \rvert$都大，于是这两个元素满足欲证命题所述性质.

<p align="right">Q.E.D.</p>


#### Generalized Title
已知 $n$ 个黑盒子中装有若干个可相互区分的元素，从这些盒子中取出所有元素装进 $n+k$ 个白盒子中（$k \geq 1$），并使得所有白盒子非空. 试证明：存在 $k+1$ 个元素，其中每一个元素原先所在的黑盒子元素数目大于其现处的白盒子元素数目. 

##### Proof of the generalized title
当一个盒子装有元素的时候，对这个盒子里的全体元素赋值为 $1$, 同时每一个元素对其赋值为 $\frac{1}{n}$ ，其中 $n$ 是这个盒子目前所装的元素数目。

我们注意到，每一个元素，无论其是在黑或白的哪一个盒子中，其取值范围为 $(0,1]$. 

考虑黑白两种盒子在元素重新装载前后的值分别为 $X$, $Y$，并且有
$$
Y = n+k > X \geq n
$$

注意到元素的总数是不变的，之所以有 $Y > X$, 正是因为存在某些元素，它们的赋值变大了，最终使得 $Y$ 增大了。

而我们已经知道，每一个元素的取值范围为 $(0,1]$. 因此对于赋值增大的元素，其每一个元素的增值小于 $1$，另一方面有 $Y-X \geq k$, 因此所有赋值增加的元素数目必定**严格大于 $k$**，而这些元素原先所在的黑盒子元素数目就大于其现处的白盒子元素数目，于是命题得证。

<p align="right">Q.E.D.</p>

##### Note
这个精妙而短小的证明据说出自伟大的高斯，它直接证明了原命题的推广形式，而且极其漂亮，作者也一并将它记录下来。
