---
title: Pigeonhole Principle Exercise 035
date: 2019-08-13 14:32:36
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

从 $1$ 至 $138$ 这 $138$ 个整数中任取 $11$ 个互异的整数，试证：在取定的整数中，一定有两个互异的整数，它们的比值 $k$ 满足 $\frac 23 \leq k \leq \frac 32$.

#### *Proof*

将集合 $[128]$ 进行分组：

$$
\{1\},\{2,3\},\{4,5,6\}, \{7,8,9,10\}, \{11,\dots, 16\}, \\
\{17, \dots, 25\}, \{26, \dots, 39\}, \{40, \dots, 60\}, \{61, \dots, 91\}, \{92, \dots, 138\}
$$

这里每一个子集都满足这样的性质，最大数与最小数的比值不超过 $\frac32$. 于是，由抽屉原理可知，取出的 $11$ 个数必定有不少于 $2$ 个位于同一个子集中，这两个数的比值 $k$ 满足 $\frac23 \leq k \leq \frac32$.

<p align="right">Q.E.D.</p>

