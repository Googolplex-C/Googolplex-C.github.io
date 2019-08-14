---
title: Pigeonhole Principle Exercise 058
date: 2019-08-13 21:48:19
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
有两个完全相同的齿轮，其中 $B$ 放在水平面上，$A$ 放在 $B$ 上，使两者的正投影完全重合，然后任意去掉它们的 $4$ 对齿。若$A$, $B$ 均有 $14$ 对齿，试问：能否将 $A$ 绕适当的角度，使得两个齿轮在水平面上的正投影合成一个完整的齿轮？

#### *Proof*

答案是：能。

考虑两个齿轮的正投影无法合成一个完整齿轮的情况：此时必有某一对重合的齿轮，它们刚好都是被挖去的。为方便叙述，我们不妨下一个定义：齿轮 $A$ 的某个特定齿 $B$ 的某个特定的齿重合，且它们都是被挖去的齿，那么称产生了一次 “贯穿”。

注意到，$A$ 和 $B$ 都被挖去了 $4$ 个齿，所以，旋转一周后，一共会产生 $4^2=16$ 次贯穿；这 $16$ 次贯穿将产生在旋转一周过程中两个齿轮的 $14$ 个相对位置中；

但注意到，初始位置自身已经产生了 $4$ 次贯穿，因此，剩下的 $13$ 个相对位置，总共产生 $12$ 次贯穿，由抽屉原理可知，存在某个相对位置，其没有产生任何的贯穿，这种情况下，两个齿轮的正投影就将重合为一个完整的齿轮。

命题得证。

<p align="right">Q.E.D.</p>
