---
title: Pigeonhole Principle Exercise 024
date: 2019-03-29 21:25:31
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
某班有 $50$ 个学生，男女各占一半，他们围成一圈，试证：必有一位学生，此人两旁坐的都是女生.

<!-- more -->
#### *Proof*
##### Version 1
目标等价于有两个女生是 “跳跃相邻” 的（她们之间只相隔了一个学生），进而等价于两个女生在相邻的奇（或者偶）号位置上.

设圆周上的 $50$ 个座位为 $A_{1}^{}$, $A_{2}^{}$, $A_{3}^{}$, $\ldots$, $A_{50}^{}$，将其分为 $2$ 组，一组是奇数号的位置： $A_{1}^{}$, $A_{3}^{}$, $\ldots$, $A_{49}^{}$，另一组是偶数号的位置： $A_{2}^{}$, $A_{4 }^{}$, $\ldots$, $A_{50}^{}$.

将 $25$ 位女生归入以上两组之中，必有不少于 $13$ 位女生在同一组中，不失一般性，我们假设这 $13$ 位女生位于奇数组中，那么必有两位女生位于相邻的奇数位置上，此时这两位女生中间恰好有一位同学.

于是命题成立.
<p align="right">Q.E.D.</p>

##### Version 2 (My Version)

称连续排列且性别相同的若干位学生为 “ $1$ 段”，并注意到男生的段数恰好等于女生的段数.

若有连续相邻的 $3$ 位女生，则命题自然成立；

否则，女生的段数必然不少于 $13$ 段，从而男生也被分为不少于 $13$ 段，男生段与女生段交叉地排布. 那么必定有一个男生段，此段中恰好只有 $1$ 位男生，而这位男生两旁都是女生，命题得证.

<p align="right">Q.E.D.</p>
