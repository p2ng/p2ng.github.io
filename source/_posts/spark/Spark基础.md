---
date: 2018-04-15 17:38:29
updated: {{ date }}
title: Spark基础
categories: Spark
---


# 术语
**Application**
基于Spark的用户程序，包含了driver程序和集群上的executor

**Driver Program**
运行main函数并且新建SparkContext的程序

**Cluster Manager**
在集群上获取资源的外部服务（例如standalone, Mesos, Yarn）

**Worker Node**
集群中任何可以运行应用代码的节点

**Executor**
是在一个worker node上为某应用启动的一个进程，该进程负责运行任务，并且负责将数据存在内存或者磁盘上。每个应用都有各自独立的executors

**Task**
被送到某个executor上的工作单元

**Job**
包含很多任务的并行计算，可以看做和Spark的action对应

**Stage**
一个Job会被拆分很多组任务，每组任务被称为Stage（就像MapReduce分map任务和reduce任务一样）



<!--more-->



# Q&A
## 框架
## SparkStreaming与Storm比较
## SparkStreaming高吞吐量怎么理解
## Spark开发与调优占比
## Spark开发与运维坑
## Scala与Java、Python、R选型


