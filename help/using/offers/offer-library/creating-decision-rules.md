---
title: 创建决策规则
description: 了解如何在Adobe Experience Platform中创建决策规则。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 15%

---

# 创建决策规则 {#creating-decision-rules}

您可以根据Adobe Experience Platform中提供的数据创建选件决策规则。 决策规则确定可向谁显示选件。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

➡️ [在视频中发现此功能](#video)

可在&#x200B;**[!UICONTROL Components]**&#x200B;菜单中访问已创建决策规则的列表。

![](../../assets/decision_rules_list.png)

要创建决策规则，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL Rules]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL Create rule]**。

   ![](../../assets/offers_decision_rule_creation.png)

1. 命名规则并提供描述，然后根据需要配置规则。

   要实现此目的，可使用&#x200B;**区段生成器**&#x200B;来帮助您构建规则的条件。 [了解详情](../../segment/about-segments.md)

   在此示例中，规则将定位忠诚度级别为“Gold”的客户。

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >与&#x200B;**[!UICONTROL Audience Destinations]**&#x200B;服务中使用的区段生成器相比，用于创建决策规则的区段生成器显示了一些特性。 例如，**[!UICONTROL Segments]**&#x200B;选项卡不可用。 但是，区段生成器文档中描述的全局流程对于构建选件决策规则仍然有效。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;确认。

1. 创建规则后，该规则会显示在规则列表中。 您可以选择它以显示其属性，并编辑或删除它。

   ![](../../assets/rule_created.png)

## 教程视频 {#video}

>[!NOTE]
>
>此视频适用于基于Adobe Experience Platform构建的Offer decisioning应用程序服务。 但是，它为在Journey Optimizer上下文中使用选件提供了通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
