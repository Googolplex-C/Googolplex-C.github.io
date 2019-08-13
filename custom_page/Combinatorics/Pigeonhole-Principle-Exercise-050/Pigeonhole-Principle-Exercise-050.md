---
title: Pigeonhole Principle Exercise 050
date: 2019-08-13 21:46:34
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
八名学生分别独立解答八个问题，结果发现，每个问题恰好被五名学生解出，试证：其中必有两名学生，他们各自解出的问题的并集就是所有的八个问题。

#### *Proof*

我们先来考虑相反的情形，也即：两个学生所解出问题的并集不足以覆盖全部问题，当且仅当：存在某个问题，使得这两个学生都没能解出。

我们称：**这个问题贯穿了这两位 / 一对学生**.

题设告诉我们，每个问题恰好被五名学生解出，也就是每个问题有 $3$ 名学生没有解出，从而每个问题贯穿了 $3$ 对学生，$8$ 个问题总共贯穿了 $24$ 对学生。

但是要使得任意两名学生解决的问题并集都无法覆盖全部问题，需要贯穿 $\binom{8}{2}= 28$ 对学生，显然 $24 < 28$, 无法做到。

于是命题得证。

<p align="right">Q.E.D.</p>
