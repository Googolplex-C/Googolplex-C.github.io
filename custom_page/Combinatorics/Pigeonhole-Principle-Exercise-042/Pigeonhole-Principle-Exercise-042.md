---
title: Pigeonhole Principle Exercise 042
date: 2019-08-13 20:08:48
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
能否在 $n \times n\,(n \geq 3)$ 的棋盘上的每个方格上填上数字 $1$, $2$, $3$, 使得该棋盘上的每行、每列、每条对角线上的数字之和互不相同。

#### *Proof*

答案是 **不能**

这个棋盘的行、列、对角线共有 $2n+2$ 条，每条都由 $n$ 个数字构成，而这 $n$ 个数字之和的可能取值下界是 $n$, 上界是 $3n$，共有 $2n+1$ 种可能项；

由抽屉原理可知，必有两组数字，它们的和相等，从而猜想不成立。

<p align="right">Q.E.D.</p>
