---
date: 2018-06-13 20:49:17
updated: {{ date }}
title: spring-cloud-starter-feign
categories: Spring
---



# 参考
https://springcloud.cc/spring-cloud-dalston.html#spring-cloud-feign

## 首先简单解释一下什么是声明式实现？
要做一件事， 需要知道三个要素，where, what, how。即在哪里（ where）用什么办法（how）做什么（what）。什么时候做（when）我们纳入how的范畴。
1）编程式实现： 每一个要素（where，what，how）都需要用具体代码实现来表示。传统的方式一般都是编程式实现，业务开发者需要关心每一处逻辑
2）声明式实现： 只需要声明在哪里（where ）做什么（what），而无需关心如何实现（how）。Spring的AOP就是一种声明式实现，比如网站检查是否登录，开发页面逻辑的时候，只需要通过AOP配置声明加载页面（where）需要做检查用户是否登录（what），而无需关心如何检查用户是否登录（how)。如何检查这个逻辑由AOP机制去实现， 而AOP的登录检查实现机制与正在开发页面的逻辑本身是无关的。

https://www.zhihu.com/question/21895282
**编程式实现**
需要以具体代码表达在哪里（where）做什么（what），如何实现（how）
**声明式实现**
只需要声明在哪里（where ）做什么（what），而无需关心如何实现（how）



# 简介



<!--more-->



# 使用
**引入**
```
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-feign</artifactId>
    <version>${spring-cloud-starter-feign.version}</version>
    <exclusions>
        <exclusion>
            <groupId>javax.ws.rs</groupId>
            <artifactId>jsr311-api</artifactId>
        </exclusion>
    </exclusions>
</dependency>
```

**show me the code**
```
package com.uc.sonic.scm.gerrit.api;

import com.uc.sonic.common.result.ReturnJsonResult;
import org.springframework.cloud.netflix.feign.FeignClient;
import org.springframework.stereotype.Service;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;
import org.springframework.web.bind.annotation.RequestParam;

@FeignClient(name = "flash-build-client", url = "${flash.build.api.url}")
@Service
public interface FlashBuildClient {

    @RequestMapping(method = RequestMethod.POST, value = "/flashbuild/gerrithooks")
    ReturnJsonResult putEventData(@RequestParam("event") String event);

}

```
