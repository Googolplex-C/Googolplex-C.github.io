---
title: 计数组合学的记号和基本概念
date: 2019-10-03 20:17:37
author: Googolplex-C
url: 
img: 
top: 
cover: 
coverImg: 
password: 
toc: 
  depth_from: 2
  depth_to: 5
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

<center><font size=7><b>计数组合学的记号和基本概念</b></font></center>

# 
$$\begin{aligned}Author&: \mathsf{Googolplex\ C} \\ Originality&: \mathsf{Level\quad 3}\end{aligned}$$

# 
<center><font size=5><b>Abstract</font></b></center>

# 
本文是计数组合学的入门内容的介绍性文章。第一部分主要是较为空泛的总结：首先大致介绍了组合学是做什么的，主要有哪些分支。其次介绍了计数组合学——作为组合学中可能是最具代表性的分支，主要关注哪些内容。之后是笔者对于自己所接触到的组合学的工具和方法简要地进行概述。第二部分开始具体地梳理计数组合中的具体内容，从集合出发，进而以代数的方式（即暂不涉及它们的组合含义）定义一系列在组合学中经常使用的记号和概念。


---

## 从集合说起
### 基本的记号与定义

###### 集合

定义 1：集合
:    参见公理集合论中的 ZF 公理；某种程度上，集合的概念是自明的。

###### 某些特定的集合记号

- $\mathbb{N}$：全体自然数（包含 0）构成的集合；
- $\mathbb{Z}$：全体整数构成的集合；
- $\mathbb{Q}$：全体有理数构成的集合；
- $\mathbb{R}$：全体实数构成的集合；
- $\mathbb{C}$：全体复数构成的集合；

注意到，表示数系的字母字体不是一般的 LaTeX 字体。对于以上的数系集合，我们可以在其右上角添加上一些上标修正其含义：
- 上标 $*$：表示原集合删去 0 得到的新集合；
- 上标 $+$：表示选取原集合中的正数得到的新集合；

示例
:    - $\mathbb{N}^*$ 和 $\mathbb{N}^+$ 都表示正整数集合；
    - $\mathbb{Q}^*$ 表示除了 0 之外的所有有理数的集合；

另外在组合学中，还会经常性地出现以下集合记号：
- $[n]$：表示前 $n$ 个正整数构成的集合，即 $[n]:=\{1, 2, \dots, n\}$

###### 关于集合的运算和指标


定义 2：集合的势（基数）
:    表示集合元素多寡的指标。
:    对于有限集合，其基数就是元素的个数（以某个自然数表示）；对于无限集合，其基数与之形成一一映射的集合的相等。
:    **记法**：集合 $A$ 的基数记为 $\lvert A \rvert$，或者记为 $\operatorname{card}A$，或者记为 $\#A$

定义 3：集合的基本运算
:    1. 并： $A \cup B := \{x \mid x \in A \text{ or } x \in B\}$
        - 注：此处的 or 是 inclusive or.
:    2. 交： $A \cap B := \{x \mid x \in A \text{ and } x \in B\}$
:    3. 差： $A \setminus B := \{x \mid x \in A \text{ and } x \notin B\}$
:    4. 补：若 $B \subseteq A$，则有 $\complement_A B := A \setminus B$
        - 注：补运算其实就是差运算的特例
        - 注：在 $A$ 明确的前提下，补集 $\complement_A B $ 也可以写为 $\overline{B}$， 或者 $B^{\complement}$，或者 $\complement B$

定义 4：集族
:    元素为集合的集合可以成为一个集族。

关于 “族”，“系” 的概念，存在着一些不同的用法，有的和类型论里的用法混在一起，叫人难以分辨，在这里姑且把它定义如上。按照上面的定义，**集族本身其实仍是个集合**。

定义 5：幂集
:    一个集合所有的子集（包括空集在内）所构成的集族成为幂集。
:    **记法**：集合 $A$ 的幂集记为 $\mathcal{P}(A)$ 或者 $\mathfrak{P}(A)$，也可以记为 $2^A$

