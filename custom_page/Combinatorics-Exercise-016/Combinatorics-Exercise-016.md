---
title: Combinatorics Exercise 016
date: 2019-02-23 18:12:36
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

试证：对于任意的正整数 $n$，都存在一个能被 $n$ 整除，且只由数字 $0$ 和 $1$ 构成的自然数.

<!-- more -->

#### *Proof*

构造一个长度为 $n$ 的自然数序列 $\{a_i\}^n_{i=1}$：
$$
a_i=\underbrace{11\cdots1}_{i\text{ 个 }1}\underbrace{0\cdots 0}_{n-i+1\text{ 个 }0}
$$
考虑这个序列模 $n$ 的结果：

1. 存在某个 $a_i$，使得模 $n$ 为 $0$：此数显然使命题成立.

2. 不存在某个 $a_i$，使得模 $n$ 为 $0$：

   那么这 $n$ 个自然数，模 $n$ 的范围是 $[n-1]$，由抽屉原理可知，存在 $i,j \in [n]$，$i <j$，使得 $a_i$ 和 $a_j$ 模 $n$ 同余，那么 $a_j-a_i$ 满足命题的性质.

综合可知，命题成立. 

<p align="right">Q.E.D.</p>

