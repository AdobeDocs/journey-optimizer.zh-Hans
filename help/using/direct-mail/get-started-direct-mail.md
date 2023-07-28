---
title: 直邮入门
description: 了解如何在Journey Optimizer中创建和直邮消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直邮、消息、营销活动
source-git-commit: 40cd058475b37b8fa7d5c0286ad230422e027cf8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# 创建直邮消息 {#create-direct}

>[!AVAILABILITY]
>
>目前，直邮渠道不适用于已购买AdobeHealthcare Shield附加产品的组织。

直邮是一种离线渠道，允许您个性化并生成直邮提供商向客户发送邮件所需的提取文件。

在创建直邮营销活动时，Journey Optimizer会自动生成一个文件，其中包含所有定向的用户档案和选定数据，如邮政地址和用户档案属性。 此文件将发送到您选择的服务器，以便您选择的直邮提供商可以访问该文件，该提供商将为您处理实际的邮寄过程。

发送直邮消息的主要步骤如下：

![](assets/dm-creation-process.png)

直邮消息只能在计划的营销活动的上下文中创建。 它们不可用于API触发的营销活动或历程。

>[!IMPORTANT]
>
>在发送直邮消息之前，请确保已配置：
>
>1. A [文件路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 指定提取文件应上载和存储的服务器，
>1. A [直邮消息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 将引用文件路由配置。
