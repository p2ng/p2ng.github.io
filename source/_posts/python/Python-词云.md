---
date: 2018-03-30 22:38:31
updated: {{ date }}
title: Python-词云
categories: Python
description:
---


# 简介
简单说，词云是根据一段文字里的关键词出现频率生成文字的图片组合，字体越大说明对应的词汇的频率越高！词云适合分析一些文本类型的字段，比如用户职位分布、热点词分析等。

# wordcloud
https://wordart.com/

## Install
`$ pip install wordcloud`

## Demo

**在线工具**
Wordle是一个用于从文本生成词云图而提供的游戏工具
Tagxedo 可以在线制作个性化词云
Tagul 是一个 Web 服务，同样可以创建华丽的词云
Tagcrowd 还可以输入web的url，直接生成某个网页的词云

**Python实现**
```
import matplotlib.pyplot as plt
from wordcloud import WordCloud
import jieba

# 是读取本地的文件
text_from_file_with_apath = open('/Users/hecom/23tips.txt').read()

# 使用jieba进行分词，并对分词的结果以空格隔开
wordlist_after_jieba = jieba.cut(text_from_file_with_apath, cut_all = True)
wl_space_split = " ".join(wordlist_after_jieba)

# 对分词后的文本生成词云
my_wordcloud = WordCloud().generate(wl_space_split)

plt.imshow(my_wordcloud)
plt.axis("off")
plt.show()
```
