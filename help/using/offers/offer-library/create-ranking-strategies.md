---
product: experience platform
solution: Experience Platform
title: 创建排名策略
description: 了解如何创建AI模型以对优惠进行排名
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 1bca78723ec8ff93f48b9afa360868c2b9bac670
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 2%

---

# 人工智能排名 {#ai-rankings}

## AI排名入门 {#get-started-with-ai-rankings}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use a trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>目前，只能对选定用户提前访问AI排名。

此功能允许您创建不同的 **排名策略** 基于您的业务目标。 在决策（以前称为选件活动）中使用这些不同的基于目标的策略，经过培训的模型系统将帮助您了解不同的排名策略对您的目标有何影响。

例如，您可以为电子邮件渠道选择一个排名策略，为推送渠道选择另一个排名策略。 对于每个渠道，经过培训的模型系统将利用多个数据点来确定在给定投放中应首先显示哪个选件，而不是考虑选件的优先级分数或 [排名公式](create-ranking-formulas.md).

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

创建排名策略后，将其分配给决策中的版面。 在 [在决策中配置选件选择](../offer-activities/configure-offer-selection.md).

### 自动优化模型 {#auto-optimization}

当前位于 [!DNL Journey Optimizer] AI排名唯一支持的模型类型是 **自动优化**.

自动优化模型旨在根据您设置的关键绩效指标(KPI)，提供可最大化回报的选件。 <!--These KPIs could be in the form of conversion rates, revenue, etc.-->此时，自动优化将重点放在以选件转化为目标来优化选件点击量。

>[!NOTE]
>
>自动优化模型不使用任何上下文或用户配置文件数据。 它会根据选件的全局性能来优化结果。

通过自动优化，挑战在于在探索性学习与对该学习的利用之间取得平衡。 这个原则称为 **&quot;多臂老虎机&quot;方法**.

为了应对此挑战，自动优化模型使用 **汤普森采样** 方法，其允许确定追求哪种选择以最大化预期回报。 换句话说，汤普森采样是一种用于解决多臂老虎机问题中探索开发难题的强化学习技术。

汤普森采样方法还能够处理诸如“冷启动”问题等挑战，即当营销活动中引入新选件时，它没有任何可从中进行培训的历史记录。

## 创建排名策略 {#create-ranking-strategy}

要创建排名策略，请执行以下步骤：

1. 访问 **[!UICONTROL Components]** 菜单，然后选择 **[!UICONTROL AI rankings]** 选项卡。

   ![](../../assets/ai-ranking-list.png)

   列出了迄今为止创建的所有排名策略。

1. 单击 **[!UICONTROL Create strategy]** 按钮。

1. 填写以下字段：

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**:必须提供的唯一名称。

   * **[!UICONTROL Model type]**:目前唯一支持的模型类型是 **[!UICONTROL Auto-optimization]**.<!--More will be supported in the future so the drop-down list will be enabled.-->

   * **[!UICONTROL Optimization metric]**：

      此选项允许营销人员选择如何构建和培训机器学习模型：根据显示的选件、在电子邮件中单击的选件和/或在Web上单击的选件。

      >[!NOTE]
      >
      >您可以根据需要选择所有量度类型。

      优化量度有两种类型：
      * **[!UICONTROL Impression]**:当前展示事件与显示的所有选件相对应。
      * **[!UICONTROL Conversion]**:转化事件与通过电子邮件或Web进行点击的所有选件相对应。

      所有选定的展示事件和/或转化事件都将使用已提供的Web SDK或Mobile SDK自动捕获。 在 [Adobe Experience Platform Web SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans).

   * **[!UICONTROL Dataset ID]**:对于转化，您需要提供一个数据集，通过从下拉列表中选择该数据集来收集事件。 了解如何在 [此部分](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >仅从与 **[!UICONTROL Experience Event - Proposition Interactions]** 字段组（以前称为mixin）会显示在下拉列表中。

1. 保存并激活排名策略。

   ![](../../assets/ai-ranking-save-activate.png)

现在，它可用于对符合条件的选件进行版面排名的决策。 在 [此部分](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## 创建数据集以收集事件 {#create-dataset}

您需要创建一个数据集，以收集转化事件。 首先，创建将在数据集中使用的架构：

1. 从 **[!UICONTROL Data Management]** 菜单，选择 **[!UICONTROL Schema]**，转到 **[!UICONTROL Browse]** 选项卡，单击 **[!UICONTROL Create schema]**.

   ![](../../assets/ai-ranking-create-schema.png)

1. 选择 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    在 [XDM系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans).


1. 在 **[!UICONTROL Search]** 字段中，键入“建议交互”并选择 **[!UICONTROL Experience Event - Proposition Interactions]** 字段组。

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    将在数据集中使用的架构必须具有 **[!UICONTROL Experience Event - Proposition Interactions]** 与其关联的字段组。 否则，您将无法在排名策略中使用它。

1. 单击 **[!UICONTROL Add field groups]**。

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >字段组以前称为mixin。

1. 键入名称并保存架构。<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    了解有关在 [架构组合的基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

现在，您可以使用此架构创建数据集。 为此，请执行以下步骤：

1. 从 **[!UICONTROL Data Management]** 菜单，选择 **[!UICONTROL Datasets]**，转到 **[!UICONTROL Browse]** 选项卡，单击 **[!UICONTROL Create dataset]**.

   ![](../../assets/ai-ranking-create-dataset.png)

1. 选择 **[!UICONTROL Create dataset from schema]**。

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. 从列表中选择之前创建的架构。

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. 单击 **[!UICONTROL Next]**。

1. 为 **[!UICONTROL Name]** 字段，单击 **[!UICONTROL Finish]**.

   ![](../../assets/ai-ranking-dataset-name.png)

现在，可以选择数据集以在 [创建排名策略](#create-ranking-strategy).

## 提供架构要求 {#schema-requirements}

此时，您必须具有：

* 制定了排名策略，
* 定义要捕获的事件类型 — 显示的选件（展示次数）和/或点击的选件（转化），
* 以及要在哪个数据集中收集事件数据。

现在，每次显示和/或单击选件时，您都希望 **[!UICONTROL Experience Event - Proposition Interactions]** 字段组 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;}或Mobile SDK。

要发送事件类型（显示的选件或点击的选件），您必须为发送到Adobe Experience Platform的体验事件中的每个事件类型设置正确的值。 以下是在JavaScript代码中实施所需的架构要求：

### 显示选件的方案

**事件类型：** `decisioning.propositionDisplay`
**来源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取
+++**有效负载示例：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### “已单击选件”方案

**事件类型：** `decisioning.propositionInteract`
**来源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取
+++**有效负载示例：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->