定义 6：笛卡尔积
:    给定 $n$ 个集合 $A_1$, $A_2$, $\cdots$, $A_n$，它们的笛卡尔积是由所有如下定义的 $n$ 元组
    $$
    (a_1, a_2, \cdots, a_n), \quad\quad \text{where}\quad \forall i \in [n], a_i \in A_i
    $$
    构成的集合。
:    **记法**：$n$ 个集合 $A_1$, $A_2$, $\cdots$, $A_n$ 的笛卡尔积记为：$A_1 \times A_2 \times \cdots \times A_n$， 或者简记为 $A_1A_2\cdots A_n$

定义 7：元组的投影
:    对于给定的 $n$ 元组 $(a_1, a_2, \cdots, a_n) \in A_1A_2\cdots A_n$ ,称其第 $i$ 个分量 $a_i$ 是该 $n$ 元组在 $A_i$ 上的投影
:    **记法**：对于 $n$ 元组 $a\in A_1A_2\cdots A_n$，其在 $A_i$ 上的投影记为 $\operatorname{pr}_i(a)$

定义 8：集合的幂
:    集合 $A$ 的 $n$ 次幂记为 $A^n := \underbrace{A \times A \times \cdots \times A}_{n\cdot A}$

定义 9：幂的对角线
:    对于集合幂 $A^n$，其对角线 $\Delta$ 是由各分量都相同所有的 $n$ 元组构成的集合

示例
:    设 $A=\{1, 2, 3\}$，那么 $A^3$ 的对角线就是 $\{(1,1,1),(2,2,2),(3,3,3)\}$

### 相关定理与命题

###### 笛卡尔积的基数
定理 1
:    对于若干个有限集合的笛卡尔积 $A_1A_2\cdots A_n$，其基数为 $\lvert A_1 \rvert \lvert A_2 \rvert \cdots \lvert A_n \rvert$

论证
:    笛卡尔积的基数实际上就是 $n$ 元组的个数。注意到每个元组的各个分量都是相互独立的，因此第一个分量有 $\lvert A_1 \rvert$ 种选择，第二个分量有 $A_2$ 种选择……以此类推，其基数为 $\lvert A_1 \rvert \lvert A_2 \rvert \cdots \lvert A_n \rvert$。

<p align="right">Q.E.D.</p>


注：其实笛卡尔积的基数公式正是组合学中乘法原理的体现及形式化表述。

###### 幂集的基数
定理 2
:    设集合 $A$ 的基数为 $\lvert A \rvert = n$，则 $A$ 的幂集的基数为 $2^n$
    
论证
:    考虑 $n$ 个元素中的任意一个，其在一个子集中可能出现，也可能不出现；所有的 $n$ 个元素是否出现在某个子集中是相互独立的，因此由乘法原理可知，所有可能的子集的数目为 $2^n$.

<p align="right">Q.E.D.</p>


## 映射与关系
### 映射

###### 映射的基本概念
定义 10：映射
:    这里不具体地写出映射的定义，只举出关于映射定义的一些要点
:    1. 映射是从一个集合到另一个集合的*数学实体*，这两个集合**可以相等**；
     2. **记法**：从集合 $A$ 到集合 $B$ 的映射记为 $f:A \mapsto B$；前者称为函数的定义域，后者称为函数的陪域，或者称为到达域、上域、目标集；
     3. 对于定义域中的任意一个元素，在陪域中**有且仅有一个**元素，由映射选定与前者对应
     4. 对于定义域中的**每一个**元素，在陪域中有且仅有一个元素，由映射选定与前者对应
        - 注意：第 3、4 点的语义焦点所强调的重点是不同的，两方面都要注意到
     5. 映射 $f:A \mapsto B$ 的值域定义为 $f(A):= \{y\in B \mid \exists\ x \in A, \mathrm{s.t.}\ y = f(x)\}$
     6. 因此，值域与像集的关系是 $f(A) \subseteq B$；当且仅当在 $f$ 是满射的时候，$f(A)=B$ 才成立

