---
title: Pigeonhole Principle Exercise 047
date: 2019-08-13 21:41:08
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
凸四边形 $ABCD$ 的每条边长度都小于 $24$, 设点 $P$ 是其内部的任意一点，试证：总有一个顶点与 $P$ 的距离小于 $17$.

#### *Proof*
我们来证明其逆否命题。

假设 $P$ 与 $A$, $B$, $C$, $D$ 四个点的距离都大于等于 $17$, 注意到 $P$ 是其内部的任意一点，因此，$\angle APB$, $\angle BPC$, $\angle CPD$, $\angle DPA$ 中必定有一者不小于 $90^\circ$.

不失其一般性，我们假设就是 $\angle APB \geq 90^\circ$,

那么，由简单的三角学知识我们知道

$$
\lvert AB \rvert \geq \min(\lvert PA \rvert, \lvert BP \rvert) \cdot \sqrt{2} \geq 17 \times \sqrt2 > 24
$$

从而这个凸四边形必定存在一条长度大于 $24$ 的边。

于是命题得证。

<p align="right">Q.E.D.</p>
