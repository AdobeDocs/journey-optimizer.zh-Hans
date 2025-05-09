---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 集成
description: 了解如何在Journey Optimizer中利用Adobe Analytics数据
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analytics，集成， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 0be35e14dba32523a7f28aaaa28d41ee693d44ba
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 5%

---

# 使用Adobe Analytics数据 {#analytics-data}

您可以利用已通过Adobe Analytics或Web SDK捕获并流式传输到Adobe Experience Platform中的所有Web行为事件数据，以触发历程并自动化客户体验。

要使此功能与Adobe Analytics配合使用，您必须：

1. 激活要使用的报表包。 [了解详情](#leverage-analytics-data)
1. 启用Journey Optimizer以使用您的Adobe Analytics数据源。 [了解详情](#activate-analytics-data)
1. 在历程中添加特定事件。 [了解详情](#event-analytic)

>[!NOTE]
>
>本节仅适用于需要使用Adobe Analytics或Web SDK数据的基于规则的事件和客户。
> 
>如果您使用的是Adobe Customer Journey Analytics，请参阅[此页面](../reports/cja-ajo.md)。
>

## 配置Adobe Analytics或Web SDK数据 {#leverage-analytics-data}

您需要启用来自Adobe Analytics或Adobe Experience Platform Web SDK的数据才能在历程中使用。

为此，请执行以下步骤：

1. 浏览到&#x200B;**[!UICONTROL 源]**&#x200B;菜单。

1. 在Adobe Analytics部分中，选择&#x200B;**[!UICONTROL 添加数据]**

   ![](assets/ajo-aa_1.png)

1. 从可用Adobe Analytics报表包列表中，选择要启用的&#x200B;**[!UICONTROL 报表包]**。 然后，单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/ajo-aa_2.png)

1. 选择您要使用默认架构还是自定义架构。

1. 从&#x200B;**[!UICONTROL 数据流详细信息]**&#x200B;屏幕中选择&#x200B;**[!UICONTROL 数据流名称]**。

1. 配置完成后，单击&#x200B;**[!UICONTROL 完成]**。

   ![](assets/ajo-aa_3.png)

这将启用该报表包的Analytics Source Connector。 无论何时收到数据，这些数据都会转换为Experience事件并发送到Adobe Experience Platform中。

![](assets/ajo-aa_4.png)

请参阅[Adobe Analytics文档](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"}和[教程](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"}以了解有关Adobe Experience Platform源连接器的更多信息。

## 激活此配置 {#activate-analytics-data}

完成此配置后，请与Adobe联系以允许Journey Optimizer环境使用此数据源。 只有Adobe Analytics数据源才需要此步骤。 要执行此操作，请执行以下操作：

1. 获取数据源ID。 以下信息可在用户界面中找到：浏览到您从&#x200B;**源**&#x200B;菜单的&#x200B;**数据流**&#x200B;选项卡创建的数据源。 找到该子域的最简单方法是筛选Adobe Analytics源。
1. 请联系Adobe客户关怀团队，并提供以下详细信息：

   * 主题：为历程启用Adobe Analytics事件

   * 内容：请启用我的环境以使用AA事件。

      * 组织ID： &quot;XXX@AdobeOrg&quot;

      * 数据源ID： &quot;ID： xxxxx&quot;

1. 在确认环境已就绪后，您可以在历程中使用Adobe Analytics数据。

## 使用Adobe Analytics或Web SDK数据创建包含事件的旅程 {#event-analytics}

您现在可以基于要在历程中使用的Adobe Analytics或Adobe Experience Platform Web SDK数据创建事件。

在以下示例中，了解如何定位将产品添加到购物车的用户：

* 如果订单已完成，用户将在两天后收到一封后续电子邮件，要求您提供反馈。
* 如果订单未完成，用户会收到一封电子邮件，提醒他们完成订单。

1. 从Adobe Journey Optimizer访问&#x200B;**[!UICONTROL 配置]**&#x200B;菜单。

1. 然后，从&#x200B;**[!UICONTROL 事件]**&#x200B;信息卡中选择&#x200B;**[!UICONTROL 管理]**。

   ![](assets/ajo-aa_5.png)

1. 单击&#x200B;**[!UICONTROL 创建事件]**。 事件配置窗格将在屏幕右侧打开。

1. 填写&#x200B;**[!UICONTROL Event]**&#x200B;参数：

   * **[!UICONTROL 名称]**：个性化设置&#x200B;**[!UICONTROL 事件]**&#x200B;的名称。
   * **[!UICONTROL 类型]**：选择&#x200B;**[!UICONTROL 单一]**&#x200B;类型。 [了解详情](../event/about-events.md)
   * **[!UICONTROL 事件ID类型]**：选择基于&#x200B;**[!UICONTROL 规则的]**&#x200B;事件ID类型。 [了解详情](../event/about-events.md#event-id-type)
   * **[!UICONTROL 架构]**：选择在[&#128279;](#leverage-analytics-data)之前创建的Analytics或WebSDK架构。
   * **[!UICONTROL 字段]**：选择有效负载字段。 [了解详情](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID条件]**：定义条件以识别将触发历程的事件。

     在此，当客户将商品添加到其购物车时，会触发事件。
   * **[!UICONTROL 配置文件标识符]**：从有效负载字段中选择一个字段或定义一个公式，以标识与事件关联的人员。

   ![](assets/ajo-aa_6.png)

1. 配置后，选择&#x200B;**[!UICONTROL 保存]**。

现在事件已准备就绪，请创建历程以使用它。

1. 从&#x200B;**[!UICONTROL 历程]**&#x200B;菜单中，打开或创建旅程。 有关详细信息，请参阅[此部分](../building-journeys/journey-gs.md)。

1. 将您之前配置的Analytics事件添加到您的历程。

   ![](assets/ajo-aa_8.png)

1. 添加一个事件，订购完成后将触发该事件。

1. 从&#x200B;**[!UICONTROL 事件菜单]**&#x200B;中，选择&#x200B;**[!UICONTROL 定义事件超时]**&#x200B;和&#x200B;**[!UICONTROL 设置超时路径]**&#x200B;选项。

   ![](assets/ajo-aa_9.png)

1. 从超时路径中，添加&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作。 此路径将用于向未完成订单的客户发送电子邮件，提醒他们购物车仍然可用。

1. 在主路径后添加&#x200B;**[!UICONTROL 等待]**&#x200B;活动，并将其设置为所需的持续时间。

   ![](assets/ajo-aa_10.png)

1. 然后，添加&#x200B;**[!UICONTROL 电子邮件操作]**。 在该电子邮件中，系统将提示客户对所下订单提供反馈。

您现在可以测试和发布历程。 [了解详情](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
