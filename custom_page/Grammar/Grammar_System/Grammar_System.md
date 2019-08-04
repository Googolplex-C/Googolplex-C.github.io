---
title: 语法体系概论
date: 2019-08-04 18 05 28
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


# 元语言与对象语言

作为一个母语是汉语的人，在学习英语语法的时候，元语言自然是汉语，对象语言自然是英语

另外，有必要分清 “研究术语” 和 “具体语言项” 之间的关系；

- 前者是在元语言中对于后者的称呼

- 后者是对象语言具体的体现

举个例子：

she's a bitch.

这里 "she" 这个单词就是具体的语言项，而在研究语法的时候，she 是个代词，在句子中作为主语；“代词”，“主语” 就是术语

某个具体的语言项被称之为术语的 **实现 (realization)**

可以借助一阶逻辑语言和其具体的模型来理解它们的关系。

# 语言的层次性

## 层次性

如果我们暂且忽略语言的具体表意，只从形式与结构上考虑它们的组成，那么可以很明确地看到，语言的构成是具有层次性的——位于不同层次的语言 “素材” 从低到高建构起了我们平常使用的语言；除了最底层和最高层的对象之外，位于其他层级的 “素材” 一方面构建起了位于其之上的层级，另一方面也由更底层的语言 “素材” 建构而成。

层次性是语言的基本属性之一。

## 语法单位与语言层级

### 概念
语法单位
:    如上一小节所述，这些位于不同层级上构成一门完整的语言的 “素材” 我们称之为 **语法单位**

语言层级
:    语法单位所处的层级称之为**语言层级**

请注意，语法单位不是特指某一个或者某几个特定的句子、单词或者短语，**它是一个语法术语**。我们在提及这个概念的时候，几乎总是不可避免地要和要与语法层次结合起来。但我们在进行语法分析的时候，可以把特指的某个句子、某个单词等称作某某语法单位（或者说 **作为**某某语法单位）

### 具体外延

按照从底层至高层的顺序，语言层次可以作以下划分：

1. 词素 morpheme

2. 词 word

3. 词组 pharse 
    // 有时也称短语

4. 分句 clause

5. 句子 sentence

6. 语段 sentence group

7. 语篇 text
 
其中，1 - 5 是语法结构意义上的层次划分，5 - 7 是语篇结构上的层次划分，句子是连接语法结构和语篇结构的桥梁。

### 层级顺序的确定

如果我们仔细考虑一下，其实可能会产生一个疑问：语言层级的顺序是如何确定的？比如，凭什么就说句子的层级位于词组之上？

或许有一种观点是：因为高层语法单位可以包含较低层的语法单位。但是考虑到 **包孕关系** 的存在，这种说法好像也略有瑕疵。

笔者认为，之所以按照这样的顺序，是因为我们天然具有这样的直觉……就好比，为什么我们承认逻辑学中那几个最基本的规律：同一律、无矛盾律等等，因为它本身就是那样的，我们不知道我们是如何知道的，但我们知道。

# 语法单位之间的关系

## 构成关系

### 概念内涵
构成关系
:    某个层级上的语法单位和构成它的语法单位之间的关系称之为 **构成关系**

构成成分
:    如果一个语法单位构成了另一个语法单位，那么前者是后者的 **构成成分**

直接构成关系
:    如果某个语法单位 A 构成了另一个语法单位 B，并且不存在第三个语法单位 C 使得 A 构成 C 的同时 C 构成 B，那么 A 就与 B 有直接构成关系，或称 A 直接构成 B

直接构成成分
:    如果一个语法单位直接构成了另一个语法单位，那么前者是后者的 **直接构成成分**

单独构成成分
:    如果一个语法单位是另一个语法单位的唯一构成成分，那么前者就是后者的单独构成成分。

**注解**

1. 请注意：我们没有断定 “A 的构成成分在语法上的层级就一定比 A 低”

2. 同一个语言项，（比如某个具体的句子或者词组）可以在一种场合下是一种单位，另一种场合下是另一个层级的单位

