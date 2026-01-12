---
solution: Journey Optimizer
product: journey optimizer
title: 在消息优化中使用试验
description: 了解如何使用内容实验来测试多个内容版本并确定哪个版本的效果最佳。
role: User
level: Intermediate
keywords: 试验，优化， A/B测试，内容试验，处理
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# 使用试验 {#experimentation}

>[!NOTE]
>
>此页面概述了如何在内容优化中使用试验。 有关内容试验（包括配置选项、量度和分析）的详细信息，请参阅[内容试验文档](../content-management/get-started-experiment.md)。

通过试验可测试多个内容版本，以确定哪些版本基于预定义的成功量度表现最佳。

要设置试验，请执行以下步骤。

假设您想在营销活动中测试以下促销消息：

* **待遇A**：“下次购买享受20%的优惠”
* **待遇B**：“超过$50美元的订单免运费”
* **待遇C**：“获取10美元的礼品卡”

要设置实验并确定哪些消息可带来最多的购买，请执行以下步骤。

1. 创建[历程](../building-journeys/journey-gs.md#jo-build)或[营销活动](../campaigns/create-campaign.md)。

   >[!NOTE]
   >
   >如果您在历程中，请添加&#x200B;**[!UICONTROL 操作]**&#x200B;活动，选择一个渠道活动，然后选择&#x200B;**[!UICONTROL 配置操作]**。 [了解详情](../building-journeys/journey-action.md#add-action)

1. 从&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡中，选择两个入站操作，例如[基于代码的体验](../code-based/get-started-code-based.md)和[应用程序内体验](../../rp_landing_pages/in-app-landing-page.md)。

1. 在&#x200B;**[!UICONTROL 优化]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 创建试验]**。

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. 根据需要设计和配置内容试验。 [了解如何操作](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   定义试验后，该试验将应用于在该营销活动中或通过历程&#x200B;**[!UICONTROL 操作]**&#x200B;活动插入的所有操作，这意味着相同的客户可以在所有表面看到相同的选件。

   >[!NOTE]
   >
   >您可以选择其他操作：试验适用于添加到营销策划或历程[操作活动](../building-journeys/journey-action.md)的所有操作。

1. [激活](review-activate-campaign.md)您的历程或营销活动。

历程/营销活动上线后，将随机为用户分配不同的内容变体。 [!DNL Journey Optimizer]跟踪哪些变体可推动更多购买，并提供可操作的见解。

使用[历程](../reports/journey-global-report-cja.md)和[营销活动](../reports/campaign-global-report-cja-experimentation.md)报告关注营销活动成功与否。<!--Link to Experimentation journey reportis missing-->

