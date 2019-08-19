---
title: Pigeonhole Principle Exercise 060
date: 2019-08-14 15:40:26
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
对正 $27$ 边形的每个顶点进行红蓝二染色，且每两个红色顶点之间必须相隔另外两个顶点，试证：必定存在三个顶点，它们都为蓝色，且可以构成一个正三角形。

#### *Proof*
从题设中不难推知一个事实：一个红色顶点和其最邻近的红色顶点之间必须至少有 $2$ 个蓝色顶点。
为下文叙述方便，我们称两个红色顶点为 “赤邻的”，当且仅当它们之间不存在红色顶点相隔。

我们可以进行分类讨论如下：

1. 每一对赤邻顶点之间都恰好有 $2$ 个蓝色顶点：

    不失其一般性，我们标定顶点 $0$, $3$, $6$, $9$, $12$, $15$, $18$, $21$, $24$ 为红色顶点，那么立马就有 $1$, $10$, $19$ 这三个顶点符合欲证命题的要求。

2. 存在某对赤邻顶点，使得它们之间的蓝色顶点数目大于 $2$

    那么我们可知，蓝色顶点的数目至少是 $19$

    另一方面我们将正 $27$ 边形的顶点作如下分划：

    $$
    \{0, 9, 18\}\\
    \{1, 10, 19\}\\
    \{2, 11, 20\}\\
    \{3, 12, 21\}\\
    \{4, 13, 22\}\\
    \{5, 14, 23\}\\
    \{6, 15, 24\}\\
    \{7, 16, 25\}\\
    \{8, 17, 26\}\\
    $$
    
    每一个等价类都构成一个正三角形的三个顶点，共有 $9$ 个等价类，而其中蓝色顶点的数目不小于 $19$, 由抽屉原理可知，至少有 $\lceil \frac{19}{9} \rceil =3$ 个蓝色顶点同属一个等价类，于是欲证命题成立。

综合可知，命题得证。

<p align="right">Q.E.D.</p>