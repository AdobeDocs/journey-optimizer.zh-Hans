---
title: 查找投放位置
description: 投放位置是用于展示优惠的容器。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: db337b5c-426a-4695-81e8-3a1b041791f2
source-git-commit: a6ba9632f6de91ed7911012ec4174cb7a01f5f12
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# 查找投放位置 {#look-up-placement}

您可以通过向以下网站发出GET请求来查找特定投放位置： [!DNL Offer Library] 包含投放位置的API `id`.

**API格式**

```http
GET /{ENDPOINT_PATH}/placements/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要查找的实体的ID。 | `offerPlacement1234` |

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回投放位置的详细信息，包括有关唯一投放位置的信息 `id`.

```json
{
     "created": "2023-05-15T11:22:50.031+00:00",
    "modified": "2023-05-15T11:22:50.031+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerPlacement1234",
    "name": "Placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/web",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": false,
    "returnMetaData": {
        "decisionName": true,
        "offerName": true,
        "offerAttributes": true,
        "offerPriority": true,
        "placementName": true,
        "channelType": true,
        "contentType": true
    }
}
```
