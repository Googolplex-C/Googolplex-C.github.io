---
title: Sperner Theorem
date: 2019-01-20 20:11:37
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

本文介绍并证明全集 $U$ 的子集族上的 Sperner 定理，并在此基础上完成其拓展命题的证明。

<!-- more -->

**约定**：记全集为 $U$，且 $\lvert U \rvert=n$；记全集 $U$ 的元为 $e$ ；记全集的幂集为 $2^{U}$，其幂集的子集为 $U$ 的子集族记作 $\mathcal{F}$ . 以上符号可以附带上下标. 

##### Sperner 定理

**$2^U$上的反链的基数至多为 ${n \choose \lfloor n/2 \rfloor}= {n \choose \lceil n/2 \rceil}$.**

我们注意到以下几个重要引理.

> 引理1：若集合 $A$ 和 $B$ 具有相同的基数，且它们都非空，并有 $A \neq B$ ，则 $A \nsubseteq B$ ，同时 $B \nsubseteq A$ .
>
> 证略.



> 引理2：若 $\mathcal{F}_1$ 是链， $\mathcal{F}_2$ 是反链，则 $\lvert \mathcal{F}_1 \cap \mathcal{F}_2 \rvert \leq 1$.
>
> 证：
>
> 设 $\mathcal{P}=\mathcal{F}_1 \cap \mathcal{F}_2$，假若 $\lvert \mathcal{F}_1 \cap \mathcal{F}_2 \rvert > 1$，则存在两个元素 $A_1, A_2 \in \mathcal{P}$.
> 注意到 $A_1, A_2$ 本身是全集 $U$ 的子集.
> $\because$ $A_1, A_2 \in \mathcal{F}_1$
> $\therefore$  $A_1 \subseteq A_2$ 或者 $A_2 \subseteq A_1$
>
> 又，$\because$ $A_1, A_2 \in \mathcal{F}_2$
> $\therefore$  $A_1 \nsubseteq A_2$ 并且 $A_2 \nsubseteq A_1$
>
> 产生矛盾，于是原命题成立 .



> 引理3：若集合 $A$ 是全集 $U$ 的子集，且 $\lvert A \rvert =k$，则所有满足 $A\in \mathcal{F}$ 的满链 $\mathcal{F}$ 的数目为 $k!\,(n-k)!$
> 特别地，$2^U$ 上的所有满链数目为 $n!$
>
> 证略.

***Proof***

