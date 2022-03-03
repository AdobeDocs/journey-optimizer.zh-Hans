---
title: 通过电邮发送实时报告
description: 了解如何使用电子邮件实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: fad7eb9feea0d8c21494b4a7c1608369e725023e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# 通过电邮发送实时报告 {#email-live-report}

电子邮件 **[!UICONTROL Live report]** 仅定向特定电子邮件投放。

从 **[!UICONTROL Executions]** 选项卡 **[!UICONTROL Messages]** 菜单，选择 **[!UICONTROL Live view]** 然后，从选定投放的高级菜单中选择 **[!UICONTROL Live report]**.

![](assets/live_report.png)

电子邮件 **[!UICONTROL Live report]** 会分为不同的小组件，用于详细描述投放的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅 [部分](live-report.md#modify-dashboard).

![](assets/live_report_5.png)

**[!UICONTROL Email performance]** 和 **[!UICONTROL Email summary]** 小组件使用图表和KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Targeted]**:符合此投放目标用户档案的用户配置文件数。

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Spam complaints]**:分类为垃圾邮件的邮件数。

* **[!UICONTROL Unsubscriptions]**:退订链接的点击次数。

* **[!UICONTROL Excluded]**:未收到消息的从定向用户档案中排除的用户用户档案数。

的 **[!UICONTROL Sending Statistics]** 小组件详细介绍您交付的成功：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](assets/live_report_6.png)

的 **[!UICONTROL Error Reasons]** 通过图表和表格，可查看在投放期间发生的错误。

的 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

<!--
![](assets/live_report_8.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.
-->
>[!NOTE]
>
>具有 **[!UICONTROL Suppressed]** 或 **[!UICONTROL Not allowed]** 在消息发送过程中，状态将被排除。 因此，当 **历程报表** 会将这些用户档案显示为已在历程([读取区段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) ) **电子邮件报表** 将不会在 **[!UICONTROL Sent]** 量度，因为在发送电子邮件之前，这些量度会被过滤掉。
>
>了解 [禁止列表](../messages/suppression-list.md) 和 [允许列表](../messages/allow-list.md). 要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
