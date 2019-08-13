---
title: Pigeonhole Principle Exercise 043
date: 2019-08-13 20:16:45
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
在正 $2008$ 边形 $A_1A_2\dots A_{2008}$ 的每个顶点上随意填上 $1$, $2$, $\dots$, $502$ 中的一个数，试证：存在一个矩形，其两条对角线对应的两对顶点填数之和相等。

#### *Proof*

考虑图形所有经过中心的对角线，共 $\frac{2008}{2}=1004$ 条这样的对角线，也即 $1004$ 对数字；

每一对角线确定的数对的取值下限是 $2$, 上限是 $1004$, 共 $1003$ 个取值选项。由抽屉原理可知，存在两条对角线，它们各自确定的数对之和相等。

而由简单的几何知识可知，这两条对角线必定是一个矩形的对角线。

<p align="right">Q.E.D.</p>