概念 11：映射的分类
:    1. 单射
     2. 满射
     3. 非单射也非满射
        - 映射可以既是单射，也是满射，此时称之为双射
     
:    为了后文的叙述方便，笔者定义一些自定义的概念
    - **纯单射**：是单射但不是满射的映射
    - **纯满射**：是满射但不是单射的映射

关于映射的分类，老生常谈了，此处不予赘述

概念 12：映射的复合
:    同样地，笔者不想再照本宣科地重新写一遍复合映射的定义，只列出一些需要注意的要点；
:    1. **复合映射本质上仍然是映射**，重要的事情说三遍
     2. 在概念的定义上麻烦的地方在于，不同的教材或者资料对于一个细节的叙述不太一致（数学界比较麻烦的一点）
        - 有的资料对于复合映射 $g\,\circ\,f$ 的 “中间集合” 是这样要求的：映射 $g$ 的定义域必须等于 $f$ 的陪域
        ```viz{align=center}
        digraph G{
          graph[rankdir=LR,label="两个函数 f 和 g 各自的定义域和陪域"]
          subgraph cluster{
            graph[label="domain of  ' f '"]
            node[shape=circle,width=0.1]
            a[label=a]
            b[label=b]
            c[label=c]
            d[label=d]
          }
          subgraph cluster_2{
            graph[label="codomain of  ' f '"]
            node[shape=circle,width=0.1]
            e[label=e]
            f[label=f]
            g[label=g]
            h[label=h]
            i[label=i]
          }
          subgraph cluster_3{
            graph[label="domain of  ' g '"]
            node[shape=circle,width=0.1]
            e2[label=e]
            f2[label=f]
            g2[label=g]
            h2[label=h]
            i2[label=i]
          }
          subgraph cluster_4{
            graph[label="codomain of  ' g '"]
            node[shape=circle,width=0.1]
            j[label=j]
            k[label=k]
            l[label=l]
            m[label=m]
            o[label=o]
            p[label=p]
          }
        
          a -> e
          b -> g
          c -> h
          d -> g

          e2 -> j
          f2 -> l
          g2 -> p
          h2 -> p
          i2 -> m

          edge[style=invis,label="         "]
          e -> e2
          f -> f2
          g -> g2
          h -> h2
          i -> i2
        }
        ```

        ```viz{align=center}
        digraph G{
          graph[rankdir=LR,label="两个函数 f 和 g 复合后"]
          subgraph cluster{
            graph[label="domain of  ' f '"]
            node[shape=circle,width=0.1]
            a[label=a]
            b[label=b]
            c[label=c]
            d[label=d]
          }
          subgraph cluster_2{
            graph[label="codomain of  ' f ' \nas well as\n domain of  ' g '"]
            node[shape=circle,width=0.1]
            e[label=e]
            f[label=f]
            g[label=g]
            h[label=h]
            i[label=i]
          }
          subgraph cluster_4{
            graph[label="codomain of  ' g '"]
            node[shape=circle,width=0.1]
            j[label=j]
            k[label=k]
            l[label=l]
            m[label=m]
            o[label=o]
            p[label=p]
          }
        
          a -> e
          b -> g
          c -> h
          d -> g

          e -> j
          f -> l
          g -> p
          h -> p
          i -> m
        }
        ```

        - 有的资料的要求稍微宽松一些：映射 $g$ 的定义域只须包含于 $f$ 的陪域
        ```viz{align=center}
        digraph G{
          graph[rankdir=LR,label="两个函数 f 和 g 各自的定义域和陪域"]
          subgraph cluster{
            graph[label="domain of  ' f '"]
            node[shape=circle,width=0.1]
            a[label=a]
            b[label=b]
            c[label=c]
            d[label=d]
          }
          subgraph cluster_2{
            graph[label="codomain of  ' f '"]
            node[shape=circle,width=0.1]
            e[label=e]
            f[label=f]
            g[label=g]
            h[label=h]
            i[label=i]
          }
          subgraph cluster_3{
            graph[label="domain of  ' g '"]
            node[shape=circle,width=0.1]
            e2[label=e]
            f2[label=f]
            g2[label=g]
            i2[label=i]
          }
          subgraph cluster_4{
            graph[label="codomain of  ' g '"]
            node[shape=circle,width=0.1]
            j[label=j]
            k[label=k]
            l[label=l]
            m[label=m]
            o[label=o]
            p[label=p]
          }
        
          a -> e
          b -> g
          c -> h
          d -> g

          e2 -> j
          f2 -> l
          g2 -> p
          i2 -> m

          edge[style=invis,label="         "]
          e -> e2
          f -> f2
          g -> g2
          i -> i2
        }
        ```

        ```viz{align=center}
        digraph G{
          graph[rankdir=LR,label="两个函数 f 和 g 复合后"]
          subgraph cluster{
            graph[label="domain of  ' f '"]
            node[shape=circle,width=0.1]
            a[label=a]
            b[label=b]
            c[label=c]
            d[label=d]
          }
          subgraph cluster_2{
            graph[label="codomain of  ' f ' \nas well as\n domain of  ' g '"]
            node[shape=circle,width=0.1]
            e[label=e]
            f[label=f]
            g[label=g]
            h[label=h]
            i[label=i]
          }
          subgraph cluster_4{
            graph[label="codomain of  ' g '"]
            node[shape=circle,width=0.1]
            j[label=j]
            k[label=k]
            l[label=l]
            m[label=m]
            o[label=o]
            p[label=p]
          }
        
          a -> e
          b -> g
          c -> h
          d -> g

          e -> j
          f -> l
          g -> p
          i -> m
        }
        ```

        - 当然，如果反过来这样要求：只需令映射 $f$ 的陪域只须包含于 $g$ 的定义域即可；那么复合操作就不是 well-defined 的了。（此处不展示示意图，为什么请读者自证）
        - 关于中间集合的底线约束是：**$f$ 的值域起码必须包含于 $g$ 的定义域中**

