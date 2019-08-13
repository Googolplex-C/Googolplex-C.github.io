---
title: Pigeonhole Principle Exercise 051
date: 2019-08-13 21:46:54
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

#### Title
设整数 $a$ 与 $2$ 和 $5$ 均互质，试证：对于任意正整数 $n$，总存在 $a$ 的一个方幂以 $\underbrace{00\dots 01}_{n\ digits}$ 结尾。

#### *Proof*

首先需要辨析的一点是，$\underbrace{00\dots 01}_{n\ digits}$ 前面是否还需要由数字？笔者认为应该是需要的，如果按照这种方式去理解题意，证明过程会相对复杂一些。

为方便起见设 $m = 10^n$, 由整数的阿基米德性质可知，必定存在一个方幂 $p$ 使得 $a^p > m$.

另外，由初等数论的知识我们可以得知，**$a$ 的任意正整数次幂都和 $10$ 的任意正整数次幂互质**。

考虑长度为 $m-1$ 的序列 

$$
a^p, a^{2p}, a^{3p}, \cdots, a^{(m-1)p}
$$

在模 $m$ 意义下的余。

首先，序列的任意一项都不可能余 $0$.

1. 若序列中存在某项模 $m$ 余 $1$, 则欲证命题自动成立。

2. 若序列中不存在某项模 $m$ 余 $1$，则这 $m-1$ 项在模 $m$ 意义下的余数取值可选数目为 $m-2$，由抽屉原理可知，必定存在两项 $a^{ip}$ 和 $a^{jp}$ 模 $m$ 同余（假设 $i > j$）

    于是，我们有

    $$
    a^{ip} \equiv a^{jp} \mod m \\
    \Rightarrow (a^{ip} - a^{jp}) \equiv 0 \mod m \\
    \Rightarrow a^{jp}(a^{(i-j)p}-1) \equiv 0 \mod m \\
    $$
    
    注意，$a^{jp}$ 和 $m$ 互质，因此我们有
    
    $$
    (a^{(i-j)p}-1) \equiv 0 \mod m \\
    a^{(i-j)p} \equiv 1 \mod m
    $$
    
    并且，我们还有 $a^{(i-j)p} > a^p > m$，因此 $a^{(i-j)p}$ 就是符合要求的方幂。

命题得证。

<p align="right">Q.E.D.</p>
