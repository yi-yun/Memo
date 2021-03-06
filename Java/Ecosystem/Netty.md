---
title: Netty.md
date: 2018-11-21 10:56:52
tags: 
categories: 
---

**目录 start**
 
1. [Netty](#netty)
    1. [使用](#使用)
        1. [编解码相关](#编解码相关)
            1. [Protobuf](#protobuf)
    1. [原理](#原理)
        1. [源码](#源码)

**目录 end**|_2019-04-22 00:14_|
****************************************
# Netty
> [trustlin](https://github.com/trustin)`Netty Mina 的作者`

Netty是由JBOSS提供的一个java开源框架。Netty提供异步的、事件驱动的网络应用程序框架和工具，用以快速开发高性能、高可靠性的网络服务器和客户端程序。

> [知乎: 通俗地讲，Netty 能做什么？](https://www.zhihu.com/question/24322387)  
> [为什么选择Netty作为基础通信组件？ ](https://my.oschina.net/zhaky/blog/760469)

************************

> [Netty4.x官方文档](http://netty.io/wiki/user-guide-for-4.x.html)  
> [Netty权威指南](https://javablog.net/book/3/netty-authoritative-guide.html)  
> [Reactive Extension (Rx) Adaptor for Netty ](https://github.com/ReactiveX/RxNetty)

> [《Netty 实战》 Netty In Action 中文版](https://github.com/ReactivePlatform/netty-in-action-cn)
> [参考博客: 从线程模型的角度看 Netty 为什么是高性能的？ ](https://crossoverjie.top/2018/07/04/netty/Netty(2)Thread-model/)  



********************

## 使用
> 部分内容参考自 Netty权威指南第二版

> [手淘、微博一直钟情的 Netty框架是个什么鬼？](https://yq.aliyun.com/roundtable/53346)
> [对于Netty的十一个疑问  ](https://news.cnblogs.com/n/205413/)  
> [NettyServer与SpringBoot集成](https://segmentfault.com/a/1190000004919133)  
> [Netty NIO 框架性能压测-短链接-对比Tomcat ](http://www.oschina.net/question/12_8749)


### 编解码相关
> [参考博客: Netty(三) 什么是 TCP 拆、粘包？如何解决？](https://crossoverjie.top/2018/08/03/netty/Netty(3)TCP-Sticky/)  

#### Protobuf
> [Protobuf基础](/Java/AdvancedLearning/ClassFile.md#protobuf) | 
> [Netty中的使用案例](https://github.com/Kuangcp/NettyBook2/blob/master/src/main/java/com/phei/netty/codec/protobuf/README.md)
>> 要搭配处理半包的解码器

1. 使用 ProtobufVarint32FrameDecoder 
2. 继承自 LengthFieldBasedFrameDecoder
3. 继承自 ByteToMessageDecoder 自己处理

*****************************
## 原理
> [Netty核心组件](http://cmsblogs.com/?p=2467)  
> [Netty 编解码技术 数据通信和心跳监控案例](https://segmentfault.com/a/1190000013122610)  
> [Netty 拆包粘包和服务启动流程分析](https://segmentfault.com/a/1190000013039327)  
> [Netty序章之BIO NIO AIO演变](https://segmentfault.com/a/1190000012976683)

> [Netty构建游戏服务器(一) 有原理图](http://ju.outofmemory.cn/entry/278582)  
[Netty高性能开发备忘录](http://www.10tiao.com/html/321/201611/2659763226/5.html)

### 源码
> [官方Demo](https://github.com/netty/netty/tree/4.1/example/src/main/java/io/netty/example)
> [Netty实战配套源码](https://github.com/ReactivePlatform/netty-in-action-cn)
> [Netty权威指南2 源码](https://github.com/Kuangcp/NettyBook2)
