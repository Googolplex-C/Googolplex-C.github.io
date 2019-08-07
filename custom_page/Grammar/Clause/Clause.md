---
title: 语言层级：分句
date: 2019-08-06 10:39:13
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

# 概念：分句

分句的内涵
:    1. 从结构形式上看：由一个或者一个以上的词组构成的序列

    2. 从语义含义上看：主语 + 谓语 的语法构造


因此：**（划重点！）**

<p align=center><font color="red"><b>若一个或者一个以上的词组在一定语境中构成了一种主谓关系，那么就可以判定为分句。</b></font></p>

**注意**

1. 由于从属关系的存在，分句的直接构成成分不一定是词组，也有可能是另一个分句;

2. 有时候分句可以只由一个词组组成

    ```
    - Where is the vase?

    - On the table.
    ```

    On the table 这个介词词组就可以认为是一个分句，在其所处的语境中实际上构成了一个主谓关系：(The vase is) on the table. 但是主语和谓语动词被省略了，后面会提到这是一个典型的非完全句的例子。

# 分句的分类

## 按照构成关系中的层级

1. 独立分句

2. 从属分句

独立分句
:    不依附于其他结构存在的分句。

**注**：

1. 独立分句往往自身就是一个句子

从属分句
:    不能独立存在，只能充当另一分句或者其他结构的组成成分的分句

**注**：
1. 之前在[特殊的包孕：从属](../Grammar_System/Grammar_System.html#特殊的包孕从属)中已经叙述过,从属分句又简称**从句**

### 主句与从句

从句即是从属分句，不再赘述。

主句
:    一个带有从句的独立分句

示例：

```viz{align=center}
graph G{
    graph[rankdir=TB]
    node[shape=none]

    subgraph G1{
        S
        V
        O
        A[label="A(subordinate clause)"]

    }

    subgraph cluster{
        
        graph[label="",rankdir=LR]
        {   
            rank = same
            You -- "can do" -- so -- if -- it -- rains[style=invis]
        }
    }

    subgraph G2{
        y[label="main clause"]
    }

    S -- You
    V -- "can do"
    O -- so
    A -- if:n,rains:n

    You:s,rains:s -- y

}
```

**注意：** 主句与从句的概念是相对的，一个分句在某种语境下是主句，到了另一种语境下可能就是分句

如下例所示：

```viz{align=center}
graph G{
    node[shape=none]
    subgraph G1{
        node[shape=none]
        S, V
        O[label="O(Subordinate Clause)"]
    }

    subgraph G2{
        graph[rank = same]
        node[shape=none]
        a -- b -- c[style=invis]
        a[label=I]
        b[label=think]
        c[label="you can do so if it rains"]
    }

    z[label="main clause"]

    S -- a
    V -- b
    O -- c
    a:s,c:s -- z
}
```

## 按照动词词组的形式

根据分句中的动词词组的形式，可以分为以下三类：

1. **限定分句**：动词词组是限定形式

2. **非限定分句**：动词词组是非限定形式

3. **无动词分句**：不出现动词词组

前两者的概念与解释请参见[概念梳理：动词，词组，分句的限定 / 非限定形式](../Finite_and_non_Finite/Finite_and_non_Finite.html)

无动词分句的示例如下

```
Full of apologies, the manager approached us.

The oranges, when ripe, are picked and sorted manually.
```

## 各个概念的交织关系

限定分句可以作为独立分句或者从属分句，非限定分句和无动词分句只能作为从属分句

另一角度而言，独立分句只能是限定分句，从属分句可以是限定分句，非限定分句和无动词分句

```viz{align=center}
graph G{
    rankdir=LR
    独立分句 -- 限定分句

    从属分句 -- 限定分句,非限定分句,无动词分句
}




