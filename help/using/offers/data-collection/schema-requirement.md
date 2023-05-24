---
product: experience platform
solution: Experience Platform
title: 配置事件捕获
description: 瞭解如何設定優惠方案以擷取事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 設定資料彙集 {#schema-requirements}

為了能夠取得對決策事件以外的事件型別的意見反應，您必須為中的每種事件型別設定正確的值 **體驗事件** 會傳送至Adobe Experience Platform的ID。

>[!CAUTION]
>
>對於每種事件型別，請確定資料集中使用的結構描述具有 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 [了解详情](create-dataset.md)

以下是實作JavaScript程式碼所需的結構描述需求。

>[!NOTE]
>
>決定事件不需要傳入，因為決定管理會自動產生這些事件，並將它們放入 **[!UICONTROL ODE DecisionEvents]** 資料集<!--to check--> 是自動產生的。

## 追蹤印象

請確定事件型別和來源如下：

**體驗事件型別：** `decisioning.propositionDisplay`
**來源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**範例裝載：**

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

## 追蹤點按

請確定事件型別和來源如下：

**體驗事件型別：** `decisioning.propositionInteract`
**來源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**範例裝載：**

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

## 追蹤自訂事件

對於自訂事件，資料集中使用的結構描述也必須具有 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組相關聯，但對必須用來標籤這些事件的體驗事件型別沒有特定要求。

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
