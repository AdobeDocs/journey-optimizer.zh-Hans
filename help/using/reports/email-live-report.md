---
title: 通过电邮发送实时报告
description: 了解如何使用电子邮件实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---

# 通过电邮发送实时报告 {#email-live-report}

电子邮件&#x200B;**[!UICONTROL Live report]**&#x200B;仅定向特定的电子邮件投放。

从&#x200B;**[!UICONTROL Messages]**&#x200B;菜单的&#x200B;**[!UICONTROL Executions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Live view]** ，然后从选定投放的高级菜单中选择&#x200B;**[!UICONTROL Live report]**。

![](../assets/live_report.png)

电子邮件&#x200B;**[!UICONTROL Live report]**&#x200B;分为不同的小组件，用于详细描述投放成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅此[部分](live-report.md#modify-dashboard)。

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** 和小 **[!UICONTROL Email summary]** 组件使用图表和KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

**[!UICONTROL Sending Statistics]**&#x200B;图表详细列出了交付的成功情况：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](../assets/live_report_6.png)

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

**[!UICONTROL Bounce Reasons]**&#x200B;和&#x200B;**[!UICONTROL Bounce categories]**&#x200B;小组件包含与弹回消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

>[!NOTE]
>
>在消息发送过程中，将排除状态为&#x200B;**[!UICONTROL Suppressed]**&#x200B;或&#x200B;**[!UICONTROL Not allowed]**&#x200B;的用户档案。 因此，虽然&#x200B;**历程报表**&#x200B;会将这些用户档案显示为已在历程（[读取区段](../building-journeys/read-segment.md)和[消息](../building-journeys/journeys-message.md)活动）中移动，但&#x200B;**电子邮件报表**&#x200B;不会在&#x200B;**[!UICONTROL Sent]**&#x200B;量度中包含这些用户档案，因为在发送电子邮件之前已将它们过滤掉。
>
>了解有关[抑制列表](../suppression-list.md)和[允许列表](../allow-list.md)的更多信息。 要找出所有排除案例的原因，您可以使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