###### 映射与基数、映射的逆

定义 13：集合之等势
:    称两个集合（不管是不是有限集合）是等势的，当且仅当它们之间**存在**一个双射

Note
:    请注意，在*定义 13* 中，我们的表述是 “存在一个双射”，这里有个小小的问题：
:    对于两个有限集合而言，如果它们之间存在一个双射，那么它们之间就不存在纯单射或者纯满射，也就是说，在这两个集合之间的映射要么是双射，要么是非单非满映射
:    但是对于两个无限集合而言，事情就不一样了，它们之间在存在双射的前提之下，也可以存在纯单射或者纯满射
:    那么在无限集合和有限集合之间情况又会怎么样呢？如果你思考了很久没有想出答案，我建议你点击右上角关闭本页面，先去学习一下更基础的知识或者放松一下身心

定义 14：嵌入映射
:    设 $A_0$ 是 $A$ 的子集，定义 $A_0$ 到 $A$ 的映射 $i:A_0\mapsto A$ 使得 $$\forall\, x \in A_0,\quad i(x)=x$$ 称 $i$ 为 $A_0$ 到 $A$ 的嵌入映射

定义 15：恒等映射
:    从某个集合自身出发映射到自身的嵌入映射称之为该集合上的恒等映射

Note
:    说白了，恒等映射就是元素映射到自己的映射，且它显然是个双射。

定义 16：逆映射
:    对于一个映射 $f:A\mapsto B$，若存在一个映射 $g:B \mapsto A$，使得 $g \circ f$ 为 $f$ 上的恒等映射，那么称 $g$ 是 $f$ 的逆映射
:    **记法**：映射 $f$ 的逆映射记为 $f^{-1}$

