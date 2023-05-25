---
product: experience platform
solution: Experience Platform
title: 配置事件捕获
description: 了解如何配置优惠方案以捕获事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 34d30a4c45f007da6197999dbf1d0b283fba8248
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 3%

---

# 配置数据收集 {#schema-requirements}

为了能够获取有关决策事件以外的事件类型的反馈，您必须为中的每种事件类型设置正确的值 **体验事件** 发送至Adobe Experience Platform的内容。

>[!CAUTION]
>
>对于每种事件类型，请确保数据集中使用的架构具有 **[!UICONTROL 体验事件 — 建议交互]** 与其关联的字段组。 [了解详情](create-dataset.md)

以下是您需要实施到JavaScript代码中的架构要求。

>[!NOTE]
>
>无需发送决策事件，因为决策管理会自动生成这些事件并将其放入 **[!UICONTROL ODE DecisionEvents]** 数据集<!--to check--> 是自动生成的。

## 跟踪展示

确保事件类型和源如下所示：

**体验事件类型：** `decisioning.propositionDisplay`
**来源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取
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
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## 跟踪点击次数

确保事件类型和源如下所示：

**体验事件类型：** `decisioning.propositionInteract`
**来源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取
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

## 跟踪自定义事件

对于自定义事件，数据集中使用的架构还必须具有 **[!UICONTROL 体验事件 — 建议交互]** 字段组相关联，但对必须用于标记这些事件的体验事件类型没有特定要求。

>[!NOTE]
>
>要将您的自定义事件计入 [频率封顶](../offer-library/add-constraints.md#capping)，您需要将体验事件发送到以下两个Edge数据收集端点之一，以将其连接到Adobe Experience Platform端点：
>
>* POST/ee/v2/interact
>* POST/ee/v2/collect
>
>如果您使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}，则会自动建立连接。

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
