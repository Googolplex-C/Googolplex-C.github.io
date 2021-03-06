---
title: Pigeonhole Principle Exercise 040
date: 2019-08-13 17:21:42
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
已知一个国际社团的成员来自 $6$ 个国家，共有 $1957$ 人，分别用 $1$, $2$, $\dots$, $1957$ 将这些成员唯一地编号。试证：此社团中必定有一个成员，他的编号是他的两位同胞（此处同胞的定义是来自同一国家的成员）编号之和，或者他的某位同胞的编号的两倍。


#### *Proof*
假设命题不成立，即：对于此社团中的任意一位成员，他的编号都不是他某两位同胞的编号之和，也不是他某位同胞编号的两倍；这也意味着，对于同一个国家的任何两个成员，其编号之间的差值所表示的编号都不属于他们的同胞。

注意到：$1957 = 6 \times 326 + 1$, 由抽屉原理可知，必定有某个国家，记为 $A$ 国，其成员数至少为 $327$；不妨记这个国家的成员为

$$
a_1 > a_2 > \cdots > a_{327}
$$

考察序列

$$
(a_1 - a_{327}^{}), (a_2-a_{327}^{}),(a_3-a_{327}^{}), \cdots, (a_{326}-a_{327}^{})
$$

这些值是必定有唯一的社团成员与之对应，并且根据我们的假设，他们必定不是 $A$ 国的成员，而只可能是其他五个国家的成员。

注意到：$326  = 5 \times 65 + 1$, 由抽屉原理可知，必定有某个国家，记为 $B$ 国，其在上一个序列中的成员数至少为 $66$；不妨记这个国家的在上一序列中的成员为

$$
b_1 > b_2 > \cdots > b_{66}
$$

考察序列

$$
(b_1 - b_{66}^{}), (b_2-b_{66}^{}),(b_3-b_{66}^{}), \cdots, (b_{65}-a_{66}^{})
$$

这些值是必定有唯一的社团成员与之对应，并且根据我们的假设，他们必定不是 $A$, $B$ 国的成员，而只可能是其他四个国家的成员。

注意到：$65  = 4 \times 16 + 1$, 由抽屉原理可知，必定有某个国家，记为 $C$ 国，其在上一个序列中的成员数至少为 $17$；不妨记这个国家的在上一序列中的成员为

$$
c_1 > c_2 > \cdots > c_{17}
$$

考察序列

$$
(c_1 - c_{17}^{}), (c_2-c_{17}^{}),(c_3-c_{17}^{}), \cdots, (c_{16}-a_{17}^{})
$$

这些值是必定有唯一的社团成员与之对应，并且根据我们的假设，他们必定不是 $A$, $B$, $C$ 国的成员，而只可能是其他三个国家的成员。

注意到：$16  = 3 \times 5 + 1$, 由抽屉原理可知，必定有某个国家，记为 $D$ 国，其在上一个序列中的成员数至少为 $6$；不妨记这个国家的在上一序列中的成员为

$$
d_1 > d_2 > \cdots > d_{6}
$$

考察序列

$$
(d_1 - d_{6}^{}), (d_2-d_{6}^{}),(d_3-d_{6}^{}), \cdots, (d_{5}-d_{6}^{})
$$

这些值是必定有唯一的社团成员与之对应，并且根据我们的假设，他们必定不是 $A$, $B$, $C$, $D$ 国的成员，而只可能是其他两个国家的成员。

注意到：$5  = 2 \times 2 + 1$, 由抽屉原理可知，必定有某个国家，记为 $E$ 国，其在上一个序列中的成员数至少为 $3$；不妨记这个国家的在上一序列中的成员为

$$
e_1 > e_2  > e_{3}
$$

考察序列

$$
(e_1 - e_{3}^{}), (e_2-e_{3}^{})
$$

这些值是必定有唯一的社团成员与之对应，并且根据我们的假设，他们必定不是 $A$, $B$, $C$, $D$, $E$ 国的成员，而只可能是最后一个国家的成员。

最后，我们记剩下的那个国家为 $F$, 我们已知到 $(e_1 - e_{3}^{}), (e_2-e_{3}^{})$ 对应这个国家的某两位成员，那么 $e_1-e_2$ 对应哪个国家呢？

按照假设，这个成员不属于以上六个国家中的任何一个，于是产生矛盾。

所以假设不成立，命题得证。

<p align="right">Q.E.D.</p>


#### Note

本问题真的非常巧妙，笔者暂时还不是非常适应这种思路……
