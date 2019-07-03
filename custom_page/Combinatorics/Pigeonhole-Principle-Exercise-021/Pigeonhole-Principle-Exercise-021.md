---
title: Pigeonhole Principle Exercise 021
date: 2019-03-17 23:25:20
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
大厅中聚集着 $100$ 位客人，其中任何一个人至少认识其他 $67$ 人，试证：这些客人中一定可以找到 $4$ 个人，他们之中任意两人彼此认识.

<!-- more -->
#### *Proof*
首先，认识关系是对称的，$a$ 认识 $b$，那么 $b$ 也自然认识 $a$；不妨定义非自反的对称关系 $\mathrm{R}$：$a\ \mathrm{R}\ b$ 当且仅当 $a$ 和 $b$ 认识.
并定义集合 $S_a$ 为所有与 $a$ 认识的人的集合.

在所有的客人中任意地选取一位，记为 $x$，且另有客人 $y \in S_x$.考虑集合 $S_x$ 和 $S_y$，显然因为
$$
(\left| S_x \right| -1)+(\left| S_y \right| -1) \geq (67-1) \times 2 = 132 > (100-2)= 98
$$

所以，必存在第三位客人，记为 $z$，满足 $z \in S_x \cap S_y$，于是 $x$，$y$，$z$ 三位客人相互认识.

现在我们来证明另存在第四位客人与前面三位客人都认识，为方便起见，记 $S'_i = S_i - \{x,y,z\}$，其中 $i=x,y,z$，显然可知 $\left|S'_i \right| \geq 65$.

于是
$$
\left| S'_x \cap S'_y \cap S'_z \right| = \left| S'_x \cap (S'_y \cap S'_z )\right| \geq \left| S'_x \right|+\left|S'_y \cap S'_z \right| - 97 \\
\geq \left| S'_x \right| + \left| S'_y \right| + \left| S'_z \right| -97\times 2 \geq 65\times3-97 \times 2=1
$$

所以这个集合有且仅有一个成员，他与 $x$，$y$ 和 $z$ 都认识，于是命题得证.

<p align="right">Q.E.D.</p>


