---
title: Pigeonhole Principle Exercise 022
date: 2019-03-18 00:23:07
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
某人步行 $10$ 小时，共行 $45$ 公里，第 $1$ 小时走了 $6$ 公里，最后一个小时走了 $3$ 公里. 试证：存在连续的两小时，这期间此人至少走了 $9$ 公里.

<!-- more -->
#### *Proof*
本问题较简单.

设 $a_i$ 是第 $i$ 小时行走的距离，那么由题意显然可知，$\sum_{i=2}^9 a_i = 45- 3-6=36$;

假设待证命题不成立，那么 $\sum_{i=1}^9 a_i+a_{i+1} < 9 \times 9=81$，从而 $2\times\sum_{i=2}^9 a_i < 81-9 =72$，这与上面的推论显然矛盾.

于是，待证命题成立.

<p align="right">Q.E.D.</p>