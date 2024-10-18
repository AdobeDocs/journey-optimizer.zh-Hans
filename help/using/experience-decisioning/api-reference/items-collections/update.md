---
title: 更新项目集合
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
source-git-commit: b057d198d3c5b12121ee50d7a97ff4b33b8209b4
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 5%

---

# 更新项目集合 {#update-item-collection}

您可以通过向选件库API发出PATCH请求来修改或更新项目收藏集。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](https://jsonpatch.com/)。

**API格式**

```http
PATCH /{ENDPOINT_PATH}/item-collections/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要更新的实体的ID。 | `itemCollections1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated item collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated item collection description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `value` | 要用于更新参数的新值。 |
| `path` | 要更新的参数的路径。 |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**响应**

成功的响应返回项目集合的更新详细信息，包括`id`。

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