Part 1：现证明，对于全集 $U$，存在子集族 $\mathcal{F}$ 使得 $\lvert \mathcal{F} \rvert= {n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$

考虑子集族 $\mathcal{F}_0 = \{ A \in 2^U \mid \lvert A \rvert =  \lfloor n/2 \rfloor \}$，可知对于一切 $A_1,A_2 \in \mathcal{F}_0$，有$A_1 \neq A_2, \ \lvert A_1 \rvert = \lvert A_2 \rvert$ .
由引理 1 可知，$A_1 \nsubseteq A_2$ 并且 $A_2 \nsubseteq A_1$

于是，$\mathcal{F}_0$ 是反链.

Part 2：现证明，$2^U$ 上的反链的基数不能大于 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$

使用反证法，假定存在反链 $\mathcal{A}$ 使得 $\lvert \mathcal{A} \rvert > {n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$

对于所有 $A \in \mathcal{A}$，构造序对集 $P(A)=\{(A, \mathcal{L}) \mid \mathcal{L} \text{是满链}, A \in \mathcal{L} \}$.

于是有
$$
\sum_{A \in \mathcal{A}}  \Bigl| P(A) \Bigr| = \sum_{A \in \mathcal{A}}\Bigl( \lvert A \rvert!(n-\lvert A \rvert)! \Bigr)
$$
注意到当且仅当 $\lvert A \rvert = \lfloor n/2 \rfloor$ 时，$\lvert A \rvert!(n-\lvert A \rvert)!$ 取得最小值，即有：
$$
\sum_{A \in \mathcal{A}}\Bigl| \lvert A \rvert!(n-\lvert A \rvert)! \Bigr| \geq \lvert \mathcal{A}\rvert \cdot \Bigl( \lfloor n/2 \rfloor!(n-\lfloor n/2 \rfloor)! \Bigr)
$$
由因为 $\lvert \mathcal{A} \rvert > {n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$，因此有
$$
\lvert \mathcal{A}\rvert \cdot \Bigl( \lfloor n/2 \rfloor!(n-\lfloor n/2 \rfloor)! \Bigr) >{n \choose \lfloor n/2 \rfloor} \cdot \Bigl( \lfloor n/2 \rfloor!(n-\lfloor n/2 \rfloor)! \Bigr) = n!
$$
由引理 3 可知，全集 $U$ 的所有的满链的数目为 $n!$ ，于是由抽屉原理可知：
对于某个满链，记作 $\mathcal{L}_0$ ，存在$A_1,A_2 \in \mathcal{A}$，使得 $(A_1,\mathcal{L}_0),  (A_2,\mathcal{L}_0) \in \bigcup_{A \in \mathcal{A}} P(A)$

另外由序对 $(A, \mathcal{L})$ 的定义可知，$A_1, A_2 \in \mathcal{L}_0$；但同时 $A_1, A_2 \in \mathcal{A}$ .

于是
$$
\lvert \mathcal{A}\  \cap \ \mathcal{L}_0 \rvert \geq 2 >1
$$
与引理 2 矛盾.
于是 Part 2 证明完毕.

综合 Part 1 和 Part 2，原定理得证.

<p align="right">Q.E.D</p>

##### 拓展命题
**1. 设 $n$ 为偶数，反链 $\mathcal{A}$ 的基数为 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$ ，当且仅当其恰由 $U$ 的所有 $\lfloor n/2 \rfloor$-子集构成；**

**2. 设 $n$ 为奇数，反链 $\mathcal{A}$ 的基数为 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$ ，当且仅当其或者由 $U$ 的所有 $\lfloor n/2 \rfloor$-子集构成，或者由 $U$ 的所有 $\lceil n/2 \rceil$-子集构成，但 $\mathcal{A}$ 中不能同时存在 $\lfloor n/2 \rfloor$-子集和 $\lceil n/2 \rceil$-子集.**

> 引理4：若反链 $\mathcal{A}$ 的基数为 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$，则对于一切 $A \in \mathcal{A}$，$\lvert A \rvert = \lfloor n/2 \rfloor$ 或者 $\lvert A \rvert = \lceil n/2 \rceil$
>
> 证：
>
> 结合 Sperner 定理证明的 Part 2 可知：
> $$
> \sum_{A \in \mathcal{A}}  \Bigl| P(A) \Bigr| = \sum_{A \in \mathcal{A}}\Bigl( \lvert A \rvert!(n-\lvert A \rvert)! \Bigr) \leq n!
> $$
> 由条件知反链 $\mathcal{A}$ 的基数为 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$，而
> $$
> \min(\sum_{A \in \mathcal{A}}\Bigl( \lvert A \rvert!(n-\lvert A \rvert)! \Bigr))= \sum_{A \in \mathcal{A}}\min\Bigl( \lvert A \rvert!(n-\lvert A \rvert)! \Bigr)
> \\ = {n \choose \lfloor n/2 \rfloor}\cdot \Bigl( \lfloor n/2 \rfloor!(n-\lfloor n/2 \rfloor)! \Bigr) =n!
> $$
> 也即反链 $\mathcal{A}$ 中的子集元素必须是 $\lfloor n/2 \rfloor$-子集或者 $\lceil n/2 \rceil$-子集才能保证前面的约束条件成立.

***Proof of Statement 1***

充分性显然成立；

必要性由引理 4 推出成立.

***Proof of Statement 2***

在引理 4 的基础上，只需证明 $\mathcal{A}$ 中不能同时存在 $\lfloor n/2 \rfloor$-子集和 $\lceil n/2 \rceil$-子集即可.

$\because$ $n$ 为奇数，记 $m=\lfloor n/2 \rfloor = \lceil n/2 \rceil$

又，记全集 $U$ 的$\lfloor n/2 \rfloor$-子集为 $X_1, X_2, \dots, X_m$，其构成集族 $\mathcal{X}$；$\lceil n/2 \rceil$-子集为 $Y_1, Y_2, \dots, Y_m$，其构成集族 $\mathcal{Y}$.

假设存在反链 $\mathcal{A}$ 的基数为 ${n \choose \lfloor n/2 \rfloor} = {n \choose \lceil n/2 \rceil}$ ，且有 $\mathcal{A} \subseteq \mathcal{X} \cup \mathcal{Y}$, $\mathcal{P}=\mathcal{A} \cap \mathcal{X} \neq \varnothing$, $\mathcal{Q}=\mathcal{A} \cap \mathcal{Y} \neq \varnothing$.

因为 $\mathcal{A}$ 是反链，因此可以推出结论如下：

- $\forall X \in \mathcal{P}, \ \forall Y \in \mathcal{Q},  \  X \nsubseteq Y$

- $\forall X \in \mathcal{X-P}, \ \forall Y \in \mathcal{Y-Q},  \  X \nsubseteq Y$

总的来说，我们有

$$
\forall X \in \mathcal{X},\ \forall Y \in \mathcal{Y}, (X \subseteq Y) \leftrightarrow ((X \in \mathcal{P}\ \wedge \ Y \in \mathcal{Y} -\mathcal{Q}) \ \vee \ (X \in \mathcal{X}-\mathcal{P}\ \wedge \ Y \in \mathcal{Q})) 
\label{i}
\tag{i}
$$

另外，由于 $\mathcal{P},\mathcal{X}-\mathcal{P}$ 非空，选择 $X' \in \mathcal{P}, X^{''} \in \mathcal{X}-\mathcal{P}$. 

记 $C$ 是 $X', X^{''}$的最大公共子集，即 $C= X' \cap X^{''}$. 设 $r= \lvert C \rvert$

于是 $X', X^{''}$ 的剩下的不相交的部分就分别记作 $\{e_1',e_2',e_3' \dots e_{m-r}' \}$ 和 $\{e_1^{''},e_2^{''},e_3^{''} \dots e_{m-r}^{''} \}$

进而，递归地构造 $U$ 的子集列 $\{Z\}$ 如下：

- $Z_0=X'$

- $Z_1=\{e_1^{''}\} \cup Z_0 - \{e_1'\}$

- $Z_2=\{e_2^{''}\} \cup Z_1 - \{e_2'\}$  
  ……

- $Z_{i+1}=\{e_{i+1}^{''}\} \cup Z_i - \{e_{i+1}'\}$  
  ……

- $Z_{m-r}=\{e_{m-r}^{''}\} \cup Z_{m-r-1} - \{e_{m-r}'\}=X^{''}$

**注意到 $X' \in \mathcal{P}, X^{''} \in \mathcal{X}-\mathcal{P}$，于是必定存在 $0 \leq i \leq m-r-1$ ，恰使得 $Z_i \in \mathcal{P}, Z_{i+1} \in \mathcal{X}-\mathcal{P}$.**

构造集合 $Y=Z_i \cup \{e_{i+1}^{''}\}=Z_{i+1} \cup \{e_{i+1}'\}=Z_i \cup Z_{i+1} \in \mathcal{Y}$.

注意到，$Z_i \subseteq Y, \ Z_{i+1} \subseteq Y$ 且 $Z_i \in \mathcal{P}, Z_{i+1} \in \mathcal{X}-\mathcal{P}$ . 于是我们发现无论 $Y \in \mathcal{Q}$ ，还是 $Y \in \mathcal{Y}-\mathcal{Q}$，都与之前推出的结论 $\eqref{i}$ 矛盾. 证毕.

<p align="right">Q.E.D</p>

