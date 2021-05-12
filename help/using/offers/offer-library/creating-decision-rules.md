---
title: 创建决策规则
description: 了解如何在Adobe Experience Platform中创建决策规则。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# 创建决策规则 {#creating-decision-rules}

您可以根据Adobe Experience Platform中提供的数据创建优惠决策规则。 决策规则决定可向谁显示优惠。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

![](../../assets/do-not-localize/how-to-video.png) [在视频中发现此功能](#video)

可在&#x200B;**[!UICONTROL Components]**&#x200B;菜单中访问创建的决策规则的列表。

![](../../assets/decision_rules_list.png)

要创建决策规则，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL Rules]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL Create rule]**。

   ![](../../assets/offers_decision_rule_creation.png)

1. 命名规则并提供说明，然后根据需要配置规则。

   为此，Adobe Experience Platform的&#x200B;**区段生成器**&#x200B;可帮助您构建规则的条件。 有关如何使用它的详细信息，请参阅[专用文档](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/segment-builder.html)。

   在此示例中，该规则将目标具有“黄金”忠诚度级别的客户。

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >用于创建决策规则的区段生成器与与&#x200B;**[!UICONTROL Audience Destinations]**&#x200B;服务一起使用的区段生成器相比，显示了一些特性。 例如，**[!UICONTROL Segments]**&#x200B;选项卡不可用。 但是，区段生成器文档中描述的全局流程对于构建优惠决策规则仍然有效。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;进行确认。

1. 创建规则后，该规则将显示在规则列表中。 您可以选择它以显示其属性，并编辑或删除它。

   ![](../../assets/rule_created.png)

## 教程视频{#video}

>[!NOTE]
>
>此视频适用于在Adobe Experience Platform上构建的Offer Decisioning应用程序服务。 但是，它提供了在Journey Optimizer环境中使用优惠的通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
