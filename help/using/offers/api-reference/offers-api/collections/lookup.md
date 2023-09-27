---
title: 查找收藏集
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# 查找收藏集 {#look-up-collection}

集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。

您可以通过向以下网站发出GET请求来查找特定收藏集： [!DNL Offer Library] 包含收藏集的API `id` 在请求路径中。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要查找的实体的ID。 | `offerCollection1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回收藏集的详细信息，包括有关您的唯一收藏集的信息 `id`.

```json
{
        "created": "2022-09-16T18:59:23.063+00:00",
    "modified": "2022-09-16T18:59:23.063+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerCollection1234",
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}
```
