---
layout: post
title: "数据挖掘指南[2]推荐系统入门"
date: 2014-08-29 12:00
comments: true
categories: [Tutorial, Translation]
published: true
---

原文：http://guidetodatamining.com/chapter-2/

内容：

* 推荐系统工作原理
* 社会化协同过滤工作原理
* 如何找到相似物品
* 曼哈顿距离
* 欧几里得距离
* 闵可夫斯基距离
* 皮尔逊相关系数
* 余弦相似度
* 使用Python实现K最邻近算法
* 图书漂流站（BookCrossing）数据集

## 你喜欢的东西我也喜欢

我们将从推荐系统开始，开启数据挖掘之旅。推荐系统无处不在，如亚马逊网站的“看过这件商品的顾客还购买过”板块：

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-2/chapter-2-1.png)

last.fm上对音乐和演唱会的推荐（相似歌手）：

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-2/chapter-2-2.png)

在亚马逊的例子里，它用了两个元素来进行推荐：一是我浏览了里维斯翻译的《法华经》一书；二是其他浏览过该书的顾客还浏览过的译作。

本章我们讲述的推荐方法称为协同过滤。顾名思义，这个方法是利用他人的喜好来进行推荐，也就是说，是大家一起产生的推荐。他的工作原理是这样的：如果要推荐一本书给你，我会在网站上查找一个和你类似的用户，然后将他喜欢的书籍推荐给你——比如巴奇加卢比的《发条女孩》。

### 如何找到相似的用户？

所以首先要做的工作是找到相似的用户。这里用最简单的二维模型来描述。假设用户会在网站用五颗星来评价一本书——没有星表示书写得很糟，五颗星表示很好。因为我们用的是二维模型，所以仅对两本书进行评价：史蒂芬森的《雪崩》（纵轴）和拉尔森的《龙纹身的女孩》（横轴）。

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-2/chapter-2-3.png)

首先，下表显示有三位用户对这两本书做了评价：

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-2/chapter-2-4.png)

现在我想为神秘的X先生推荐一本书，他给《雪崩》打了四星，《龙纹身的女孩》两星。第一个任务是找出哪个用户和他最为相似。我们用距离来表示。

[前往GitHub阅读全文](https://github.com/jizhang/guidetodatamining/blob/master/chapter-2.md)
