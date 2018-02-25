---
date: 2018-02-18 09:33:25
updated: {{ date }}
title: Homebrew
tags:
categories: Mac
permalink:
keywords:
description:
---

# Homebrew
https://brew.sh/
http://caskroom.github.io/
[brew和brew cask有什么区别？](https://www.zhihu.com/question/22624898)

## install
```
# brew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# cask
brew tap caskroom/cask
```



# Homebrew cask upgrade
由于Homebrew-cask不支持动态显示软件版本是否有更新，所以要安装插件来管理...
https://github.com/buo/homebrew-cask-upgrade
## install
```
brew tap buo/cask-upgrade
```



# Command
## Homebrew
```
brew list               显示所有的已安装的软件
brew info $<软件包>      显示某个包信息
brew info               显示安装的包数量、文件数量以及占用空间 

brew search text        搜索本地远程仓库的软件，已安装会显示绿色的勾
brew install <formula>  安装指定软件
brew unistall <formula> 卸载指定软件

brew update             自动升级homebrew（从github下载最新版本）
brew outdated           检测已经过时的软件
brew upgrade            升级所有已过时的软件，即列出的以过时软件
brew upgrade <formula>  升级指定的软件
brew pin <formula>      禁止指定软件升级
brew unpin <formula>    解锁禁止升级
brew upgrade --all      升级所有的软件包，包括未清理干净的旧版本的包

brew cleanup -n         列出需要清理的内容
brew cleanup <formula>  清理指定的软件过时包
brew cleanup            清理所有的过时软件
```

## Homebrew cask
用法基本同`Homebrew`一致

## Homebrew cask upgrade
```
brew help cu            help
brew cu                 Upgrade outdated apps
brew cu [CASK]          Upgrade a specific app
```



# 全球最大基友交友网共享
https://github.com/jaywcjlove/awesome-mac/blob/master/README-zh.md

# 备份
https://zhuanlan.zhihu.com/p/28249327

# Show Case

