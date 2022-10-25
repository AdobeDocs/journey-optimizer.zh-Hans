---
title: 创建决策规则
description: 了解如何创建决策规则以定义可向谁显示选件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 55d9befff9b9bf1bc81c6553cd76f015fdd3116e
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 10%

---

# 创建决策规则 {#create-decision-rules}

您可以根据Adobe Experience Platform中提供的数据创建选件决策规则。 决策规则确定可向谁显示选件。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

➡️ [在视频中发现此功能](#video)

创建的决策规则列表可在 **[!UICONTROL 组件]** 菜单。

![](../assets/decision_rules_list.png)

要创建决策规则，请执行以下步骤：

1. 转到 **[!UICONTROL 规则]** ，然后单击 **[!UICONTROL 创建规则]**.

   ![](../assets/offers_decision_rule_creation.png)

1. 命名规则并提供描述，然后根据需要配置规则。

   为此， **区段生成器** 可帮助您构建规则的条件。 [了解详情](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >与与 **[!UICONTROL 受众目标]** 服务。 例如， **[!UICONTROL 区段]** 选项卡。 但是， [区段生成器](../../segment/about-segments.md) 文档仍对构建选件决策规则有效。 在 [Adobe Experience Platform Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. 在工作区中添加和配置新字段时， **[!UICONTROL 区段属性]** 窗格显示属于该区段的估计用户档案的信息。 单击 **[!UICONTROL 刷新估计]** 更新数据。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >如果规则参数包含不在配置文件中的数据（如上下文数据），则配置文件估计不可用。 例如，要求当前天气为≥80度的资格规则。

1. 单击 **[!UICONTROL 保存]** 确认。

1. 创建规则后，该规则会显示在 **[!UICONTROL 规则]** 列表。 您可以选择它以显示其属性，然后编辑或删除它。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>中当前不支持基于事件的选件 [!DNL Journey Optimizer]. 如果您根据 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您将无法在选件中利用它。

## 教程视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
