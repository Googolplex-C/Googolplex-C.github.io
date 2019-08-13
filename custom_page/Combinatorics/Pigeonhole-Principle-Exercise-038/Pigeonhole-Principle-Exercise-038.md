---
title: Pigeonhole Principle Exercise 038
date: 2019-08-13 15:42:27
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
在 $2k \times 2k$ 的格子棋盘上，将 $3k$ 个格子涂黑，剩下的格子都是白色的，试证：可以去掉 $k$ 行 $k$ 列，使得剩下的所有格子都是白色的。

#### *Proof*
我们不妨先以行视角来看这个棋盘，先考虑黑格子个数最多的 **前 $k$ 行**，这 $k$ 行中至少含有 $2k$ 个格子；

假设不然，那么这 $k$ 行中必定有某行的黑格子数目小于等于 $1$，而剩下的 $k$ 行中却含有多于 $k$ 个黑格子，从而剩下的某行中黑格子数目必定大于 $1$，这和我们挑选黑格子个数最多的前 $k$ 行这一操作相矛盾。

将所选中的 $k$ 行去掉；更换为列视角来考察棋盘，此时只剩下至多 $3k-2k=k$ 个黑格子，从而这些剩下的黑格子分布在至多 $k$ 列上，我们继续将这些列去掉即可（如果剩下的黑格子所分布的列的数目不足 $k$，那么我们去掉这些列之后，已经使得棋盘上没有黑格子了，此时再随便去掉若干列即可）。

于是命题得证。

<p align="right">Q.E.D.</p>

