---
title: 更新选择策略
description: 选择策略包括与约束关联的集合以及确定优惠的排名方法。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# 更新选择策略 {#update-selection-strategy}

您可以通过向选件库API发出PATCH请求来修改或更新选择策略。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](http://jsonpatch.com/)。

**API格式**

```http
PATCH /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要更新的实体的ID。 | `selectionStrategy1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated selection strategy"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated selection strategy description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `value` | 要用于更新参数的新值。 |
| `path` | 要更新的参数的路径。 |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**响应**

成功响应将返回选择策略的更新详细信息，包括ID。

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
