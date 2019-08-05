---
title: "概念梳理：动词，词组，分句的限定 / 非限定形式"
date: 2019-08-05 22:47:47
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

# 定义：限定与非限定

**限定与非限定这一对范畴，首先是针对动词的。**

（动词的）限定形式
:    若一个动词满足以下条件

    - 允许具有**时 (tense)** 的标记
    - 允许受其主语的**人称**和**数**的影响发生屈折变化

    那么称这个动词以限定形式出现

（动词的）非限定形式
:    若一个动词不以限定形式出现，那么它就以非限定形式出现。

# 动词词组的限定与非限定

我们都知道，动词词组可能只由一个主动词构成，也可能由不少于一个助动词 + 主动词构成；前者称为简单动词词组，后者称为复杂动词词组。

限定动词词组
:    若动词词组的**第一个动词**以限定形式出现，那么该动词词组就是限定动词词组

非限定动词词组
:    若动词词组的**第一个动词**以非限定形式出现，那么该动词词组就是非限定动词词组

# 分句的限定与非限定

我们知道，从语义上讲，分句一定是在某个语境下形成了 “主语 + 谓语” 的结构，我们考虑那些具有 **谓语动词** 的分句

限定分句
:    若某个分句的谓语动词由限定动词词组充当，那么该分句就是限定分句。

非限定分句
:    若某个分句的谓语动词由非限定动词词组充当，那么该分句就是非限定分句。

# 关系整理

```viz{align=center}
digraph G{
    graph[rankdir=TB]

    a[label="是否受 tense、主语的人称和数的影响？",shape=none]
    b[label=限定形式动词]
    c[label=非限定形式动词]
    d[label=限定动词词组]
    e[label=非限定动词词组]
    f[label=限定分句]
    g[label=非限定分句]

    a -> b[label=Y]
    a -> c[label=N]
    b -> d[label=第一个动词]
    c -> e[label=第一个动词]
    d -> f[label=作为谓语动词]
    e -> g[label=作为谓语动词]
}
```

