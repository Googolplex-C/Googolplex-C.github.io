---
title: Combinatorics Exercise 027
date: 2019-04-03 18:16:54
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
在 $8 \times 8$ 方格纸的每个格子里填上互异的整数，试证：存在两个邻格（有公共边的格子），这两个格子里的整数的差的绝对值不小于 $5$.

<!-- more -->

#### *Proof*
对于两个格子 $(x_1,y_1)$ 和 $(x_2,y_2)$，定义它们之间的 “简单路径” 为 
$$
(x_1,y_1)\rightarrow (x_2,y_1) \rightarrow (x_2,y_2)
$$
显然，任何两个格子之间都存在简单路径，且沿简单路径途中的每一步都位于邻格之间.

不妨设最大数为 $a_0$，最小数为 $a_n$，从前者到后者的简单路径上的第 $i$ 个格子记为 $a_i$，并且注意到这 $64$ 个格子的整数互异，因此我们有
$$
63 \leq a_0-a_n=\sum_{i=0}^{n-1}(a_i-a_{i+1}) \leq \sum_{i=0}^{n-1}\lvert a_i-a_{i+1}\rvert
$$
而在方格纸上，简单路径长度的最大值为 $14$，即 $n \leq 14$，因为 $\lceil \frac{63}{14}\rceil=5$，由抽屉原理可知，必定存在某 $i$ 使得 $\lvert a_i-a_{i+1}\rvert \geq 5$，于是命题得证.

<p align="right">Q.E.D.</p>



