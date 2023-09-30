---
solution: Journey Optimizer
product: journey optimizer
title: 创建 IP 预热营销活动
description: 了解如何创建IP预热活动
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP 、池、可投放性
hide: true
hidefromtoc: true
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 8%

---

# 创建 IP 预热营销活动 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="激活 IP 预热计划选项"
>abstract="选择此选项后，可以在IP预热计划中使用活动。 然后，促销活动计划将由与之关联的IP预热计划驱动。"

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [IP预热入门](ip-warmup-gs.md)
* **[创建 IP 预热营销活动](ip-warmup-campaign.md)**
* [创建IP预热计划](ip-warmup-plan.md)
* [执行IP预热计划](ip-warmup-execution.md)

>[!ENDSHADEBOX]

在中创建IP预热计划本身之前 [!DNL Journey Optimizer]，您首先需要创建一个或多个启用了专用选项的营销活动，以便在IP预热计划中使用它们。

要创建IP预热活动，请执行以下步骤。

1. 创建 [电子邮件](../email/email-settings.md) 渠道 [曲面](channel-surfaces.md) 用于您已为预热计划标识的域和IP。

   >[!NOTE]
   >
   >了解如何在中选择要在电子邮件平面中使用的域和IP [本节](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >与您的可投放性顾问合作，确定要用于IP预热计划的域和IP。<!--TBC-->

1. 创建 [营销活动](../campaigns/create-campaign.md) 并选择 [电子邮件](../email/create-email.md#create-email-journey-campaign) 操作。

1. 选择为IP预热创建的曲面。

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 计划]** 部分，选择 **[!UICONTROL IP预热计划激活]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   营销活动 [计划](../campaigns/create-campaign.md#schedule) 将由与之关联的IP预热计划驱动，这意味着该计划不再在营销策划本身中定义。

1. 完成创建电子邮件营销活动的步骤，如定义营销活动属性， [受众](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->、和 [内容](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >有关如何配置营销活动的更多信息，请参阅 [此页面](../campaigns/get-started-with-campaigns.md).

1. [激活](../campaigns/review-activate-campaign.md) 营销活动。

   >[!NOTE]
   >
   >对于激活了IP预热计划的实时营销活动， **[!UICONTROL 删除]** 按钮在与IP预热计划关联之前可用。 营销活动一旦用于计划，便无法再删除。

1. 营销策划显示在 **[!UICONTROL 营销活动]** 列表。 要轻松检索在当前沙盒上创建的所有IP预热营销活动，您可以在 **[!UICONTROL IP热身]** 营销活动选项。

   ![](assets/ip-warmup-campaign-filter.png)

活动一旦启用，即可在IP预热计划中使用。 [了解详情](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->