### 构成关系的表示方法
1. 树形表示法

    ```viz{align=center}
    digraph G{
        graph[rankdir=TB]

        a[label=词素]
        b[label=词]
        c[label=词组]
        d[label=分句]
        e[label=句子,style=invis]

        
        node[shape=none]

        subgraph cluster_1{
            f[label="The evenings has turned cold just recently"]
        }
        
        subgraph cluster_2{
            g[label="The evenings"]
            h[label="has turned"]
            i[label="cold"]
            j[label="just recently"]
        }
        
        subgraph cluster_3{
            k[label="The"]
            l[label="evenings"]
            m[label="has"]
            n[label="turned"]
            o[label="cold"]
            p[label="just"]
            q[label="recently"]
        }

        subgraph cluster_4{
            r[label="The"]
            s[label="evening"]
            t[label="s"]
            u[label="has"]
            v[label="turn"]
            w[label="ed"]
            x[label="cold"]
            y[label="just"]
            z[label="recent"]
            end[label="ly"]
        }
        

        d -> c -> b ->a

        f -> j,i,h,g

        g -> k,l

        h -> m,n

        i -> o

        j -> p,q

        k -> r
        
        l -> s,t

        m -> u

        n -> v,w 

        o -> x

        p -> y

        q -> z,end
    }
    ```

    从而从逻辑关系上看，不同层次的语法单位是一个树形关系。

2. 嵌套括号表示法

    前一种方法虽然非常直观，也能详尽地表示各个语法层次间的构成关系，但是较为繁琐，我们可以用另一种比较简便的方法表示，也就是嵌套括号方法。
    ```viz{align=center}
    graph G{

        sentence[label="[[[The] [evenings]] [[has] [turned]] [[cold]] [[just] [recently]]]", shape=none,fontsize=30]
    }
    ``` 

    示例中的语言层级到 “词” 这一层就为止；

