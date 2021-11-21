---
title: 创建决策规则
description: 了解如何在Adobe Experience Platform中创建决策规则。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 12%

---

# 创建决策规则 {#creating-decision-rules}

您可以根据Adobe Experience Platform中提供的数据创建选件决策规则。 决策规则确定可向谁显示选件。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

➡️ [在视频中发现此功能](#video)

创建的决策规则列表可在 **[!UICONTROL Components]** 菜单。

![](../../assets/decision_rules_list.png)

要创建决策规则，请执行以下步骤：

1. 转到 **[!UICONTROL Rules]** ，然后单击 **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. 命名规则并提供描述，然后根据需要配置规则。

   为此， **区段生成器** 可帮助您构建规则的条件。 [了解详情](../../segment/about-segments.md)

   在此示例中，规则将定位忠诚度级别为“Gold”的客户。

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >与与 **[!UICONTROL Audience Destinations]** 服务。 例如， **[!UICONTROL Segments]** 选项卡。 但是，区段生成器文档中描述的全局流程对于构建选件决策规则仍然有效。

1. 单击 **[!UICONTROL Save]** 确认。

1. 创建规则后，该规则会显示在规则列表中。 您可以选择它以显示其属性，并编辑或删除它。

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>中当前不支持基于事件的选件 [!DNL Journey Optimizer]. 如果您根据 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您将无法在选件中利用它。

## 教程视频 {#video}

>[!NOTE]
>
>此视频适用于基于Adobe Experience Platform构建的Offer decisioning应用程序服务。 但是，它为在Journey Optimizer上下文中使用选件提供了通用指南。

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
