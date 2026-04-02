---
title: 为历程和营销活动分配优先级分数
description: 了解如何为历程和营销活动分配优先级分数。
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 35%

---

# 分配优先级分数 {#priority}

Journey Optimizer允许您为历程&#x200B;**[!UICONTROL 操作]**&#x200B;活动中的历程、营销活动或入站渠道操作分配优先级分数。

当存在强加的限制（如频率上限）时，优先级对于确定历程、营销活动或操作的优先级至关重要。

如果客户符合许多历程、营销策划或沟通的条件，而您希望选择他们应该输入和接收的内容，则应使用此字段。

## 为历程和营销活动分配优先级分数 {#priority-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="优先级"
>abstract="为该营销活动分配优先级分数。存在频率上限等强加的约束时，优先级对于确定营销活动的优先级至关重要。</br>输入一个数值（从 0 到 100）。请注意，数值越高，优先级越高。对于两个营销活动具有相同优先级分数的情况，将会显示首先激活的营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="优先级"
>abstract="为该历程分配优先级分数。当存在频率上限等强加的约束时，优先级对于确定历程的优先级至关重要。</br>输入一个数值（从 0 到 100）。请注意，数值越高，优先级越高。对于两个历程具有相同优先级分数的情况，将会显示首先激活的历程。"

➡️ [通过观看视频了解此功能](#video)

分配优先级得分对于入站通信（如Web、移动设备和应用程序内）至关重要。 如果您有多个使用相同渠道配置的营销活动（例如，网页顶部的横幅），则可能会出现问题，因为可以尽可能只显示来自一个营销活动的内容。 优先级分数是您插入首选项的位置，当收件人可能有资格参与多个营销活动时，应显示哪个营销活动。

>[!NOTE]
>
>在营销活动中，优先级得分仅适用于Web、应用程序内和基于代码的入站渠道。

要为历程或营销活动分配优先级得分，请在历程或营销活动属性中的&#x200B;**[!UICONTROL 优先级得分]**&#x200B;字段中输入一个数值（从0到100）。 数字越大，优先级越高。

如果您创作此营销活动，并且希望确保显示此营销活动内容，则可以为其指定100分。

![](assets/priority-score.png)

>[!IMPORTANT]
>
>如果两个历程或营销活动具有相同的优先级分数，则系统没有时间分隔机制。 确保优先级得分是唯一的，以避免冲突。

## 为入站频道操作分配优先级分数 {#priority-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="优先级"
>abstract="为该历程操作分配优先级分数。如果有多个历程操作或营销活动使用相同的渠道配置，优先级对于确定入站操作的优先级至关重要。</br>输入一个数值（从 0 到 100）。请注意，数值越高，优先级越高。在默认情况下，操作的优先级分数从历程的总体优先级分数继承。"

Journey Optimizer还允许您在[操作](../building-journeys/journey-action.md)活动中为入站渠道操作分配优先级分数。

这样，当有多个历程操作或营销活动使用相同的渠道配置时，您就可以优先执行集客操作。

>[!NOTE]
>
>在&#x200B;**[!UICONTROL 操作]**&#x200B;活动中，优先级得分仅适用于Web、应用程序内和基于代码的入站渠道。

在&#x200B;**[!UICONTROL 冲突管理]**&#x200B;部分中，默认情况下选中&#x200B;**[!UICONTROL 使用历程优先级]**&#x200B;选项，这意味着操作的优先级分数继承自历程的整体优先级分数。

要为&#x200B;**[!UICONTROL 操作]**&#x200B;活动中定义的集客操作分配优先级得分，请取消选择&#x200B;**[!UICONTROL 使用历程优先级]**&#x200B;选项，然后在&#x200B;**[!UICONTROL 优先级]**&#x200B;字段中输入一个数值（从0到100）。 数字越大，优先级越高。

![](assets/action-journey-priority-score.png){width=70%}

## 操作方法视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3445011?captions=chi_hans&quality=12)
