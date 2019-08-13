---
title: Pigeonhole Principle Exercise 044
date: 2019-08-13 20:31:51
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

将一段圆周分成 $36$ 段，分别用 $1$, $2$, $\dots$, $36$ 对每一段圆弧唯一地标号，试证：无论如何标号，总存在相邻接的 $3$ 段圆弧，它们的标号之和至少是 $56$.

#### *Proof*
记这 $36$ 段圆弧上的标号为 $a_1$, $a_2$, $\dots$, $a_{36}$, 那么相邻接的 $3$ 段圆弧标号之和就表示为

$$
a_1+a_2+a_3, a_2+a_3+a_4, \dots, a_{36}+a_1+a_2
$$

它们的总和为 $[(1+36) \times 36 \div 2] \times 3 = 36 \times 55 +18$，于是由抽屉原理可知，存在邻接的三段圆弧，其上标号之和至少为 $56$.

<p align="right">Q.E.D.</p>
