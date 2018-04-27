---
date: 2018-01-07 09:31:01
updated: {{ date }}
title: 单机模式 - 安装Spark2.* + Python3.*
categories: Spark
---

# 参考
http://spark.apache.org/
http://spark.apache.org/docs/latest/api/python/pyspark.html

# 简介

# Mac
*非常幸运的告诉你正使用MacOS，因为有一个牛逼的工具`brew(可查阅其它资料)`*

- 进入命令行工具
```
# 根据文件名查询软件
brew search apache-spark

# 查看软件的基本信息
brew info apache-spark

# 安装软件
brew install apache-spark

# 稍等片刻（安装包有200+M）
。。。。。。

# 安装完成后验证是否可用（这里使用pyspark，不懂Python都要被小学生鄙视啦，哈）
pyspark

# 到这里已经把Spark环境安装完成了...散发出大大到光环，如此简单

# 等等为什么是基于Python2.*跑起的Spark环境呢，不行...翻阅stackoverflow给出答案了
vim ~/.profile
export PYSPARK_PYTHON=python3
source ~/.profile

# 前提你的Mac电脑必须要有Python3的运行环境（命令行：python3），如果没有就...
brew install python3

# 好了，到这里算是完成了
pyspark
```

- done
![done](/uploads/posts/WX20180107-095252.png)

- SparkUI
默认是：http://localhost:4040
如果有端口占用了会递增+1，注意console的日志输出

- brew的spark安装目录
/usr/local/Cellar/apache-spark

- Anaconda-Navigator For Mac方式
[THIS](/2018/01/10/anaconda-navigator-for-mac/) 
