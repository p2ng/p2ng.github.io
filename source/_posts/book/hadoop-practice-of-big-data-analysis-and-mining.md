---
date: 2018-03-11 22:47:33
updated: {{ date }}
title: Hadoop大数据分析与挖掘实战
categories: book 
---

# 参考
[Hadoop大数据分析与挖掘实战](https://item.jd.com/11837003.html)



# 数据挖掘基础
**定义挖掘目标**
针对具体的数据挖掘应用需求，首先要明确本次的挖掘目标是什么？系统完成后能达到什么样的效果？因此必须分析应用领域，包括应用中的各种知识和应用目标，了解相关领域的有关情况，熟悉背景知识，弄清用户需求。要想充分发挥数据挖掘的价值，必须要对目标有一个清晰明确的定义，即决定到底想干什么。
## 数据挖掘建模过程
目标定义（任务理解，指标确定）
数据采集（建模抽样，质量把控，实时采集）
数据整理（数据探索，数据清洗，数据变换）
构建模型（模式发现，构建模型，验证模型）
模型评价（设定评价标准，多模型对比，模型优化）
模型发布（模型部署，模型重构）
 
## 流程
业务系统 -> 数据抽取（ETL） -> 数据探索与预处理 -> 建模&应用 -> 结果&反馈



<!--more-->



# 书本案例
## 法律咨询数据分析与服务推荐
**目标：**
合适的资源推荐给用户，用户就会对该电子商务网站产生依赖，从而建立稳定的企业忠实顾客群，进而提高用户满意度。例如，当访问主页时，可以在婚姻栏目发现热点推荐。当访问具体的知识页面时，在页面的右边和下面发现也存在一些热点推荐和基于内容的关键字推荐。

**分析方法与思路**
1. 通过用户访问网站页面时记录访问日志（IP、地理信息、用户ID、时间、网站分类等等）
1. 数据量太大意味着物品数与用户数很多，在模型构建用户与物品的稀疏矩阵时，出现设备内存空间不够的情况，并且模型计算需要消耗大量的时间
1. 用户区别很大，不同用户关注的信息不同，因此即使能够得到推荐结果，其推荐效果也会不好
1. 以用户浏览网页的类型分类，然后推荐每个类型中的内容

**分析过程**
1. 从系统中获取用户访问网站的原始记录
1. 对数据进行多维度分析，用户访问内容、流失用户分析以及用户分类等分析
1. 对数据进行预处理，包括数据去重、数据删选、数据分类等处理过程
1. 以用户访问html后缀等网页位关键条件（网页包含分类信息），对数据进行处理
1. 对比多种推荐算法进行推荐，通过模型评价，得到比较好的智能推荐模型。通过模型对样本数据进行预测，获得推荐结果



## 电商产品评论数据情感分析
**目标**
1. 分析某一商品的用户情感倾向
1. 从评论文本中挖掘出该商品的优点与不足
1. 提炼不同品牌商品的卖点

**分析方法与过程**
1. 利用爬虫工具（八抓鱼）
1. 对获取对数据进行基本对处理操作，包括数据预处理（文本去重、机械语料压缩以及短句删除）、中文分词、停用此过滤
1. 文本评论数据经过处理后，运用多种手段对评论数据进行多方面对分析
1. 从对应结果对分析中获取文本评论数据中有价值对内容

**构建模型**
1. 情感倾向性模型
1. 基于语义网络都评论分析
1. 基于LDA模型的主题分析



## 航空公司客户价值分析
**目标**
1. 借助航空公司客户数据，对客户进行分类（利用类似Hive/SparkSQL等抽取数据大表：客户基本信息、乘机信息、积分信息等大类别）
1. 对不同的客户类别进行特征分析，比较不同类客户对价值
1. 对不同价值的客户类别提供个性化服务，制定相应对营销策略

**分析方法与过程**
识别客户价值，即通过航空公司客户数据识别不同价值等客户。识别客户价值应用最广泛等模型是通过三个指标（最近消费时间间隔recency、消费频率frequency、消费金额monetary）来进行客户细分，识别出高价值等客户，简称`RFM模型`



## 基站定位数据商圈分析
**目标**
1. 对用户的历史定位数据，采用数据挖掘技术，对基站进行分群
1. 分析不同商圈分群的特征，比较不同商圈类别的价值，选择合适的区域进行运营商（也可以其它）的促销活动

**分析方法与过程**
1. 从移动通信运营商提供的特定接口上解析、处理、并滤除用户属性后得到用户定位数据
1. 以单个用户为例，进行数据探索分析，研究在不同基站的停留时间，并进一步进行预处理，包括数据规约和数据变换
1. 利用上一步，形成的已完成数据预处理的建模数据，基于基站覆盖范围区域的人流特征进行商圈聚类，分析各个商圈分群的特征，选择合适的区域进行运营商的促销活动



## 互联网电影智能推荐
**目标**
根据用户对电影的评分数据，利用只能推荐技术，实现电影只能推荐

**分析方法与过程**
常用推荐算法：基于内存的推荐算法、协同过滤推荐算法和基于网络结构的推荐算法
`协同过滤推荐`的主要研究方向分为`基于内存的算法`和`基于模型的算法`两类，其中`基于内存的协同过滤推荐算法`按照`相似度`比较对象的不同，又可以分为`基于用户`和`基于项目`两种，但基于用户的协同过滤随着用户数的增加，计算的复杂度会越来越大，因此`基于项目的协同过滤`应用相对较多。
显式评分：用户直接对项目对打分
隐式评分：根据用户的历史行为记录，如浏览频率、评论等信息间接推测出的评分

1. 从视频网站的数据库中选择性抽取用户对电影的评分数据和电影元数据
1. 利用用户对电影的评分数据构造`用户 - 项目评分矩阵`
1. 利用2）形成的`用户 - 项目评分矩阵`，计算`电影项目之间的相似度`
1. 利用2）的`用户 - 项目评分矩阵` 和3）的`电影项目之间的相似度`，计算用户的电影项目评分预测，并把预测评分高的电影项目作为推荐结果

矩阵：
N * M（用户数目 * 电影数目）列 * 行
用户1电影1评分    用户1电影2评分    用户1电影3评分    用户1电影4评分    。。。
用户2电影1评分    用户2电影2评分    用户2电影3评分    用户2电影4评分    。。。
用户3电影1评分    用户3电影2评分    用户3电影3评分    用户3电影4评分    。。。
。。。



## 家电故障备件储备预测分析
**目标**
对不同的地区进行整理分析，构建地区、故障、故障出现率数据，使用协同过滤算法预测各地区故障及故障率

**分析方法与过程**
1. 从数据源中抽取出历史数据
1. 根据历史数据，进行数据探索分析，研究数据对缺少和异常情况，并进一步进行预处理
1. 数据预处理的过程中需要对数据进行属性提取、变换、从而得到用于协同过滤算法模型的建模数据
1. 利用3）的建模数据，建立协同过滤算法模型。针对地区、地区故障、地区故障率数据，使用协同过滤算法模型进行预测分析。根据模型的输出结果进行应用，根据应用的情况来优化模型。反复循环，最终得到模型的结果，用于实际应用



## 市供水混凝投药量控制分析



## 基于图像处理的车辆压双黄线检测
**分析方法与过程**
1. 从数据源中抽取出历史视频数据（视频按照帧来分割）
1. 根据历史视频数据，进行数据探索分析，研究数据的缺失和异常情况，并进一步预处理
1. 数据预处理主要是对图像数据进行预处理，包括道路双黄线自动提取、道路背景提取、运动车辆提取、运动车辆阴影去除、运动车辆与行人区分等；针对不同的处理应用不同的技术，如均值滤波、变形Sobel算子、P-参数和最大类间方程以及Otus阀值化技术等过滤图像数据
1. 经过数据预处理后的图像数据，应用车辆中心检测方法以及灰度帧差统计方法来检测车辆压双黄线

**车辆压双黄线检测流程图**
开始

自动双黄线检测 -> 失败 -> 人工标记双黄线

道路背景提取

基于背景差分法和高斯混合模型法的车辆目标检测与跟踪

行人与车辆区分

车辆压双黄线检测

结束