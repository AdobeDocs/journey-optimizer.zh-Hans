---
title: 更新个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 8%

---

# 更新个性化优惠 {#update-personalized-offer}

您可以通过向以下网站发出PATCH请求来修改或更新个性化优惠： [!DNL Offer Library] API

有关JSON补丁程序的更多信息（包括可用的操作），请参阅官方网站上的 [JSON修补程序文档](https://jsonpatch.com/).

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要更新的实体的ID。 | `personalizedOffer1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`， `replace`， `remove`， `copy` 和 `test`. |
| `path` | 要更新的参数的路径。 |
| `value` | 要用于更新参数的新值。 |

**响应**

成功的响应会返回投放位置的更新详细信息，包括投放位置ID。

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
