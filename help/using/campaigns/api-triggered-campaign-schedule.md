---
solution: Journey Optimizer
product: journey optimizer
title: 计划API触发的营销活动
description: 了解如何计划API触发的营销活动。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 计划API触发的营销活动 {#api-schedule}

使用&#x200B;**[!UICONTROL 计划]**&#x200B;选项卡定义营销活动计划。

## 设置开始和结束日期

默认情况下，API触发的营销活动在触发后立即开始，在发送消息后立即结束。 如果不想在营销活动触发后立即执行，则可以使用&#x200B;**[!UICONTROL 营销活动开始]**&#x200B;选项指定发送消息的日期和时间。

利用&#x200B;**[!UICONTROL 营销活动结束]**&#x200B;选项，可指定何时应停止执行营销活动。 在指定的日期之外，将不会执行营销活动。

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>在[!DNL Adobe Journey Optimizer]中计划营销活动时，请确保您的开始日期/时间与所需的首次投放一致。

## 设置速率控制

[!DNL Journey Optimizer]允许您为出站操作（电子邮件、短信、推送通知）启用速率控制。

此功能对于防止下游系统（如登陆页面或客户关怀平台）上的过载特别有用。 例如，您可以将速率限制设置为每秒165条消息，以确保平稳投放而不会淹没下游系统。

要设置速率控制，请在&#x200B;**[!UICONTROL 投放设置]**&#x200B;部分中启用&#x200B;**[!UICONTROL 限制投放]**&#x200B;选项，并指定所需的&#x200B;**[!UICONTROL 投放速率]**。

![](assets/throttling-rate-control.png)

## 后续步骤 {#next}

准备好营销活动配置和内容后，即可对其进行查看和激活。 [了解详情](review-activate-campaign.md)
