---
date: 2018-03-14 21:21:24
updated: {{ date }}
title: Linux时间
categories: other
---

# 背景
今天在升级一个系统时遇到个小问题，系统是完全`前后端分离（Vue + Egg / SpringBoot）`，靠接口签名来验证身份，重点来了，接口签名算法用到时间`yyyyMMddHH`的字符串。

# 细节
部署前端（Vue + Egg）机器A：
用`root用户`登陆输入`date`命令出来的时间是`东八区`，但是切换到`部署系统用户`后是`零时区`...这就坑爹了
A机器生成的签名，去到B机器肯定校验不通过啦！！！

部署后端（SpringBoot）机器B：

# 解决
最近有同学升级了A机器的libc-2.12.so -> libc-2.14.so文件导致，降级后消除异常

# 思考
1. Linux的用户还会分不同的时区？不都是直接系统时间？
1. 还好是内部办公网的测试环境一台机器，假如是生产网或者多台机器时，怎么快速排查并解决？（docker的优势又出来了，😄）
