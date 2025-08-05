---
solution: Journey Optimizer
product: journey optimizer
title: 计划行动营销活动
description: 了解如何计划行动营销活动。
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 创建，优化器，营销活动，界面，消息
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 16%

---

# 计划行动营销活动 {#action-campaign-schedule}

使用&#x200B;**[!UICONTROL 计划]**&#x200B;选项卡定义营销活动计划。

默认情况下，手动激活营销活动后，营销活动便会开始，而发送一次消息后，营销活动便会结束。 如果不想在营销活动激活后立即执行营销活动，则可以使用&#x200B;**[!UICONTROL 营销活动开始]**&#x200B;选项指定发送消息的日期和时间。

利用&#x200B;**[!UICONTROL 营销活动结束]**&#x200B;选项，可指定何时应停止执行营销活动。 在指定的日期之外，将不会执行营销活动。

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>在 [!DNL Adobe Journey Optimizer] 中计划营销活动时，请确保开始日期/时间与所需的首次投放时间一致。对于定期营销活动，如果计划的首次时间已过，则营销活动将根据定期规则滚动到下一个可用时间段。

根据活动渠道，还提供其他计划选项：

* **频率**（电子邮件、短信、推送操作）

  您可以定义营销活动消息的发送频率。 为此，请在营销活动创建屏幕中使用&#x200B;**[!UICONTROL 操作触发器]**&#x200B;选项来指定是否应每天、每周或每月执行营销活动。

* **IP预热计划激活**（电子邮件）

  对于电子邮件营销活动，您可以创建特定的IP预热计划激活营销活动。 营销活动计划将由与之关联的IP预热计划驱动，这意味着不再在营销活动本身中定义计划。 [了解如何创建IP预热营销活动](../configuration/ip-warmup-campaign.md)。

## 后续步骤 {#next}

活动计划就绪后，您可以查看和激活该活动。 [了解详情](review-activate-campaign.md)
