---
title: Pigeonhole Principle Exercise 055
date: 2019-08-13 21:47:48
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
能否在边长 $2\sqrt2 +1$ 的正方形中放置 $17$ 个半径为 $\frac12$ 的圆，使得任意两个圆都外离？

#### *Proof*
答案是 **不能**

注意到，正方形的四个角落实际上是圆无法覆盖到的地方（画一下就知道什么意思了），因此考虑圆心的实际可出现范围，实际上是一个与原正方形中心重合，边长缩小为 $2\sqrt2$ 的小正方形。

我们将这个小正方形分解为 $16$ 个边长为 $\frac{\sqrt2}{2}$ 的方格，于是抽屉原理告诉我们，这 $17$ 个圆的圆心中必定有至少两个处于同一个方格中，而同一方格内两个点的距离上限是 $\frac{\sqrt2}{2} \times \sqrt2 =1$. 我们知道圆的半径是 $\frac12$, 因此这两个圆心所代表的圆无法外离。

命题得证。

<p align="right">Q.E.D.</p>

