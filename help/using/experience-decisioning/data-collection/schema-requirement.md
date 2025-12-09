---
solution: Journey Optimizer
product: Journey Optimizer
title: 配置事件捕获
description: 了解如何配置优惠方案以捕获事件
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 093e5ba2a74b498bb31d0398e1df460fd93b285f
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# 配置数据收集 {#schema-requirements}

要获得有关决策事件以外的事件类型的反馈，您必须在发送到Adobe Experience Platform的&#x200B;**体验事件**&#x200B;中为每个事件类型设置正确的值。

>[!CAUTION]
>
>对于每种事件类型，请确保数据集中使用的架构具有与之关联的&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组。<!--[Learn more](create-dataset.md)-->

以下是您需要实施到JavaScript代码中的架构要求。

## 跟踪展示 {#track-impressions}

确保正确配置以下字段：

**体验事件类型：** `decisioning.propositionDisplay`

**propositionEventType：** `_experience.decisioning.propositionEventType.display`

**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取

+++**示例有效负载：**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## 跟踪点击次数 {#track-clicks}

确保正确配置以下字段：

**体验事件类型：** `decisioning.propositionInteract`

**propositionEventType：** `_experience.decisioning.propositionEventType.interact`

**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量摄取

建议中的每个选件都包含一个跟踪令牌，该令牌是Adobe生成的唯一标识符。 此令牌必须在相应的点击或展示事件中完全按照收到的样式传递（不会发生更改）。 匹配跟踪令牌可确保Adobe能够准确地将用户操作与正确的优惠决策相关联，从而实现下游报表和基于人工智能的优化。

>[!CAUTION]
>
>如果您在跟踪点击时未在`propositionAction.tokens`字段中传递跟踪令牌，则点击事件将无法正确归因于相应的选件。 这将导致跟踪数据不完整，并将对报表和基于人工智能的排名优化产生负面影响。 始终确保在点击跟踪实施中包括建议中的跟踪令牌。

+++**示例有效负载：**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## 跟踪自定义事件 {#track-custom-events}

对于自定义事件，数据集中使用的架构还必须具有与其关联的&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组，但必须用于标记这些事件的体验事件类型没有特定要求。

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, the connection is made automatically.-->
