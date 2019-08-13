---
title: Pigeonhole Principle Exercise 037
date: 2019-08-13 15:11:24
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

平面上 $8$ 个点，每两个点之间都连接一条单向有向线段，试证：必存在 $4$ 个点 $A$, $B$, $C$, $D$，其中 $A$ 指向 $B$，$B$ 指向 $C$, $C$ 指向 $D$.

#### *Proof*

$8$ 个点可以确定 $\binom{8}{2}=28$ 条线段，因为有 $28 = 8 \times 3 +4$，由抽屉原理可知，必定有一个点，从该点至少射出 $4$ 条单向线段，不妨记该点为 $A$.

我们不妨考虑被 $A$ 射中的 $4$ 个点，它们之间可以确定 $\binom{4}{2}=6$ 条线段，因为有 $6 = 4 \times 1 +2$，由抽屉原理可知，必定有一个点，从该点至少射出 $2$ 条单向线段，不妨记该点为 $B$.
 
考虑被 $B$ 点射中的两个点，它们之间必定有一者被另一个点所射中，于是记被射中的点为 $D$，发射单向箭头的点为 $C$.

于是，我们就找到了题设中所描述的四个点。

<p align="right">Q.E.D.</p>

