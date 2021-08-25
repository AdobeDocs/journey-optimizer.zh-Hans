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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# 重试 {#retries}

当电子邮件由于临时&#x200B;**软退件**&#x200B;或&#x200B;**Ignored**&#x200B;错误而失败时，将执行多次重试。 每个错误都会增加一个错误计数。 当此计数器达到限制阈值时，地址将添加到禁止列表。

>[!NOTE]
>
>在[投放失败类型](../suppression-list.md#delivery-failures)部分中了解有关错误类型的更多信息。

在默认配置中，阈值设置为以下三个错误：

* 对于同一投放，在第三次遇到错误时，地址被禁止。

* 如果存在不同的投放并且两个错误在至少24小时之间发生，则在每次错误时错误计数递增，并且在第三次尝试时地址也被抑制。

如果重试投放成功，则地址的错误计数会重新初始化。

您可以使用&#x200B;**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**&#x200B;菜单中的&#x200B;**[!UICONTROL Edit]**&#x200B;按钮修改限制阈值。

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## 重试时间段 {#retry-duration}

**重试时间段**&#x200B;是重试投放遇到临时错误或软退件的任何电子邮件的时间段。

默认情况下，自将消息添加到电子邮件队列之后，将对&#x200B;**3.5天**（或&#x200B;**84小时**）执行重试。

但是，为确保不再需要重试尝试，您可以在创建或编辑应用于电子邮件渠道的[消息预设](message-presets.md)时根据需要更改此设置。

例如，对于与密码重置相关并包含仅有效一天的链接的事务型电子邮件，您可以将重试期限设置为24小时。 同样，对于午夜销售，您可能需要定义6小时的重试期限。

>[!NOTE]
>
>重试周期不能超过84小时。 营销电子邮件的最短重试期限为6小时，事务电子邮件的最短重试期限为10分钟。

了解在[此部分](message-presets.md#create-message-preset)中创建消息预设时如何调整电子邮件重试参数。

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->