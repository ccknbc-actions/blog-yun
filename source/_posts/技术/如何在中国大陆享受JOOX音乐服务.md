---
title: 如何在中国大陆享受JOOX音乐服务
date: 2020-10-07 18:00:00
updated: 2020-10-06 18:00:00
tags: 
- JOOX MUSIC
- 音乐
id: 10
sticky: 3
categories: 
- JOOX MUSIC
- 音乐
cover: https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-06~20:11:17.gif
top_img: https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-06~20:11:13.png
---

**本篇教程不需要科学上网工具，但会提及，并且`JOOX APP`之后是可以全球不受限制听歌哦**

在开始之前你可能需要知道`JOOX`什么，看了标题你知道它能提供流媒体音乐服务，但你需要了解一下它的身世

JOOX是一个起源于香港的正版音乐流媒体服务，提供包括三大唱片公司在内，超过200万首高品质歌曲的收听与下载。该服务发布于2014年12月，支持Android和iOS平台，在香港等地区运营。但现在它已在七个国家或地区运营，并支持了web和win, mac客户端[可上官网查看](https://www.joox.com/limits)，但你显然能发现页脚写着`Tencent`，啊没错就是你想的腾讯，其实你可以理解为海外版QQ音乐，但腾讯音乐娱乐的投资还不止这些，但这不是本文重点，前面提到，由于版权原因，只在特定地区运营，也就是限制了IP，而要享受JOOX提供的服务，就得让你的IP被识别为它支持的地区IP，大家通常都是使用魔法上网工具，来访问，但我发现它对IP限制并没有那么严格，那么是否可以伪造IP呢

## 火狐浏览器

打开浏览器，插件商店搜索`X-Forwarded-For Header`

安装后打开你的搜索引擎，搜索你想使用地区IP，比如香港或者泰国，马来西亚等，填入IP即可，就像图中所示

![X-Forwarded-For Header](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~12:56:23.png)

然后打开[JOOX官网](https://www.joox.com/)，就会根据你的IP自动识别区域，不同地区曲库不同所以根据个人需要来哦，接下来注册账号，不过如果是不使用中文的地区，可以在侧栏点击`lang`切换语言为中文哦，以下以泰国作为示例

![QQ图片20201007125937](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~12:59:56.png)

点击右上角Sign Up注册账号，根据相应要求填写信息，注册即可

![QQ截图20201007130110](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~13:04:38.png)

![QQ截图20201007130237](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~13:04:57.png)

你可以使用邮箱注册，手机号绑定绑定大陆手机号也是可以的，当然作为腾讯家的东西，你可以绑定微信，是不是很方便呢，这些你以后可以在APP中操作，这里不再赘述，登陆后你就可以尽情享受JOOX提供的音乐服务了

![QQ图片20201007130420](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~13:08:01.png)

## Chrome浏览器，QQ浏览器之类的呢

打开浏览器，插件商店搜索`Header-Editor`，至于怎么访问谷歌应用商店，不用我多说了吧

安装后按照下图所示填入即可，和火狐差不多

![QQ截图20201007130958](https://cdn.jsdelivr.net/gh/ccknbc-backup/photos/blog/2020-10-07~13:11:20.png)

但记得做好分类，以便于切换，即`Description`，要切换时记得`Active`选中即可，不使用时记得关闭插件或取消勾选以免影响国内一些网站的访问

## 总结

X-Forwarded-For 是一个 HTTP 扩展头部，主要是为了让 Web 服务器获取访问用户的真实 IP 地址（其实这个真实未必是真实的，后面会说到）。
    那为什么 Web 服务器只有通过 X-Forwarded-For 头才能获取真实的 IP？
    这里用 PHP 语言来说明，不明白原理的开发者为了获取客户 IP，会使用 $_SERVER['REMOTE_ADDR'] 变量，这个服务器变量表示和 Web 服务器握手的 IP 是什么（这个不能伪造）。
    但是很多用户都通过代理来访问服务器的，那么假如使用该全局变量，PHP获取到的 IP 就是代理服务器的 IP（不是用户的）。
    可能很多人看的晕乎乎的，那么看看一个请求可能经过的路径：客户端=>（正向代理=>透明代理=>服务器反向代理=>）Web服务器。其中正向代理、透明代理、服务器反向代理这三个环节并不一定存在。

什么是正向代理呢，很多企业会在自己的出口网关上设置代理（主要是为了加速和节省流量）。
透明代理可能是用户自己设置的代理（比如为了FQ，这样也绕开了公司的正向代理）。
服务器反向代理是部署在 Web 服务器前面的，主要原因是为了负载均衡和安全考虑。

现在假设几种情况：
    假如客户端直接连接 Web 服务器（假设 Web 服务器有公网地址），则 $_SERVER['REMOTE_ADDR'] 获取到的是客户端的真实 IP 。
    假设 Web 服务器前部署了反向代理（比如 Nginx），则 $_SERVER['REMOTE_ADDR'] 获取到的是反向代理设备的 IP（Nginx）。
    假设客户端通过正向代理直接连接 Web 服务器（假设 Web 服务器有公网地址），则 $_SERVER['REMOTE_ADDR'] 获取到的正向代理设备的 IP 。
其实这里的知识点很多，记住一点就行了，$_SERVER['REMOTE_ADDR'] 获取到的 IP 是 Web 服务器 TCP 连接的 IP（这个不能伪造，一般 Web 服务器也不会修改这个头）。

这个方法也能用于一些国外其他网站，但对于要求比较严格的，大家只能老老实实使用代理咯，好了，今天就讲到这里，我们下篇文章见！