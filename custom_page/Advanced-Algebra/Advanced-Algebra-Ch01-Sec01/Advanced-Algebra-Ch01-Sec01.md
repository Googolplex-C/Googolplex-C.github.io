---
title: 高等代数笔记 章一 节一
date: 2019-07-04 21 31 40
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
export_on_save: html
html:
  embed_local_images: false
  embed_svg: true
  offline: false
  toc: true
---

# 引言

##### 代数学的研究内容

1. 古典代数学：

    代数方程的根的存在性和分布，如何计算这些根；
    
2. 近世代数：

    研究数、文字以及更广泛元素的代数规律，以及群、环、域、格、线性空间等代数系统的性质。

##### 本课程的内容框架

###### Part 1 线性代数部分

```viz{align=center}
strict  digraph G{
//attribute_statement:
//    ("graph" | "node" | "edge") *attribute_list*
    graph[splines="ortho"]
    node[shape="rect"]
//node_statement:
//    *node_id* *[attribute_list]*
    a[label="线性方程组"]
    b[label="向量空间"]
    c[label="行列式"]
    d[label="矩阵"]
    e[label="线性空间"]
    f[label="线性变换"]
    g[label="若当标准型"]
    h[label="双线性函数\n二次型"]
    i[label="欧氏空间与酉空间"]
    j[label="线性代数与分析、几何"]

//subgraph
    
//edge_statement:
//    (*node_id* | *subgraph*) *edgeRHS* *[attribute_list]*
    a -> b, c, d
    b -> e -> h
    d -> f -> g
    g -> i -> j
    f -> i -> j
    d -> c
    e -> f


}
```

