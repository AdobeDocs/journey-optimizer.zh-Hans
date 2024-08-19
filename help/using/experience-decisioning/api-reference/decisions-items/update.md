---
title: 更新决策项
description: 决策项目是营销优惠，您可以创建这些优惠并将其组织到收藏集和目录中。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# 更新决策项 {#update-decision-items}

您可以通过向PATCH库API发出优惠请求来修改或更新决策项目。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](http://jsonpatch.com/)。

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要更新的实体的ID。 | `offerItem1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `value` | 要用于更新参数的新值。 |
| `path` | 要更新的参数的路径。 |
| `op` | 要执行的操作的类型。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**响应**

成功的响应将返回更新项目的详细信息，包括ID。 您可以在后续步骤中使用ID来更新或删除决策项。

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
