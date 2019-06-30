---
title: Combinatorics Exercise 032
date: 2019-04-18 00:50:46
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
设 $A=\{1, 2, 3, \cdots, 25\}$，若某个集合由 $A$ 中的五个不同的元素组成，则称其为 $A$ 的一个 “五元集”，试证：至多可以有 $A$ 的 $30$ 个五元集，使得其中任意两个五元集的交集至多只有一个数.

<!-- more -->

#### *Proof*
假设这样的五元集不止 $30$ 个，也即至少有 $31$ 个五元集，使得其中任意两个五元集的交集至多只有一个元素；

这 $31$ 个集合一共出现了 $31 \times 5 =155$ 个·次 的元素，而 $A$ 只有 $25$ 个元素，从而必然有一个元素，出现了至少 $\lceil \frac{155}{25} \rceil=7$ 次；那么这个元素所在的 $7$ 个五元集除了该元素本身之外，两两之间再无相交元素，从而除了该元素外，它们必定包含另外 $4 \times 7 =28 > 24$ 个互异的元素，这与 $A$ 只有 $25$ 个元素矛盾.

从而命题得证.
<p align="right">Q.E.D.</p>
