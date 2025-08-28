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
source-git-commit: eeacfacf3068f831afb7b7ad78214941a9259c93
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 10%

---

# 计划行动营销活动 {#action-campaign-schedule}

使用&#x200B;**[!UICONTROL 计划]**&#x200B;选项卡定义营销活动计划。

## 设置开始和结束日期

默认情况下，手动激活营销活动后，营销活动便会开始，而发送一次消息后，营销活动便会结束。 如果不想在营销活动激活后立即执行营销活动，则可以使用&#x200B;**[!UICONTROL 营销活动开始]**&#x200B;选项指定发送消息的日期和时间。

利用&#x200B;**[!UICONTROL 营销活动结束]**&#x200B;选项，可指定何时应停止执行营销活动。 在指定的日期之外，将不会执行营销活动。

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>在 [!DNL Adobe Journey Optimizer] 中计划营销活动时，请确保开始日期/时间与所需的首次投放时间一致。对于定期营销活动，如果计划的首次时间已过，则营销活动将根据定期规则滚动到下一个可用时间段。

## 设置速率控制

[!DNL Journey Optimizer]允许您为出站操作（电子邮件、短信、推送通知）启用速率控制。

此功能对于防止下游系统（如登陆页面或客户关怀平台）上的过载特别有用。 例如，您可以将速率限制设置为每秒165条消息，以确保平稳投放而不会淹没下游系统。

要设置速率控制，请在&#x200B;**[!UICONTROL 投放设置]**&#x200B;部分中启用&#x200B;**[!UICONTROL 节流投放]**&#x200B;选项，并指定所需的&#x200B;**[!UICONTROL 每秒投放速率]**。

* 支持的最低投放率：每秒1个。
* 支持的最大投放率：启用“限制投放”选项时，每秒投放2000次。

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>设置投放率时，活动受众可以执行的最长时间范围为12小时。 如果投放率设置为不允许在12小时时间范围内发送消息的所有受众的值，则剩余的用户档案将从营销活动中排除。 您可以在营销活动报告中查看这些排除的用户档案的计数。

## 设置执行频率

对于电子邮件、短信和推送通知操作，您可以定义发送营销活动消息的频率。 为此，请在营销活动创建屏幕中使用&#x200B;**[!UICONTROL 操作触发器]**&#x200B;选项来指定是否应每天、每周或每月执行营销活动。

![](assets/action-triggers.png)

## 设置IP预热计划

对于电子邮件操作，您可以创建特定的IP预热计划激活活动。 营销活动计划将由与之关联的IP预热计划驱动，这意味着不再在营销活动本身中定义计划。 [了解如何创建IP预热营销活动](../configuration/ip-warmup-campaign.md)。

## 后续步骤 {#next}

活动计划就绪后，您可以查看和激活该活动。 [了解详情](review-activate-campaign.md)
