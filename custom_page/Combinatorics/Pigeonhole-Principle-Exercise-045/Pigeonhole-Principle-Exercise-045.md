---
title: Pigeonhole Principle Exercise 045
date: 2019-08-13 20:54:35
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
在任何一个凸 $2n$ 边形（$n \geq 2$）中，总有一条对角线不与任何一条边平行。

#### *Proof*

首先，我们准备一些在凸多边形中的命题和引理：

引理1
:    在凸多边形中，经过同一个顶点的两条对角线必定不平行。

引理2
:    若在凸多边形中，两条对角线平行，那么这两条对角线的四个定点必定互不相同。

这两个命题其实都非常显然，略证。

引理3
:    对于一个凸 $2n$ 边形，存在一组互不相交的对角线（段），并且任意一组互不相交的对角线段的数目不超过 $2n-2$

下面开始正式的证明：

一个凸 $2n$ 边形共有 $n(2n-3)$ 条对角线，假设命题不成立，即：任何一条对角线，都有一条边与之平行，那么由抽屉原理我们可以得知：

$$
\lceil \frac{n(2n-3)}{2n} \rceil =\lceil \frac{2n-3}{2}\rceil = 2n -1
$$

即存在某一条边，有 $2n-1$ 条对角线与之平行，由引理2可知，这 $2n-1$ 条对角线都是互不相交的，这与引理3 矛盾。

因此，假设不成立，命题得证。

<p align="right">Q.E.D.</p>


