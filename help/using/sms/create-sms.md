---
solution: Journey Optimizer
product: journey optimizer
title: 创建短信消息
description: 了解如何在Journey Optimizer中创建短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 13%

---

# 创建短信消息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建短信"
>abstract="添加文本消息，然后使用表达式编辑器对其进行个性化设置。"

>[!NOTE]
>
>根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。为此，短信收件人可以使用选择加入和选择退出关键词进行回复。 [了解如何管理选择退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## 在历程或营销策划中创建短信消息 {#create-sms-journey-campaign}

要开始个性化短信消息，请执行以下步骤：

>[!BEGINTABS]

>[!TAB 向历程添加短信消息]

1. 打开您的历程，然后从面板的操作部分拖放短信活动。

   ![](assets/sms_create_1.png)

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。

   ![](assets/sms_create_2.png)

   有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md)

您现在可以从 **[!UICONTROL 编辑内容]** 按钮。 [设计短信内容](#sms-content)

>[!TAB 向营销活动添加短信消息]

1. 创建新的计划营销活动或API触发的营销活动，选择 **[!UICONTROL 短信]** 作为您的操作，然后选择 **[!UICONTROL 应用程序界面]** 。 [了解有关短信配置的更多信息](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 属性]** ，编辑营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

   ![](assets/sms_create_4.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否跟踪短信消息中链接的点击量。

1. 单击 **[!UICONTROL 选择受众]** 按钮，以从可用的Adobe Experience Platform区段列表中定义要定位的受众。 [了解详情](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL 计划]** 在 [此部分](../campaigns/create-campaign.md#schedule).

1. 从 **[!UICONTROL 操作触发器]** 菜单，选择 **[!UICONTROL 频率]** 短信消息：

   * 一次
   * 每日
   * 每周
   * 月

您现在可以从 **[!UICONTROL 编辑内容]** 按钮。 [设计短信内容](#sms-content)

>[!ENDTABS]

## 定义短信内容{#sms-content}

1. 在历程或营销活动配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮来配置短信内容。

1. 单击 **[!UICONTROL 消息]** 字段来打开表达式编辑器。

   ![](assets/sms-content.png)

1. 使用表达式编辑器定义内容并添加动态内容。 您可以使用任何属性，如配置文件名称或城市。 详细了解 [个性化](../personalization/personalize.md) 和 [动态内容](../personalization/get-started-dynamic-content.md) 在表达式编辑器中。

1. 单击 **[!UICONTROL 保存]** 并在预览中查看您的消息。 [了解详情](send-sms.md)

   ![](assets/sms-content-preview.png)

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [在历程中添加消息](../building-journeys/journeys-message.md)
