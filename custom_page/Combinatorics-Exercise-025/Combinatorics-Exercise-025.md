---
title: Combinatorics Exercise 025
date: 2019-03-31 01:06:26
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
有若干个同学在操场上做游戏，他们彼此的距离都不相等，每个人的手中都有一把水枪，并且每个人都向距离自己最近的人开枪，试证：每人至多中 $5$ 枪.

<!-- more -->
#### *Proof*
不妨假设有人中了不少于 $6$ 枪，称此人为 $A$. 考虑 $A$ 与这 $6$ 个人组成的 $6$ 个夹角（每相邻的两个人与 $A$ 形成一个夹角）——由抽屉原理可知，必定有一个夹角不小于 $60^{\circ}$.

不妨称与 $A$ 形成此夹角的这两个人为 $P$, $Q$，即有 $\angle PAQ \geq 60_{}^{\circ}$；又因为所有人的距离都不相等，所以，在 $\triangle PAQ$ 中，另外的两个角中必有其一是小于 $60_{}^{\circ}$ 的.

而由正弦定理可知，边 $PQ$，也就是 $\angle PAQ$ 所对的边在 $\triangle PAQ$ 中不是最短边.

但，因为 $P$ 和 $Q$ 二人都向 $A$ 开枪，因此 $PQ$ 在 $\triangle PAQ$ 中必须是最短边，产生矛盾.

于是假设不成立，命题得证.

<p align="right">Q.E.D.</p>


