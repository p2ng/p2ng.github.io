---
comments: true
date: 2018-01-10 00:16:20
updated: {{ date }}
title: Anaconda Navigator For Mac
tags: 
categories: 
permalink:
keywords: 
description:
---

# 参考

# 简介

# 安装
`brew cask install anaconda`

# 设置国内镜像源
```
vim ~/.condarc

channels:
 - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
 - defaults
show_channel_urls: true
```

***

# 安装PySpark
http://spark.apache.org
http://spark.apache.org/docs/latest/api/python/pyspark.html
- 新建环境`PySpark`
- 搜索并安装`pyspark`

***

# 安装TensorFlow
https://www.tensorflow.org/
- 新建环境`TensorFlow`
- 搜索并安装`TensorFlow`

***

# 安装PyTorch
http://pytorch.org/
- 新建环境`PyTorch`
- 搜索并安装`conda`
- 进入该环境的目录（默认如：`/usr/local/anaconda3/envs/PyTorch/bin`）
- 执行`conda install pytorch torchvision -c pytorch`，安装PyTorch
- 好像要翻墙，不然下载不到PyTorch的包，还好中断过后不是全新覆盖下载。😄
![done](/uploads/posts/Snip20180112_3.png)
- 用Anaconda跑起Python3环境，Done😊
![done](/uploads/posts/Snip20180112_4.png)