定理 3：逆映射与双射
:    某个函数存在逆映射，当且仅当这个映射是双射

Note
:    上面的定理证明就略过吧，因为它繁而不难。但是笔者还是想提供一些直观上的论述（画个草图就理解了）：
:    1. 若某个函数是纯单射，那么我们强行定义出来的它的 “逆映射” 就不满足*定义 10* 中的要点4；
     2. 若某个函数是纯满射，那么我们强行定义出来的它的 “逆映射” 就不满足*定义 10* 中的要点3；
     3. 若某个函数是非单非满映射，那么强行定义出来的它的 “逆映射” 将同时不满足要点3 和要点 4；


逆映射、复合映射与单满双射这些概念之间，存在有相当多时不时会用上的命题和定理，尽管要证明它们需要绕一些弯，但是大多数都是繁而不难的证明。因此，笔者就直接省略这些命题以及它们的证明吧。

### 关系
###### 关系的基本概念
定义 17：关系
:    定义在 $n$ 个集合 $A_1$, $A_2$, $\cdots$, $A_n$ 之间的 $n$ 元关系是它们的笛卡尔积 $A_1 \times A_2 \times \cdots \times A_n$ 上的子集。
:    称 $n$ 元组 $(a_1, a_2, \cdots, a_n)$ 满足关系 $R$，当且仅当 $(a_1,a_2,\cdots,a_n) \in R \subseteq A_1 \times A_2 \times \cdots \times A_n$

Note
:    “关系” 这个概念的定义看上去好像有点陌生，其实从另一个角度来看可以理解成（形式逻辑）中 “谓词” 这一概念的推广，或者说另一种解读方式。这样一来，前者就容易理解多了，谓词（不管是一元还是多元）对于其谓词变量输入给出的要么是真，要么是假；而在关系中，一组有序的元素要么满足给定的 $n$ 元关系，要么不满足此关系；
:    关系这个定义值得注意之处在于，它用集合论的语言定义了 “谓词” 这个概念——后者在朴素集合论或者面向中学生的朴素的形式逻辑学中往往被表述为 “具有某种性质”——这么表述往往是带有模糊性的

当有 $A_1 = A_2 = \cdots = A_n = A$ 时，我们称它们之间的 $n$ 元关系为：$A$ 上的 $n$ 元关系。

我们最关心的是 $A$ 上的二元关系！

概念 18：特定的二元关系性质
:    **自反性**
:    **对称性**
:    **传递性**
:    **完全性**
:    它们的含义也是老生常谈了，此处略

定义 19：逆关系
:    对于已有的关系 $R$，定义其逆关系 $R^{-1}$ 如下
    $$x\,R\,y \Leftrightarrow y\,R^{-1}\,x$$

定义 20：关联矩阵（ 0-1 矩阵）
:    对于某个非空有限集合 $A$ 上的二元关系，我们可以定义这样一个矩阵 $[r_{ij}]$ 来直观地描述此二元关系
     $$r_{ij}=\begin{cases}
     1 \qquad \text{if } a_i\,R\,a_j \\
     0 \qquad \text{if } a_i\,\not R\,a_j \\
     \end{cases}
     $$

定义 21：截线
:    设集合 $A$ 上定义了二元关系 $R$，并有 $x \in A$
:    沿元素 $x$ 的 $R$ 的第一截线定义为：$\langle x\mid R\rangle:=\{y\mid x\,R\,y\}$  
    沿元素 $x$ 的 $R$ 的第二截线定义为：$\langle R\mid x\rangle:=\{y\mid y\,R\,x\}$  

## 组合学的符号和基本概念

现在我们开始正式地引入组合学中常见的符号和基本概念。  
请注意，在这里我们对于这些符号的定义是在 algebraic sense 层面上的，而**暂时不涉及其具体的组合意义**。对于涉及到这些基本记号的某些命题，采用最初等的、最直观可信的代数方法进行论证。
### （形式的）各种记号
定义 22：降阶乘
:    $$(x)_k:=\prod^{k}_{i=1}\,(x-i+1) \qquad \text{where }\ x \in \mathbb{C},\ k \in \mathbb{N}$$ 称为 $x$ 的 $k$ 次降阶乘