3. 联系上一小节的理论

    - 在树形表示法中，树形结构的底层级的单位就是更高层级中对应单位的构成成分；

    - cold 在词组层面被视为一个形容词词组；尽管其本身就是一个单独的形容词，这就是一个典型的单独构成关系的例子：作为词的cold单独构成了作为词组的cold（联系[概念内涵](#概念内涵)中的注解第 2 点）

    - 词 just 直接构成了词组 just recently——这是一个直接构成关系的例子

    - 作为对比，词素 -ly 则是词组 just recently 的间接构成成分

## 功能与形式
考虑例子
```viz{align=center}
graph G{
    node[shape=none]

    "the weather has been cold just recently"
}
```

其中，"just recently" 可以替换成别的词组：
```viz{align=center}
graph G{
    node[shape=none]
    graph[rankdir=LR]

    "the weather has been cold ":e -- "just recently":w,"this month":w,"during the past week":w

}
```

所以，在句子中副词短语的位置上，可以由 名词短语 和 介词词组来代替原来的副词词组；

但是我们却不可以用副词词组去代替句首的名词词组

```viz{align=center}
graph G{
    node[shape=none]
    graph[rankdir=LR]

    "the weather has been cold "

    "just recently has been cold  (×)"

    "during the past has been cold  (×)"

}
```

可以有时候，不同的词组是可以相互替换的，但是有时候却不可以。

功能
:    一个单位，在由其组成的单位时，在出现与否、可出现的位置等方面的 出现权

功能与形式的区别

1. 前者说明的是某个语法单位在更高层次单位中的地位

2. 后者说明的是一个单位在更低层级中的内部结构

简单滴说，“状语”“主语” 这些属于功能类别，而“名词词组” “分句” 这些属于形式类别。


## 特殊的构成关系：包孕


### 概念
包孕 (embedding)
:    在语法的层级体系当中，位于某个层级的语法单位作为**同一层级或者更低层级**语法单位的构成成分的现象

### 举例
1. 词组包孕于词组

```viz{align=center}
graph G{
    graph[rankdir=TB]

    students[shape=none]
    "at this college"[shape=none]
    for[shape=none]
    "all our students"[shape=none]

    a[label=名词词组]
    b[label=名词]
    c[label=介词词组]

    d[label=介词词组]
    e[label=介词]
    f[label=名词词组]

    a -- b,c
    b -- students[style=dotted]
    c -- "at this college"[style=dotted]

    d -- e,f
    e -- for[style=dotted]
    f -- "all our students"[style=dotted]
}
```

2. 语法单位可以包孕在层级更低的单位中

```viz{align=center}
graph G{
    graph[rankdir=TB]

    node[shape=none]
    a[label=分句]
    b[label=名词词组]
    c[label=动词词组]
    d[label=名词词组,shape=box]
    d1[label=限定词]
    d2[label=前置修饰语]
    d3[label=名词中心词]
    e[label=关系分句,shape=box]
    f[label=名词词组]
    g[label=动词词组]
    h[label=副词词组]

    a -- b,c,d
    d -- d1,d2,d3,e
    e -- f,g,h

    edge[style=dotted]
    b -- "the room"
    c -- "has"
    d1 -- some
    d2 -- large
    d3 -- windows
    f -- which
    g -- face
    h -- south
}
```

### 意义

1. 包孕现象使得某些语法单位具有理论上的**无限拓展性**，也即使说，这些语法单位理论上可以无限扩展

    例如：

    ```viz{align=center}
    graph G{
        "...[the cat [that killed the rat [that ate the malt[that lay in the house [that Jack built]]]]]"[shape=none,fontsize=17]
    }
    ```

    理论上也不难理解，语法层级之间本来是纯粹的树形关系，但是因为包孕关系的缘故，使得层级的构成关系图中出现了环，从而在构建语言时候，可以沿着这个环无限 “循环” 下去

    ```viz{align=center}
    digraph G{
        graph[rankdir=BT]

        mid[label="......",shape=none]

        层级1 -> 层级2
        层级2 -> mid -> 层级i[color=red]
        层级i -> 层级2[constraint=false,color=red]
    }
    ```

2. 包孕具有**高度的灵活性**，如果我们需构建一个形式上很复杂（或者语义上很丰富）的语法单位，它将会是一个有力的工具。


### 特殊的包孕：从属

#### 概念
从属 (subordination)
:    一个分句作为另一个分句的构成成分的现象

从属是一种的包孕现象的一种，这种情况下，作为构成成分的分句称之为 **从属分句**，简称**从句**


从属分句常常需要一个**从属连词**引导

#### 举例
1. 从属关系的例子

```viz{align=center}
graph G{
    graph[rankdir=TB]

    a[label=分句]
    

    node[shape=none]
    c[label=名词词组]
    d[label=动词词组]
    e[label=形容词词组]
    e1[label=状语从句,shape=box]
    

    g[label=连词]
    c1[label=名词词组]
    d1[label=动词词组]
    f[label=介词词组]
    c2[label=名词词组]


    

    a -- c,d,e,e1
    e1 -- g,c1,d1,f,c2

    edge[style=dotted]
    c -- "The weather"
    d -- "has been"
    e -- "remarkly warm"
    g -- since
    c1 -- we
    d1 -- returned
    f -- "from Italy"
    c2 -- "last week"
}
```


### 并列

#### 概念
并列 (Coordination)
:    位于语言层级中相同层级的两个或者两个以上的语法单位，构成一个性质上仍等价于单个的这种单位，这种现象称之为并列。

并列的各个语法单位常常用一个连接词相连，这个连接词称之为**并列连词**

#### 举例
1. 分句并列
```viz{align=center}
graph G{
    node[shape=none,fontsize=17]

    "[I hate that woman], and [she is a bitch]"
}
```

2. 介词短语并列
```viz{align=center}
graph G{
    node[shape=none,fontsize=17]

    "You can go [[by car], or [by rail]]"
}
```
#### 意义
1. 笔者不是非常确定应该把并列视作一种特殊的包孕关系，从而与从属关系平级；还是将它视作一种与包孕平级相对的构建复杂语法单位的手段；

2. 不管怎样，并列也同样使得语法单位在理论上具有**无限扩展性**。
