---
title: Pigeonhole Principle Exercise 054
date: 2019-08-13 21:47:26
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
在面积为 $3$ 的区域内放 $6$ 个面积为 $1$ 的图形，试证：必有两个图形的交集不小于 $\frac15$.

#### *Proof*

由容斥原理配合放缩我们可以知道，这些图形重叠部分的面积 $S_c$ 不大于两两图形重叠面积之和 $S_d$；

另外，由于面积为 $3$ 的区域容纳了总面积为 $6$ 的图形，因此我们可以得知，$6-3 =3 \leq S_c$, 从而 $S_d \geq 3$.

而 $6$ 个图形的重叠部分数目最多为 $\binom{6}{2}=15$, 因此即使考虑极端情形，也必有两个图形的交集不小于 $\frac{3}{15}=\frac15$.

<p align="right">Q.E.D.</p>
