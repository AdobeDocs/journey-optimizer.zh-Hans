---
title: PTR记录
description: '"了解如何管理ptr-records"'
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
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---


# PTR记录

## 关于PTR记录

指针记录(PTR)是一种域名系统(DNS)记录类型，它提供链接到IP地址的域名。

使用PTR记录，接收邮件服务器可以通过确定其IP地址是否与服务器所连接的名称对应来检查邮件服务器发送的真实性。

## 访问子域的PTR记录

在Customer Journey Management中委派子域后，将自动创建PTR记录并与此子域关联。 您可以从&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL PTR records]**&#x200B;菜单访问它。

![](../assets/ptr-records.png)

该列表使用以下语法显示为每个委派的子域生成的PTR记录：

* “r”表示记录，
* “xx”表示IP地址的最后两个数字，
* 子域名。

您可以从列表中打开PTR记录以显示关联的子域名和IP地址。

>[!NOTE]
>
>请注意，PTR记录是只读的，您无法修改与IP地址关联的子域。
