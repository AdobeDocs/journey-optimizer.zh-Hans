---
title: 更新投放
description: 投放位置是用于展示优惠的容器。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 8%

---

# 更新投放位置 {#update-placement}

您可以通过向以下网站发出PATCH请求来修改或更新投放位置： [!DNL Offer Library] API。

有关JSON补丁程序的更多信息（包括可用的操作），请参阅官方网站上的 [JSON修补程序文档](https://jsonpatch.com/).

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/placements/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要更新的实体的ID。 | `offerPlacement1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated placement"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated placement description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`， `replace`， `remove`， `copy` 和 `test`. |
| `path` | 要更新的参数的路径。 |
| `value` | 要用于更新参数的新值。 |

**响应**

成功的响应将返回投放位置的更新详细信息，包括其唯一投放位置 `id`.

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
