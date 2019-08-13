---
title: Pigeonhole Principle Exercise 048
date: 2019-08-13 21:42:43
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
在 $15 \times 15$ 的方格纸中的每一个小方格任意地写上 $1$ 至 $56$ 中的整数（含端点），试证：一定可以找到四个小方格，它们构成一个方格纸上的平行四边形的四个顶点（包含退化情形），且这个平行四边形的两条对角线各自对应的两对端点之和相等。

#### *Proof*

将方格纸上的小方格用坐标形式表示：$P(i,j)$ 表示第 $i$ 行 第 $j$ 列的方格

我们不妨设 $P(8,8)$ 为对称中心，将其他格子进行如下分划

$$
\{P(1,1),P(15,15)\},\quad \{P(1,2),P(15,14)\}, \quad \dots, \quad\{P(1,15),P(15,1)\}    \\
\{P(2,1),P(14,15)\},\quad \{P(2,2),P(14,14)\}, \quad \dots, \quad\{P(2,15),P(14,1)\}    \\
\dots \quad \dots \quad \dots \quad \dots \\
\{P(7,1),P(9,15)\},\quad \{P(7,2),P(9,14)\}, \quad \dots, \quad\{P(7,15),P(9,1)\}   \\
\{P(8,1),P(8,15)\},\quad \{P(8,2),P(8,14)\}, \quad \dots, \quad\{P(8,7),P(8,9)\}    \\
$$

总之，将剩下的格子都按照 $\{P(i,j),P(16-i,16-j)\}$ 的方式划分等价类，可见每一个等价类中的两个格子的连线中点就是 $P(8,8)$

注意到等价类的数目为 $\frac{15^2-1}{2}=112$，而每个等价类中两个点之和的取值范围是 $2$ 至 $112$ 共 $111$ 种选项，由抽屉原理可知，必定存在两个等价类，它们内部点的数值之和相等——同时，这两个等价类表示的两对点构成一个以 $P(8,8)$ 为中心的平行四边形，从而命题得证。

<p align="right">Q.E.D.</p>


