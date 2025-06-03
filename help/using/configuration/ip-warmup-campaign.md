---
solution: Journey Optimizer
product: journey optimizer
title: 创建 IP 预热营销活动
description: 了解如何创建IP预热活动
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP 、池、可投放性
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---

# 创建 IP 预热营销活动 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="激活 IP 预热计划选项"
>abstract="选择此选项后，可以在 IP 预热计划中使用营销活动。然后将由与其关联的 IP 预热计划推动营销活动计划。"

在[!DNL Journey Optimizer]中创建IP预热计划本身之前，首先需要创建一个或多个专门用于IP预热计划<!--through a dedicated option-->的营销活动。

要创建IP预热活动，请执行以下步骤。

1. 为域以及您为预热计划标识的IP创建电子邮件渠道[配置](channel-surfaces.md)。

   与您的可投放性顾问合作，确定要使用的域和IP。 在[本节](../email/email-settings.md#subdomains-and-ip-pools)中了解如何在电子邮件配置中选择它们。

   >[!CAUTION]
   >
   >在IP预热计划[启动](ip-warmup-execution.md)后不要编辑电子邮件渠道配置。

1. 创建计划的营销[营销活动](../campaigns/create-campaign.md)并选择[电子邮件](../email/create-email.md#create-email-journey-campaign)操作。

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. 选择为IP预热创建的配置。

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same configuration as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从&#x200B;**[!UICONTROL 计划]**&#x200B;部分中，选择&#x200B;**[!UICONTROL IP预热计划激活]**。

   ![](assets/ip-warmup-campaign-plan-activation.png)

   营销活动[计划](../campaigns/create-campaign.md#schedule)将由与之关联的IP热备计划驱动，这意味着不再在营销活动本身中定义该计划。

1. 完成创建电子邮件营销活动的步骤，如定义营销活动属性、[受众](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->和[内容](../email/get-started-email-design.md#key-steps)。

   >[!IMPORTANT]
   >
   >IP预热活动中允许的受众必须基于[区段](../audience/creating-a-segment-definition.md)，并使用[默认合并策略](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/merge-policies/overview#default-merge-policy){target="_blank"}创建。

   有关如何配置营销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

1. [激活](../campaigns/review-activate-campaign.md)营销活动。 其状态更改为&#x200B;**[!UICONTROL 实时]**。

   >[!NOTE]
   >
   >不应在IP预热计划上使用[业务规则](../conflict-prioritization/rule-sets.md#apply-frequency-rule)。 应用这些规则可能会妨碍达到营销活动所需数量的定向用户档案。

   对于激活了IP预热计划的实时营销活动，**[!UICONTROL 删除]**&#x200B;按钮可用，直到它与IP预热计划关联为止。 营销活动一旦用于计划，便无法再删除。

1. 该营销活动显示在&#x200B;**[!UICONTROL 营销活动]**&#x200B;列表中。 要轻松检索在当前沙盒上创建的所有IP预热营销活动，您可以对&#x200B;**[!UICONTROL IP预热营销活动]**&#x200B;营销活动选项进行过滤。

   ![](assets/ip-warmup-campaign-filter.png)

活动一旦启用，即可在IP预热计划中使用。 [了解详情](ip-warmup-plan.md)

IP预热活动只能用于一个IP预热计划。 但是，同一IP预热计划的一个或多个阶段中可以使用相同的活动。 [了解详情](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>在IP预热计划中使用实时营销活动时，当计划标记为[已完成](ip-warmup-execution.md#mark-as-completed)后，该营销活动的状态将更改为&#x200B;**[!UICONTROL 已停止]**。

