---
title: 委派子域
description: 了解如何委派子域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# 子域委派入门

## 隔离您的品牌以保护您的声誉

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量（交易消息、营销信息等）。让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商加入阻止列表，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被加入阻止列表。

## 使您的资源URL对客户而言透明

实施解决方案时，需要面向外部的组件：这些功能包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过由Adobe和客户托管的组件进行管理，但它们包含可供电子邮件收件人查看的URL。 为避免拥有指示底层技术解决方案或托管提供商的URL，可以设置子域以使其对电子邮件的收件人透明。 [了解有关域委派的更多信息](https://helpx.adobe.com/cn/campaign/kb/domain-name-delegation.html)。

## Journey Optimizer中的子域委派

Journey Optimizer提供了以下几项功能来帮助您管理子域：

* [直接从](delegate-subdomain.md) 界面委派子域，
* [将Google TXT记录](google-txt.md) 添加到子域，以确保将电子邮件成功发送到Gmail地址，
* [访问为子](ptr-records.md) 域生成的PTR记录，以便通过发送邮件服务器来验证它们。
