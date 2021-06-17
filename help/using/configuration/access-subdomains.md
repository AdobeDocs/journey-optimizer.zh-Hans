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
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: f4b36903b7b961dd20442acaf446e2ce99cc2b31
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---


# 访问委派的子域

所有委派的子域都显示在&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**&#x200B;菜单中。 过滤器可帮助您优化列表（委派日期、用户或状态）。

![](../assets/subdomain-list.png)

**[!UICONTROL Status]**&#x200B;列提供有关子域委派过程的信息：

* **[!UICONTROL Draft]**:子域委派已另存为草稿。单击子域名以恢复委派过程，
* **[!UICONTROL Processing]**:子域在使用之前会先执行多项配置检查，
* **[!UICONTROL Success]**:子域已成功完成检查，并可用于投放消息。
* **[!UICONTROL Failed]**:提交子域委派后，一个或多个检查失败。

要访问有关子域的详细信息，请从列表中将其打开。 您可以：

* 检索在委派过程中配置的子域名（只读），以及生成的URL（资源、镜像页面、跟踪URL），

* 将Google网站验证TXT记录添加到子域以确保对其进行验证（请参阅[将Google TXT记录添加到子域](google-txt.md)）。

![](../assets/subdomain-delegated.png)
