---
title: Pigeonhole Principle Exercise 006
date: 2019-02-01 21:04:33
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

平面上有 $25$ 个点，且满足：在任意 $3$ 个点中，存在 $2$ 个点，其距离小于 $1$ . 试证：必定存在这样的 $13$ 个点，使得它们当中任意两个点的距离小于 $2$ . 

<!-- more -->

#### *Proof*

针对命题 “是否存在两个距离大于 $2$ 的点” 进行讨论：

1. 若不存在这样的两个点：  
    也即这 $25$ 个点中任意两个点的距离都小于 $2$ ，于是欲证命题显然成立；

2. 若存在这样的两个点：  
    不妨将其记作 $A$, $B$ ，因为 $\lvert AB \rvert >2 >1$，由题中约束条件可知，对于除此二点之外的 $23$ 个点中的任意一点 $X$，必恰有如下之一情形：

    1. $\lvert AX \rvert < 1$，从而点 $X$ 位于以 $A$ 为圆心，半径为 $1$ 的圆内（不包括圆周本身）
    2. $\lvert BX \rvert < 1$，从而点 $X$ 位于以 $B$ 为圆心，半径为 $1$ 的圆内（不包括圆周本身）

    由抽屉原理可知，存在至少 $12$ 个点分布在以 $A$ ( 或$B$ ) 为圆心，半径为 $1$ 的圆内（不包括圆周本身）. 于是这 $12$ 个点连同圆心一起，构成了满足欲证命题性质的 $13$ 个点，命题成立.  

综上所述，命题成立.

<p align="right"> Q.E.D.</p>

