---
title: 更新扩展放置
description: Exd放置包含与约束和排名方法关联的集合，用于确定优惠。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 74e090e1-4dbe-484b-a482-ef43e082e7b1
TQID: https://experienceleague.adobe.com/6RpNeMQUn2qEfAzQ-Q7f7PgBRJCLqp7WnsoKx0xr12s
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 5%

---

# 更新扩展投放位置 {#update-exd-placement}

您可以通过向选件库API发出PUT请求来修改或更新投放位置。

有关JSON PUT的更多信息（包括可用的操作），请参阅JSON PUT官方文档。

**接受和内容类型标头**

下表显示了组成请求标头中Content-Type字段的有效值：

| 参数 | 描述 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API格式**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要更新的实体的ID。 | `placement1234` |

**请求**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| 参数 | 描述 |
| --------- | ----------- |
| `value` | 要用于更新参数的新值。 |
| `path` | 要更新的参数的路径。 |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**响应**

成功的响应会返回扩展位置的更新详细信息，包括ID。

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
