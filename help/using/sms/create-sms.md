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
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 13%

---

# 创建短信消息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建短信消息"
>abstract="添加您的 SMS 消息，并使用表达式编辑器开始对其进行个性化设置。"

## 添加短信消息 {#create-sms-journey-campaign}

浏览以下选项卡，了解如何在营销活动或历程中添加短信消息。

>[!BEGINTABS]

>[!TAB 向历程添加短信消息]

1. 打开您的历程，然后从拖放短信活动 **操作** 面板的部分。

   ![](assets/sms_create_1.png)

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。

   ![](assets/sms_create_2.png)

   有关如何配置旅程的更多信息，请参阅 [此页面](../building-journeys/journey-gs.md)

   此 **[!UICONTROL 表面]** 默认情况下，字段已预填充，用户将使用最后一个表面用于该渠道。

您现在可以从以下位置开始设计短信消息的内容 **[!UICONTROL 编辑内容]** 按钮。 [定义短信内容](#sms-content)

>[!TAB 向营销活动添加短信消息]

1. 创建新的计划活动或API触发的活动，选择 **[!UICONTROL 短信]** 作为您的操作，然后选择 **[!UICONTROL 应用程序表面]** 以使用。 [了解有关短信配置的更多信息](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 属性]** 部分，编辑营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

   ![](assets/sms_create_4.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪短信消息中链接的点击次数。

1. 单击 **[!UICONTROL 选择受众]** 按钮，从可用的Adobe Experience Platform区段列表中定义要定位的受众。 [了解详情](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身份命名空间]** 字段，选择要使用的命名空间，以标识所选区段中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 营销活动设计为按特定日期或重复频率执行。 了解如何配置 **[!UICONTROL 计划]** 中的促销活动 [本节](../campaigns/create-campaign.md#schedule).

1. 从 **[!UICONTROL 操作触发器]** 菜单，选择 **[!UICONTROL 频率]** 短信消息的：

   * 一次
   * 每日
   * 每周
   * 月

您现在可以从以下位置开始设计短信消息的内容 **[!UICONTROL 编辑内容]** 按钮。 [设计短信内容](#sms-content)

>[!ENDTABS]

## 定义短信内容{#sms-content}

1. 在历程或营销策划配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮以配置短信内容。

1. 单击 **[!UICONTROL 消息]** 用于打开表达式编辑器的字段。

   ![](assets/sms-content.png)

1. 使用表达式编辑器定义内容并添加动态内容。 您可以使用任何属性，例如配置文件名称或城市。 详细了解 [个性化](../personalization/personalize.md) 和 [动态内容](../personalization/get-started-dynamic-content.md) 在表达式编辑器中。

1. 定义内容后，您可以将跟踪URL添加到消息中。 为此，请访问 **[!UICONTROL 辅助函数]** 菜单并选择 **[!UICONTROL 辅助程序]**.

   请注意，要使用URL缩短功能，您必须首先配置子域，然后该子域将链接到您的表面。 [了解详情](sms-subdomains.md)

   >[!CAUTION]
   >
   > 要访问和编辑SMS子域，您必须具有 **[!UICONTROL 管理短信子域]** 生产沙盒的权限。

   ![](assets/sms_tracking_1.png)

1. 在 **[!UICONTROL 辅助函数]** 菜单，单击 **[!UICONTROL URL函数]** 然后选择 **[!UICONTROL 添加URL]**.

   ![](assets/sms_tracking_2.png)

1. 在 `originalUrl` 字段中，粘贴要缩短的URL。

1. 单击 **[!UICONTROL 保存]** 并在预览中查看您的消息。 您可以使用 **[!UICONTROL 模拟内容]** 以预览缩短的URL或个性化内容。

   ![](assets/sms-content-preview.png)

您现在可以测试短信消息并将其发送给受众。 [了解详情](send-sms.md)
发送后，您可以在促销活动或历程报表中衡量短信的影响。 有关报告的更多信息，请参考[此章节](../reports/campaign-global-report.md#sms-tab)。

>[!NOTE]
>
>根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。要实现此目的，短信收件人可以使用选择启用和选择禁用关键词进行回复。 [了解如何管理选择退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**相关主题**

* [预览、测试和发送短信消息](send-sms.md)
* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销策划中添加消息](../campaigns/create-campaign.md)
