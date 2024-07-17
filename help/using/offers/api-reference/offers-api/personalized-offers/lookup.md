---
title: 查找个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2e30b155-688b-432b-a703-d09de12ebdfd
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# 查找个性化优惠 {#look-up-personalized-offer}

个性化优惠是基于资格规则和约束的可自定义营销消息。

您可以通过向[!DNL Offer Library] API发出请求来查找特定的个性化优惠，GET路径中包含个性化优惠ID。

**API格式**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要查找的实体的ID。 | `personalizedOffer1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回个性化优惠的详细信息，包括有关您的独特个性化优惠`id`的信息。

```json
{
    "created": "2023-05-15T14:35:16.781+00:00",
    "modified": "2023-05-15T14:38:26.691+00:00",
    "etag": 2,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "personalizedOffer1234",
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}
```
