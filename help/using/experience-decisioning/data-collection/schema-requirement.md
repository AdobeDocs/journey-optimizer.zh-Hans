---
product: experience platform
solution: Experience Platform
title: 配置事件捕获
description: 了解如何配置优惠方案以捕获事件
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 42b7b7fe7ab6380ca54e05ab0905f2517f489782
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# 配置数据收集 {#schema-requirements}

要获得有关决策事件以外的事件类型的反馈，您必须在发送到Adobe Experience Platform的&#x200B;**体验事件**&#x200B;中为每个事件类型设置正确的值。

>[!CAUTION]
>
>对于每种事件类型，请确保数据集中使用的架构具有与之关联的&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组。 [了解详情](create-dataset.md)

以下是您需要实施到JavaScript代码中的架构要求。

>[!NOTE]
>
>无需发送决策事件，因为决策管理会自动生成这些事件，并将其放入自动生成的&#x200B;**[!UICONTROL ODE DecisionEvents]**&#x200B;数据集<!--to check-->中。

## 跟踪展示 {#track-impressions}

确保事件类型和源如下所示：

**体验事件类型：** `decisioning.propositionDisplay`
**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次摄取
+++**示例有效负载：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## 跟踪点击次数 {#track-clicks}

确保事件类型和源如下所示：

**体验事件类型：** `decisioning.propositionInteract`
**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次摄取
+++**示例有效负载：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## 跟踪自定义事件 {#track-custom-events}

对于自定义事件，数据集中使用的架构还必须具有与其关联的&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组，但必须用于标记这些事件的体验事件类型没有特定要求。

>[!NOTE]
>
>若要在[capping](../items.md#capping)中考虑自定义事件，您需要将体验事件发送到以下两个Adobe Experience Platform数据收集端点之一，以将其连接到Edge端点：
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>如果您使用的是[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"}或[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=zh-Hans){target="_blank"}，则会自动建立连接。
