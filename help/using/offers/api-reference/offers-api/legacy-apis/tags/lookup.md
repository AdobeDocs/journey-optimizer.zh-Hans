---
title: 查找集合限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---

# 查找集合限定符 {#look-up-tag}

GET您可以通过向[!DNL Offer Library] API发出请求（请求路径中包含集合限定符`id`）来查找特定的集合限定符（以前称为“标记”）。

**API格式**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要查找的实体的ID。 | `tag1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回集合限定符的详细信息，包括有关唯一集合限定符`id`的信息。

```json
{
       "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
