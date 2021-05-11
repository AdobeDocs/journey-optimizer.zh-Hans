---
title: 监视消息执行
description: 学习监控指南
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 消息监视{#monitor-message-execution}

![](assets/do-not-localize/badge.png)

为确保消息的执行、发送和传递成功，[!DNL Journey Optimizer]优惠功能可监视当前发布和触发的消息。 您可以从&#x200B;**[!UICONTROL Executions]**&#x200B;列表实时查看邮件在旅程<!--and APIs-->中的执行情况。

要访问此列表，请从&#x200B;**[!DNL Journey Optimizer]**&#x200B;主页中选择&#x200B;**[!UICONTROL Messages]**，然后单击&#x200B;**[!UICONTROL Executions]**&#x200B;选项卡。

此选项卡提供两个视图:**[!UICONTROL Live view]**&#x200B;和&#x200B;**[!UICONTROL Global view]**。

* **[!UICONTROL Live view]**&#x200B;选项卡提供了由一个或多个[rourneys](building-journeys/journey.md) **在过去24小时内仅**&#x200B;触发的所有已执行消息&#x200B;**的**&#x200B;实时概述。

   ![](assets/message-execution-tab-live.png)

   此列表每六十秒自动刷新一次。 如果特定消息在过去24小时内未执行，则所有列都将显示该消息的空值(0)。

* **[!UICONTROL Global view]**&#x200B;选项卡提供自消息开始日期&#x200B;**以来由一个或多个[reyreys](building-journeys/journey.md)**&#x200B;触发的所有已执行消息&#x200B;**的概述。**

   ![](assets/message-execution-tab-global.png)

   此列表每九十分钟自动刷新一次。 自每个消息开始日期起，数据随时间进行聚集。

如果某条消息已发布但尚未由某个旅程触发，则它不会列在任何选项卡中。 仅列出以下元素：
* 已触发但尚未启动（待定）的消息。
* 已触发且当前正在运行（进行中）的消息。

对于多通道消息，每个消息显示一行渠道。

![](assets/message-execution-multichannel.png)

如果某条消息已用于多个旅程，则&#x200B;**[!UICONTROL Source]**&#x200B;列将显示&#x200B;**[!UICONTROL Multiple]**。

默认情况下，消息从最近的执行日期开始显示。 单击&#x200B;**[!UICONTROL Filters]**&#x200B;图标，根据渠道、开始日期和/或结束日期搜索消息。

![](assets/message-execution-tab-filters.png)

如果您位于&#x200B;**[!UICONTROL Live view]**&#x200B;中，则<!--**[!UICONTROL Quick action]**-->第二列可打开相应的[消息](create-message.md)并访问[实时报告](reports/live-report.md)；如果您位于&#x200B;**[!UICONTROL Global view]**&#x200B;中，则可访问[全局报告](reports/global-report.md)。

![](assets/message-execution-open-live-report.png)

对于每次消息执行，都会显示许多指示符：

* **[!UICONTROL Message label]**:您在创建消息时定 [义的消息标题](create-message.md)。
* **[!UICONTROL Execution ID]**:自动生成的标识符。
* **[!UICONTROL Source]**:利用该消息的旅程名称。
* **[!UICONTROL Start date]**:从旅程执行消息的日期和时间。
* **[!UICONTROL Excluded]**:由于排除规则而从初始目标中排除的用户档案数。
* **[!UICONTROL Sent]**:已发送的消息数。
* **[!UICONTROL Delivered]**:在收件人的邮箱（电子邮件）或设备（推送）中成功传递的邮件数，而不生成弹回或任何其他投放错误。
* **[!UICONTROL Bounces]**:由于投放失败而无法传递的消息数。[进一步了解弹回](suppression-lists.md#delivery-failures)。
* **[!UICONTROL Opens]**:已打开的消息数。
* **[!UICONTROL Clicks]**:电子邮件中链接的点击次数。

   >[!NOTE]
   >
   >推送通知不存在单击：当用户单击推送通知时，会打开应用程序，该应用程序只能视为打开。

* **[!UICONTROL Errors]**:由于技术故障而无法发送的消息数。

单击每个超链接将打开相应的消息摘要视图。 [了解有关消息的更多信息](create-message.md)。
