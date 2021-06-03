---
title: 重试
description: 了解在向抑制列表发送地址之前如何执行重试
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
source-git-commit: 80c307a349a8ca7449639e7819683bf1f3ec3d13
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 重试 {#retries}

当消息因临时&#x200B;**软退件**&#x200B;或&#x200B;**Ignored**&#x200B;错误而失败时，将执行多次重试。 每个错误都会增加一个错误计数。 当此计数器达到限制阈值时，地址将添加到禁止列表。

在默认配置<!--so can you edit this setting or not?? contradictory information was given-->中，阈值设置为以下三个错误：

* 对于同一投放，在第三次遇到错误时，地址被禁止。

* 如果存在不同的投放并且两个错误在至少24小时之间发生，则在每次错误时错误计数递增，并且在第三次尝试时地址也被抑制。

如果重试投放成功，则地址的错误计数会重新初始化。

您可以使用&#x200B;**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**&#x200B;菜单中的&#x200B;**[!UICONTROL Edit]**&#x200B;按钮修改限制阈值。<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## 消息重试持续时间{#retry-duration}

从将消息添加到电子邮件队列开始，将对&#x200B;**3.5天**&#x200B;执行重试。

重试之间的最短延迟和要执行的最大重试次数是<!--managed by the Enhanced MTA,--> ，具体取决于IP在给定域名的历史和当前表现。

3.5天后，重试队列中的任何消息都将从队列中删除，并作为退件发送回。<!--???-->