Note
:    **其他记法**：$$x^{\underline{k}}$$
:    1. 如果我们把降阶乘看做是 $x$ 和 $k$ 的二元函数，那么不妨注意降阶乘的定义范围！  
        **$x$ 可以是个复数（这个定义范围够大了吧），但 $k$ 必须是个非负整数！**
:    2. “阶乘” 这个东西和 $\Gamma$ 函数有很大的关系，但是笔者分析学真的学得很浅很差，因此此处稍提及一下；
:    3. 注意：$i$ 作为下标是从 $1$ 开始的；从而我们有：**$(n)_0 = 1$**，更进一步地有 $(0)_0 =1$
:    4. 尽管 $x$ 的范围可以是复数，但是在组合学中，$x$ 在实际上**常常取非负整数**；此时字母习惯上换成 $n$，也即有：
     $$(n)_k:=\prod^{k}_{i=1}\,(n-i+1) \qquad \text{where }\ n,\ k \in \mathbb{N}$$
:    5. 当 $n$, $k$ 都是非负整数时，若 $n < k$，则有 $(n)_k = 0$

定义 23：阶乘
:    $$n!:=(n)_n$$

定义 24：升阶乘
:    $$x^{(k)}:=\prod^{k}_{i=1}\,(x+i-1) \qquad \text{where }\ x \in \mathbb{C},\ k \in \mathbb{N}$$ 称为 $x$ 的 $k$ 次升阶乘

Note
:    **其他记法**：$$x^{\overline{k}}$$
:    1. 同样地，注意降阶乘的定义范围！  
        **$x$ 可以是个复数，但 $k$ 必须是个非负整数！**
:    2. 注意：$i$ 作为下标是从 $1$ 开始的；从而我们有：**$x^{\overline{0}}= 1$**
:    3. 尽管 $x$ 的范围可以是复数，但是在组合学中，$x$ 在实际上**常常取非负整数**；此时字母习惯上换成 $n$，也即有：
     $$n^{(k)}:=\prod^{k}_{i=1}\,(n+i-1) \qquad \text{where }\ n,\ k \in \mathbb{N}$$

记号 25
:    $$\binom{x}{y}:=\begin{cases} \frac{(x)_y}{y!} \qquad \text{if }\,x \in \mathbb{C},y \in \mathbb{N} \\ 0 \qquad \text{if }\,x \in \mathbb{C},y \notin \mathbb{N}\end{cases}$$

Note
:    **其他记法**：*记号 25* 有许多其他记法，比如：
     $$C^{y}_{x}, \quad C(n,k), \quad C^{x}_{y}$$
:    请注意我们用了降阶乘对其进行了定义，而不是按照这样的方式来定义：$\binom{x}{y}:=\frac{x!}{y!(x-y)!}$。后者在 $y > x$ 时不再是良定义的。

记号 26
:    $$\left(\!\!\!\binom{x}{y}\!\!\!\right):=\begin{cases} \frac{x^{(y)}}{y!} \qquad \text{if }\,x \in \mathbb{C},y \in \mathbb{N} \\ 0 \qquad \text{if }\,x \in \mathbb{C},y \notin \mathbb{N}\end{cases}$$

记号 27
:    $$\binom{x}{y_1\ y_2\ \cdots\ y_k}:=\begin{cases} \frac{(x)_{y_1+y_2+\cdots+y_k}}{y_1!\,y_2!\,\cdots\,y_k!} \qquad \text{if }\,x \in \mathbb{C},y \in \mathbb{N} \\ 0 \qquad \text{if }\,x \in \mathbb{C},y \notin \mathbb{N}\end{cases}$$

