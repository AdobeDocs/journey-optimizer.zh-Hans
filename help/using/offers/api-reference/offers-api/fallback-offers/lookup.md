---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 查找后备优惠
description: 如果客户不符合其他优惠的条件，则会向客户发送后备优惠
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 8f1fa116-30d2-4732-8973-bbce0dc66dec
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Z5tERXgh6YE9BWBwi-6Ok1tECp5SFJQUJj0MXMemt7Y
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 22%

---

# 查找后备优惠 {#look-up-fallback-offers}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


您可以通过向[!DNL Offer Library] API发出GET请求（在请求路径中包含备用选件ID）来查找特定的备用选件。

**API格式**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要查找的实体的ID。 | `fallbackOffer1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回后备优惠的详细信息，包括您的后备优惠和唯一的后备优惠ID。

```json
{
    "created": "2023-06-08T14:04:41.011+00:00",
    "modified": "2023-06-08T14:04:41.011+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "fallbackOffer1234",
    "name": "Fallback Offer Web",
    "description": "Fallback Offer Web Description",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "imagelink",
                    "format": "image/png",
                    "deliveryURL": "https://mysite.com"
                }
            ]
        }
    ]
}
```
