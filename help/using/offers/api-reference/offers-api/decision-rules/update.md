---
title: 更新决策规则
description: 决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 42c531fd-0dc9-492d-8827-2e1460454064
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 9%

---

# 更新决策规则 {#update-decision-rule}

您可以通过向[!DNL Offer Library] API发出PATCH请求来修改或更新决策规则。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](https://jsonpatch.com/)。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了请求标头中包含&#x200B;*Content-Type*&#x200B;字段的有效值：

| 标头名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要更新的实体的ID。 | `offerRule1234` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated decision rule"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated decision rule description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |
| `path` | 要更新的参数的路径。 |
| `value` | 要用于更新参数的新值。 |

**响应**

成功的响应返回决策规则的更新详细信息，包括其唯一的决策规则`id`。

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
