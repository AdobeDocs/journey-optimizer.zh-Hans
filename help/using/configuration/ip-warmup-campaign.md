---
solution: Journey Optimizer
product: journey optimizer
title: 创建IP预热活动
description: 了解如何创建IP预热活动
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---

# 创建IP预热活动 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="激活IP预热计划选项"
>abstract="选择IP预热计划激活选项。 活动开始后，可以将其与IP预热计划关联。"

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [IP预热入门](ip-warmup-gs.md)
* **[创建IP预热活动](ip-warmup-campaign.md)**
* [创建IP预热计划](ip-warmup-plan.md)
* [运行IP预热计划](ip-warmup-running.md)

>[!ENDSHADEBOX]

您需要创建一个或多个启用了特定选项的营销活动，以便在IP预热计划中使用它们。

要创建IP预热活动，请执行以下步骤。

1. 创建 [曲面](channel-surfaces.md) 用于您已为预热计划标识的域和IP。<!--how do you identify these or who does it at the customer level?-->

1. 创建 [营销活动](../campaigns/create-campaign.md) 并选择 [电子邮件](../email/create-email.md#create-email-journey-campaign) 操作。

1. 选择为IP预热创建的曲面。

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 计划]** 部分，选择 **[!UICONTROL IP预热计划激活]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   营销活动 [计划](../campaigns/create-campaign.md#schedule) 将由与之关联的IP预热计划驱动，这意味着该计划不再在营销策划本身中定义。

1. [激活](../campaigns/review-activate-campaign.md) 营销活动。 一旦启用，它就可以在IP预热计划中使用。

>[!NOTE]
>
>对于激活了IP预热计划的实时营销活动， **[!UICONTROL 删除]** 按钮在与IP预热计划关联之前可用。

有关如何配置营销活动的更多信息，请参阅 [此页面](../campaigns/get-started-with-campaigns.md).

