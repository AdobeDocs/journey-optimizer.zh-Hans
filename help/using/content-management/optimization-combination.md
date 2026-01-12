---
solution: Journey Optimizer
product: journey optimizer
title: 将定位与试验相结合
description: 了解如何在单个历程或营销活动中结合定位和实验，以创建复杂的优化策略。
role: User
level: Intermediate
keywords: 优化，定位，试验，组合，高级
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# 将定位与试验相结合 {#combination}

Journey Optimizer还允许您在单个历程或营销策划中组合使用定位和实验，以创建更复杂的策略。

事实上，您可以使用定位创建多个变体，并为每个变体使用试验进一步优化每个内容。 这可确保试验特定于每个定位规则，且不会跨越变体。

例如，您可以针对美国客户测试“促销活动50%折扣”与“礼品卡50美元”，针对欧洲客户运行其他测试，例如“超过50欧元的订单免运费”与“下次购买时折扣20%”。

要在历程或营销活动中同时使用定位和实验功能，请执行以下步骤。

1. 创建可在其中定义多个定位规则的历程或营销策划。 [了解如何操作](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. 为第一个定位规则创建试验。

1. 根据需要设计和配置内容试验。 [了解如何操作](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   定义试验后，该试验仅适用于第一个定位规则。

1. 返回&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，选择&#x200B;**[!UICONTROL 编辑内容]**。

1. 对于由第一个定位规则定义的组，您可以为试验的每个变体定义特定内容。

   如果您向历程或营销策划添加了多个集客操作，则相同的定位和试验组合适用于每个操作。 但是，您需要为每个操作的每个变体定义特定的内容。

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. 对其他定位规则执行类似操作，并为每个变体设计相应的内容。

1. 保存更改并[激活](review-activate-campaign.md)您的历程或营销活动。

历程/营销活动上线后，会随机将每个目标组中的用户分配给为其所属的组定义的不同内容变体。

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

