=== WPComment2Bark ===
Contributors: 7gugu
Tags: 评论, 消息通知
Requires at least: 4.7
Tested up to: 5.8
Stable tag: 1.0.0
Requires PHP: 7.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Wordpress新评论Bark通知 

== Description ==

# WPComment2Bark

## 背景 🏞

最近大半年都在搞实习和雅思，其实没做多少实用的工具出来，有点手痒痒了。因此接着博客重建的契机，动手搞了一个评论信息推送的小插件。

## 思考 🤔

### 技术指标:

1. 高触达率 🚀
2. 开箱即用 📦
3. 高度安全 🔐

### 解决方案:

1.邮件推送

原来的推送方式就是通过Email的形式来推送，有可能会出现消息推送不及时或者被拒信，无法满足高触达率的技术要求，故摒弃这种推送方式。

2.Server酱

Server酱年初也因为各种外部原因，降级成了企业微信推送，其实不是特别方便，用户还得去装一个企业微信，然后配置Bot，再去配置APIKEY。对于我们做开发的用户来说，已经是挺繁琐的步骤了，对于普通用户而言简直就是噩梦。无法满足开箱即用的要求，故放弃。

3.Bark

最后我将目光投到了Bark身上，Bark是V站的一个dalao搞的一套利用Apple消息推送机制做的Web信息推送框架。Bark也同时满足我们三项技术要求: 

- 高触达率

借助Apple推送机制，我们甚至可以在息屏的情况下，都能正常收到推送消息。无视任何垃圾回收机制，绝对在线。

- 开箱即用

用户只要下载Bark客户端，博客安装插件，配置插件，即可投入实际使用。

- 高度安全

Bark提供免费服务器的同时，也提供了源代码供用户进行审查。如果是对于隐私比较敏感的用户，还能选择通过Docker部署自己的私有推送服务器。

综合上述优点，我选择了使用Bark作为消息推送的核心功能支持。

## 作用 🏄🏼‍♀️

每当有人评论你的文章时，可以推送到你的 Bark App。

## 配置指南 🧭

1.从AppStore下载Bark客户端

![screenshot-1](../assets/screenshot-1.png)

2.上传 &amp; 安装插件

![screenshot-1](../assets/screenshot-2.png)

3.配置推送链接

首先从客户端上复制出推送API和API密钥

![screenshot-1](../assets/screenshot-3.png)

第二步，切换到博客后台，依次点击【设置->讨论】，滚动到底部，找到【Bark推送设置】


至此就完成了全部配置工作，只要有新的评论被发出，就会调用API想您推送消息。

## 插件仓库 ⛺️

[https://github.com/7gugu/WPComment2Bark](https://github.com/7gugu/WPComment2Bark)

点击【Code -&gt; Download ZIP】下载压缩包后，按照配置指南，一步一步的安装即可。

## 联系方式

1. 博客: [https://www.7gugu.com](https://www.7gugu.com)
2. 邮箱: gz7gugu@qq.com

== Changelog ==

= 1.0.0 =
* 加入Bark消息推送功能