Note
:    1. 不难看出，*记号 27* 是*记号 25* 的推广；
:    2. 当 $x$ 为非负整数，且 $y_1+y_2+\cdots+y_k=x$ 时，我们有 
     $$\binom{x}{y_1\ y_2\ \cdots\ y_k} = \frac{x!}{y_1!\,y_2!\,\cdots\,y_k!}$$

记号 28 (version 1)
:    $$\binom{x}{y}_q:=
     \begin{cases}
     1 \qquad \text{if } k=0 \\
     0 \qquad \text{if } k>n \\
     \frac{(q^n-1)(q^n-q)\cdots(q^n-q^{k-1})}{(q^k-1)(q^k-q)\cdots(q^k-q^{k-1})} \qquad \text{if } 0<k\leq n
     \end{cases}
     \qquad \text{where } \quad n,k \in \mathbb{N},\ q \neq 1 
     $$


记号 28 (version 2)
:    $$\binom{x}{y}_q:=
     \begin{cases}
     1 \qquad \text{if } k=0 \\
     0 \qquad \text{if } k>n \\
     \frac{\prod_{j=1}^{k}\sum_{i=0}^{n-j}q^i}{\prod_{j=0}^{k-1}\sum_{i=0}^{j}q^i} \qquad \text{if } 0<k\leq n
     \end{cases}
     \qquad \text{where } \quad n,k \in \mathbb{N}
     $$

Note
:    这两个记号是等价的定义。前者的分子分母同时通过 $n$ 次方差公式可以转化为后者的形式。
:    注意，这两个版本的记号（若把它们视为函数），定义域有些不一样：前者要求 $q \neq 1$，后者没有这个限制；
:    *记号 28* 也是*记号 25* 的推广：
     - version 1 中令 $q \rightarrow 1$ 可得到*记号 25* 的形式；
     - version 2 中令 $q = 1$ 可直接得到*记号 25* 的形式；

### 计数组合中常见的概念补充

定义 29：置换
:    非空集合到自身的双射又称为**置换**

###### 重集的相关概念
定义 30：重集
:    对于某个集合 $A$，形式地定义其重集为 $(A, m)$，其中 $m:A \mapsto \mathbb{N}^+\cup\{\infty\}$ 是个映射到正整数集的函数。
:    若 $A$ 是有限集，并可以表示为 $A = \{a_1, a_2, \cdots, a_n\}$，则重集 $(A,m)$ 可表示为 $\{a_1^{m(a_1)}, a_2^{m(a_2)}, \cdots, a_n^{m(a_n)}\}$
:    称 $A$ 是 $(A,m)$ 的基础集（underlying set）

Note
:    如果映射将每个元素都映射到自然数 $1$，那么重集就退化为普通的集合

# 
---

<center><font size=5><b>原创性与版权声明</font></b></center>

# 
- **Level 0**：核心内容完全原创，没有借鉴或参考其他文献和材料，但有可能不是第一次提出；
- **Level 1**：核心内容基本原创，借鉴或参考了其他的文献和材料；
- **Level 2**：核心内容部分原创，原创部分与非原创部分相互糅合；
- **Level 3**：对已有文献和材料的整理归纳或者重新组织，可能具有少量原创内容
- **Level 4**：转载 / 搬运，基本不改变已有材料的组织架构与具体内容，但可能附带极少量原创内容

注：Level 0 多见于由笔者独立解决的习题或者开放性问题；Level 1 多见于多种解法的习题或者前人已有一定结论的问题；Level 3 多见于笔记。

# 
<center><font color=red><b>本站所有文章，不论其原创性等级高低，一律不允许转载引用</b></font></center>

# 
---
<center><b>如果您觉得这篇文章有帮助，不妨为我打赏，谢谢！</b></center>

# 
<center>
<img src="../../../../themes/hexo-theme-matery-master/source/medias/reward/alipay.jpg" width="20%" height="20%">
</center>

# 
# 
# 