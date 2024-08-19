---
title: 查找决策项
description: 决策项目是营销优惠，您可以创建这些优惠并将其组织到收藏集和目录中。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---


# 查找决策项 {#lookup-decision-items}

要通过向优惠库API发出请求（请求路径中包含ID）来查找特定决策项目，请执行以下操作：GET

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-items/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要查找的实体的ID。 | `offerItem1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**响应**

成功的响应将返回决策项目的详细信息。

```json
{
    "created": "2024-06-10T16:00:34.014Z",
    "modified": "2024-07-09T22:59:21.507Z",
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerItem5678",
    "_experience": {
        "decisioning": {
            "offeritem": {
                "fCapConstraintsLastIndex": 0,
                "lifecycleStatus": "approved"
            },
            "decisionitem": {
                "itemCalendarConstraints": {
                    "endDate": "2030-12-31T08:00:00.000Z",
                    "startDate": "2024-06-10T04:00:00.000Z"
                },
                "itemCatalogID": "itemCatalong1234",
                "itemConstraints": {
                    "eligibilityRule": "rule1234",
                    "profileConstraintType": "eligibilityRule"
                },
                "itemDescription": "Offer item description",
                "itemID": "offerItem5678",
                "itemLabels": [],
                "itemName": "Offer Item One",
                "itemPriority": 1,
                "itemTags": []
            }
        }
    },
    "_<imsOrg>": {
        "some_field": "some value"
    }
}
```
