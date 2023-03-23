---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 集成
description: 了解如何在Journey Optimizer中利用Adobe Analytics数据
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics，集成， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# 使用Adobe Analytics数据 {#analytics-data}

您可以利用您已通过Adobe Analytics或Web SDK捕获并流入Adobe Experience Platform的所有Web行为事件数据，以触发历程并自动化客户体验。

要使此功能与Adobe Analytics配合使用，您必须：

1. 激活要使用的报表包。 [了解详情](#leverage-analytics-data)
1. 允许Journey Optimizer使用您的Adobe Analytics数据源。 [了解详情](#activate-analytics-data)
1. 在历程中添加特定事件。 [了解详情](#event-analytic)

>[!NOTE]
>
>本节仅适用于基于规则的事件以及需要使用Adobe Analytics或Web SDK数据的客户。
> 
>如果您使用的是Adobe Customer Journey Analytics，请参阅 [本页](../reports/cja-ajo.md).

## 配置Adobe Analytics或Web SDK数据 {#leverage-analytics-data}

需要启用来自Adobe Analytics或Adobe Experience Platform Web SDK的数据才能在您的历程中使用。

为此，请执行以下步骤：

1. 浏览到 **[!UICONTROL 源]** 菜单。

1. 在Adobe Analytics部分中，选择 **[!UICONTROL 添加数据]**

   ![](assets/ajo-aa_1.png)

1. 从可用的Adobe Analytics报表包列表中，选择 **[!UICONTROL 报表包]** 启用。 然后，单击 **[!UICONTROL 下一个]**.

   ![](assets/ajo-aa_2.png)

1. 选择要使用默认架构还是自定义架构。

1. 从 **[!UICONTROL 数据流详细信息]** 屏幕，选择 **[!UICONTROL 数据流名称]**.

1. 配置完成后，单击 **[!UICONTROL 完成]**.

   ![](assets/ajo-aa_3.png)

这会为该报表包启用Analytics源连接器。 每当数据传入时，它都会转换为体验事件并发送到Adobe Experience Platform。

![](assets/ajo-aa_4.png)

了解有关Adobe Analytics源连接器的更多信息，请参阅  [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"}.

## 激活此配置 {#activate-analytics-data}

完成此配置后，请联系Adobe以启用Journey Optimizer环境以使用此数据源。 此步骤仅对于Adobe Analytics数据源是必需的。 要执行此操作，请执行以下操作：

1. 获取数据源ID。 此信息在用户界面中可用：浏览到您从 **数据流** 选项卡 **源** 菜单。 找到该源的最简单方法是过滤Adobe Analytics源。
1. 请联系Adobe客户关怀，并提供以下详细信息：

   * 主题：为旅程启用Adobe Analytics事件

   * 内容：请允许我的环境使用AA事件。

      * 组织ID:&quot;XXX@AdobeOrg&quot;

      * 数据源ID:“ID:xxxxx&quot;

1. 确认环境已准备就绪后，即可在历程中使用Adobe Analytics数据。

## 使用Adobe Analytics或Web SDK数据创建包含事件的旅程 {#event-analytics}

您现在可以基于Adobe Analytics或Adobe Experience Platform Web SDK数据创建事件，以用于历程。

在以下示例中，了解如何定位向购物车中添加了产品的用户：

* 如果订单完成，用户将在两天后收到一封跟进电子邮件，要求提供反馈。
* 如果订单未完成，用户将收到一封电子邮件，提醒他们完成订单。

1. 从Adobe Journey Optimizer访问 **[!UICONTROL 配置]** 菜单。

1. 然后，选择 **[!UICONTROL 管理]** 从 **[!UICONTROL 事件]** 卡。

   ![](assets/ajo-aa_5.png)

1. 单击 **[!UICONTROL 创建事件]**. 事件配置窗格将在屏幕右侧打开。

1. 填写 **[!UICONTROL 事件]** 参数：

   * **[!UICONTROL 名称]**:将您的 **[!UICONTROL 事件]**.
   * **[!UICONTROL 类型]**:选择 **[!UICONTROL 单一]** 类型。 [了解详情](../event/about-events.md)
   * **[!UICONTROL 事件ID类型]**:选择 **[!UICONTROL 基于规则]** 事件ID类型。 [了解详情](../event/about-events.md#event-id-type)
   * **[!UICONTROL 架构]**:选择Analytics或WebSDK架构 [创建之前](#leverage-analytics-data).
   * **[!UICONTROL 字段]**:选择有效负荷字段。 [了解详情](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID条件]**:定义条件以识别将触发历程的事件。

      在此，当客户向购物车中添加项目时，将触发事件。
   * **[!UICONTROL 配置文件标识符]**:从有效负载字段中选择一个字段，或定义一个公式，以标识与事件关联的人员。

   ![](assets/ajo-aa_6.png)

1. 配置后，选择 **[!UICONTROL 保存]**.

现在，事件已准备就绪，请创建旅程以使用它。

1. 从 **[!UICONTROL 历程]** ，打开或创建历程。 有关详细信息，请参阅[此部分](../building-journeys/journey-gs.md)。

1. 将您之前配置的Analytics事件添加到您的历程中。

   ![](assets/ajo-aa_8.png)

1. 添加在订单完成时将触发的事件。

1. 从 **[!UICONTROL 事件菜单]**，选择 **[!UICONTROL 定义事件超时]** 和 **[!UICONTROL 设置超时路径]** 选项。

   ![](assets/ajo-aa_9.png)

1. 从超时路径中，添加 **[!UICONTROL 电子邮件]** 操作。 此路径将用于向未完成订单的客户发送电子邮件，提醒他们购物车仍然可用。

1. 添加 **[!UICONTROL 等待]** 活动，并将其设置为所需的持续时间。

   ![](assets/ajo-aa_10.png)

1. 然后，添加 **[!UICONTROL 电子邮件操作]**. 在此电子邮件中，系统将提示客户提供已下单的反馈。

您现在可以测试和发布历程。 [了解详情](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
