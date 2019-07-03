---
title: Pigeonhole Principle Exercise 030
date: 2019-04-08 22:28:18
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
设平面上有 $1980$ 个点，任意两个点之间的距离大于 $\sqrt{2}$，试证明：其中存在 $220$ 个点，它们两两之间的距离不小于 $2$.
<!-- more -->

#### *Proof*
考虑在平面上建立直角坐标系，并且在两条坐标轴上的每一个整点处作垂线，将整个平面划分为边长为 $1$ 的格网.若网格的四个顶点坐标为$(i,j)$, $(i,j+1)$, $(i+1,j)$, $(i+1,j+1)$，则记这个网格的坐标为 $(i,j)$.

按以下方式给每一个网格 $(i,j)$ 赋上 $0$ - $8$ 的编号 $f(i,j)=3 \times (j\mod 3)+ (i \mod 3)$，此时题设中平面上的所有点都恰好位于某个网格中（含边界），且一个网格中至多只有一个点，否则它们的距离必定不大于 $\sqrt{2}$，产生矛盾.

由抽屉原理可知，至少有 $\lceil \frac{1980}{9} \rceil =220$ 个点，它们位于相同编号的网格中；而任意两个编号相同的网格中各取一个点，其之间最短距离不小于 $2$，从而这些点两两之间的距离不小于 $2$.

命题得证.
<p align="right">Q.E.D.</p>


