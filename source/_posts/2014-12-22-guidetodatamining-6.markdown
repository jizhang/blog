---
layout: post
title: "数据挖掘指南[6]概率和朴素贝叶斯"
date: 2014-12-22 10:33
comments: true
categories: [Tutorial, Translation]
published: true
---

原文：http://guidetodatamining.com/chapter-6

## 朴素贝叶斯

还是让我们回到运动员的例子。如果我问你Brittney Griner的运动项目是什么，她有6尺8寸高，207磅重，你会说“篮球”；我再问你对此分类的准确度有多少信心，你会回答“非常有信心”。

我再问你Heather Zurich，6尺1寸高，重176磅，你可能就不能确定地说她是打篮球的了，至少不会像之前判定Brittney那样肯定。因为从Heather的身高体重来看她也有可能是跑马拉松的。

最后，我再问你Yumiko Hara的运动项目，她5尺4寸高，95磅重，你也许会说她是跳体操的，但也不太敢肯定，因为有些马拉松运动员也是类似的身高体重。

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-6/chapter-6-1.png)

使用近邻算法时，我们很难对分类结果的置信度进行量化。但如果使用的是基于概率的分类算法——贝叶斯算法——那就可以给出分类结果的可能性了：这名运动员有80%的几率是篮球运动员；这位病人有40%的几率患有糖尿病；拉斯克鲁塞斯24小时内有雨的概率是10%。

近邻算法又称为**被动学习**算法。这种算法只是将训练集的数据保存起来，在收到测试数据时才会进行计算。如果我们有10万首音乐，那每进行一次分类，都需要遍历这10万条记录才行。

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-6/chapter-6-2.png)

贝叶斯算法则是一种**主动学习**算法。它会根据训练集构建起一个模型，并用这个模型来对新的记录进行分类，因此速度会快很多。

![](https://github.com/jizhang/guidetodatamining/raw/master/img/chapter-6/chapter-6-3.png)

所以说，贝叶斯算法的两个优点即：能够给出分类结果的置信度；以及它是一种主动学习算法。

[前往GitHub阅读全文](https://github.com/jizhang/guidetodatamining/blob/master/chapter-6.md)
