---
title: 创建短信消息
description: 了解如何在Journey Optimizer中创建短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 15%

---

# 创建短信消息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建短信"
>abstract="添加文本消息，然后使用表达式编辑器对其进行个性化设置。"

一旦 [已创建消息](get-started-content.md)，则使用 **[!UICONTROL SMS]** 选项卡，以定义短信消息的设置和内容。


>[!AVAILABILITY]
>
>目前，短信渠道仅适用于一批组织（限量发布）。有关更多信息，请与您的 Adobe 代表联系。

![](assets/sms_1.png)

如果您是首次创建短信消息，请确保已配置短信渠道。 [了解详情](../configuration/sms-configuration.md)。

## 定义短信内容{#sms-content}

要开始个性化短信消息，请执行以下步骤：

1. 单击 **[!UICONTROL Add text message]** 字段来打开表达式编辑器。

   ![](assets/sms_3.png)

1. 使用表达式编辑器定义内容。 您可以使用任何属性来个性化内容，例如配置文件名称或城市。 在的表达式编辑器中了解有关个性化的更多信息 [此部分](../personalization/personalize.md)

   >[!NOTE]
   >
   > 短信消息最多可包含160个字符，包括空格和换行符。

   ![](assets/sms_2.png)

1. 单击 **[!UICONTROL Save]** 消息准备就绪时。

## 验证短信{#sms-preview}

定义消息内容后，即可使用测试用户档案进行预览和测试。 如果插入 [个性化内容](../personalization/personalize.md)，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

要显示您的短信消息在移动设备上的显示方式，请浏览至 **[!UICONTROL Preview]** 选项卡。

有关详细信息，请参阅[此部分](../design/preview.md)。

## 发布短信 {#sms-publish}

消息准备就绪后，您可以将其发布，以供使用 **[!UICONTROL Publish]** 按钮。 此操作会发布新版本的消息，该消息将用于您的历程中的下一次执行。

您的短信消息现在可用于历程。 [了解如何创建历程](../building-journeys/journey-gs.md).

## 选择启用和选择禁用{#sms-opt-in-out}

对于所有营销消息，短信必须包含一种让收件人轻松退订的方法。 取消订阅后，用户档案将自动从未来营销消息的受众中删除。 对于事务型消息，不必添加退订链接。

短信收件人可以使用选择启用和选择禁用关键词进行回复。 根据行业标准和法规，Adobe Journey Optimizer会自动处理传入消息中的以下关键词：开始、停止和停止。 这些关键词会触发短信提供商的标准自动回复。

要详细了解本机入站关键词支持（开始、停止和停止）如何用于短信，请参阅以下视频。

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

## 操作方法视频

了解如何配置、创作短信消息，并将其包含在客户历程中。

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)

**相关主题**

* [配置短信渠道](../configuration/sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [创建新消息](get-started-content.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
