---
title: 创建直邮消息
description: 了解如何在Journey Optimizer中创建直邮消息
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 直邮、消息、营销活动
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 18%

---

# 创建直邮消息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直邮创建"
>abstract="在计划的营销活动中创建直邮，并设计直邮提供商向您的客户发送邮件所需的提取文件。"

要创建直邮消息，请创建计划的营销活动，并配置提取文件。 直邮提供商需要此文件向客户发送邮件。

>[!IMPORTANT]
>
>在创建直邮消息之前，请确保已配置：
>
>1. A [文件路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 指定提取文件应上载和存储的服务器，
>1. A [直邮消息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 将引用文件路由配置。


## 创建直邮营销活动{#create-dm-campaign}

要创建直邮营销活动，请执行以下步骤：

1. 创建新的计划活动，然后选择 **[!UICONTROL 直邮]** 作为操作。

1. 选择 **[!UICONTROL 直邮表面]** ，然后单击 **[!UICONTROL 创建]**. [了解如何创建直邮表面](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. 在 **[!UICONTROL 属性]** 部分，编辑您的营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

1. 要定义目标受众，请单击 **[!UICONTROL 选择受众]** 按钮进行选择，然后从可用的Adobe Experience Platform受众中进行选择。 [了解详情](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >目前，受众选择限制为300万个配置文件。 根据向Adobe代表提出的请求，可取消此限制。

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择相应的命名空间以标识所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. 营销活动可以计划为特定日期，也可以设置为定期重复。 了解如何配置 **[!UICONTROL 计划]** 中的促销活动 [本节](../campaigns/create-campaign.md#schedule).

您现在可以开始配置要发送给直邮提供商的提取文件。

## 配置提取文件 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="数据字段"
>abstract="添加并配置要在直邮提供商将电子邮件发送到您的客户时所需的提取文件中显示的列和信息。最多可以添加 50 个列。"

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="提取文件格式"
>abstract="对于每个字段，使用表达式编辑器指定一个标签和要显示的信息。<br/><br/>通过<b>排序方式</b>选项，可使用所选字段为提取文件的列排序。"

1. 配置要在提取文件中显示的列和信息：

   1. 单击 **[!UICONTROL 添加]** 按钮以创建新列。

   1. 此 **[!UICONTROL 格式化]** 窗格显示在右侧，允许您设置选定的列。 指定 **[!UICONTROL 标签]** 用于列。

   1. 在 **[!UICONTROL 数据]** 字段中，选择要显示的配置文件属性， [表达式编辑器](../personalization/personalization-build-expressions.md).

   1. 要使用列对提取文件排序，请选择该列并打开 **[!UICONTROL 排序方式]** 选项。 此 **[!UICONTROL 排序方式]** 图标显示在中的列标签旁边 **[!UICONTROL 数据字段]** 部分。







直邮提供商需要使用提取文件向客户发送邮件。 要定义提取文件配置，请执行以下步骤：

1. 在Campaign配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮以配置提取文件内容。

1. 调整提取文件属性：

   1. 指定所需的 **[!UICONTROL 文件名]** 提取文件。

   1. （可选）启用 **[!UICONTROL 附加时间戳以导出文件名]** 选项。

   1. 有时您可能需要在提取文件的开头或结尾添加信息。要执行此操作，请使用 **[!UICONTROL 注释]** 字段，然后指定是否要以页眉或页脚形式包含注释。

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. 配置要在提取文件中显示的列和信息：

   1. 单击 **[!UICONTROL 添加]** 按钮以创建新列。

   1. 此 **[!UICONTROL 格式化]** 窗格显示在右侧，允许您设置选定的列。 指定 **[!UICONTROL 标签]** 用于列。

   1. 在 **[!UICONTROL 数据]** 字段中，选择要显示的配置文件属性， [表达式编辑器](../personalization/personalization-build-expressions.md).

   1. 要使用列对提取文件排序，请选择该列并打开 **[!UICONTROL 排序方式]** 选项。 此 **[!UICONTROL 排序方式]** 图标显示在中的列标签旁边 **[!UICONTROL 数据字段]** 部分。

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. 重复这些步骤以根据需要为提取文件添加任意数量的列。 请注意，最多可添加50列。

      要更改列的位置，请将其拖放到中所需的位置 **[!UICONTROL 数据字段]** 部分。 要删除列，请选择该列并单击 **[!UICONTROL 移除]** 中的按钮 **[!UICONTROL 格式化]** 窗格。

您现在可以测试直邮消息并将其发送给受众。 [了解如何测试和发送直邮消息](test-send-direct-mail.md)
