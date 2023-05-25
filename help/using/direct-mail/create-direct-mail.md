---
title: 创建直邮消息
description: 了解如何在Journey Optimizer中创建直邮消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直邮、邮件、营销活动
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
badge: label="Beta" type="Informative"
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---

# 创建直邮消息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直邮创建"
>abstract="在计划的营销活动中创建直邮，并设计直邮提供商向您的客户发送邮件所需的提取文件。"

>[!BEGINSHADEBOX]

本文档包括以下内容：

* **[创建直邮](create-direct-mail.md)**
* [配置直邮](direct-mail-configuration.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>直邮目前是私人测试版，可能会频繁更新，恕不另行通知。

直邮是一种离线渠道，允许您对直邮提供商向客户发送邮件所需的提取文件进行个性化和生成。

在创建直邮时，Journey Optimizer会生成一个文件，其中包含所有定向的用户档案和所选数据（例如邮政地址、用户档案属性）。 然后，您的直邮提供商将能够检索该文件，并负责实际发送。

直邮消息只能在计划的营销活动的上下文中创建。 它们不可用于API触发的营销活动或历程。

>[!IMPORTANT]
>
>在发送直邮消息之前，请确保已配置：
>
>1. A [文件路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 指定应将提取文件上传和存储到的服务器，
>1. A [直邮消息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 将引用文件路由配置。


## 创建直邮消息 {#create}

创建和发送直邮消息的步骤如下：

1. 创建新的计划活动，选择 **[!UICONTROL 直邮]** 作为您的操作，然后选择要使用的渠道界面。 [了解如何创建直邮表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. 单击 **[!UICONTROL 创建]** 然后定义有关促销活动的基本信息（名称、描述）。 [了解如何配置营销活动](../campaigns/create-campaign.md)

1. 单击 **[!UICONTROL 编辑内容]** 按钮以配置要发送到直邮提供商的提取文件。

1. 在中定义提取文件的名称 **[!UICONTROL 文件名]** 字段。

   有时您可能需要在提取文件的开头或结尾添加信息。要执行此操作，请使用 **[!UICONTROL 注释]** 字段，然后指定是否要包含注释作为页眉或页脚。

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. 使用左侧区域定义要作为列显示在提取文件中的信息：

   1. 单击 **[!UICONTROL 添加]** 按钮以添加新列，然后从列表中选择该列。

   1. 在 **[!UICONTROL 格式化]** 部分，为列指定标签，然后使用定义要显示的配置文件属性 [表达式编辑器](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. 要使用选定的列对提取文件排序，请切换 **[!UICONTROL 排序方式]** 选项启用。 此 **[!UICONTROL 排序方式]** 图标随后将显示在文件结构中列的标签旁边。

1. 重复这些步骤，根据需要添加任意数量的列来构建提取文件。 请注意，您最多可以添加50列。

   您可以随时删除列，方法是选择列并单击 **[!UICONTROL 移除]** 按钮来自 **[!UICONTROL 格式化]** 部分。

   ![](assets/direct-mail-complete.png)

1. 定义直邮内容后，完成营销活动的配置。

   当营销活动开始时，将自动生成提取文件并将其导出到中指定的服务器。 [文件路由配置](../direct-mail/direct-mail-configuration.md).
