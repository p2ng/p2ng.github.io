---
date: 2018-03-06 22:37:25
updated: {{ date }}
title: Mac小技巧
categories: other
---



# Mac Shell
## 查看Mac概况
`archey`,需要`brew install archey`

## Cat文件时代码高亮
`brew install ccat`

## Shell自动补充命令
`brew install autojump`

## 文件以目录树形式展开
`brew install tree`

## Mac读出一段文字
`sleep 5 && say "Hello World"` 5秒后电脑说出HelloWorld
`mvn clean install && say 'build ok!!!'` 编译耗时长不想一直等待，可以巧妙使用&&

## 快速查看日历
```
cal // 查看当前日历
cal 2018 // 查看2018年的日历
date // 查看当前时间
```

## 显示/隐藏文件夹
```
命令运行之后需要重新加载Finder：快捷键option + command + esc，选中Finder，重新启动即可

此命令显示隐藏文件
defaults write com.apple.finder AppleShowAllFiles -bool true

此命令关闭显示隐藏文件
defaults write com.apple.finder AppleShowAllFiles -bool false
```


# Keyboard
## 调用emoji表情
control + command + 空格

## 输入苹果icon
option + shift + k

## 向后删除文本
fn + delete









