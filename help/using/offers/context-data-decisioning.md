---
product: experience platform
solution: Experience Platform
title: 上下文数据和决策请求
description: 了解如何在Decisioning请求中传递上下文数据。
badge: label="旧版" type="Informative"
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 上下文数据和决策请求 {#context-data-decisioning}

本节指导您在Decisioning请求中传递上下文数据并在权限规则中使用它们。

>[!BEGINSHADEBOX]

若要更进一步，您还可以将上下文用于&#x200B;**排名公式**&#x200B;以提升优惠。 [此部分](../offers/ranking/create-ranking-formulas.md#context-data)中提供了利用上下文数据的排名公式的详细示例。

>[!ENDSHADEBOX]

## 在Decisioning请求中传递上下文数据

使用键定义Decisioning请求中的上下文数据： `xdm:ContextData`。

上下文数据属性不受XDM架构驱动。 您可以在JSON中作为决策请求有效负载的一部分传递任何上下文数据。

以下是包含上下文数据的决策请求示例（请参阅`xdm:ContextData`）：

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## 在资格规则中使用上下文数据

以下示例说明了如何在资格规则中使用在Decisioning请求中传递的上下文数据。

* 如果上下文数据功能包含特定值，则符合条件：

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* 如果渠道非空且等于移动设备，则符合条件：

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
