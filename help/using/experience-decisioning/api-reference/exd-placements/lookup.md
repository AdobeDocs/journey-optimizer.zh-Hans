---
title: 查找扩展投放位置
description: Exd放置包含与约束和排名方法关联的集合，用于确定优惠。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: cc8ae245-a96a-401e-9157-e7d4b8982081
TQID: https://experienceleague.adobe.com/0vmTC00aXOb5CDyz77rupZZSnywE1n7eOx6czrtJZIU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 6%

---

# 查找扩展投放位置 {#list-exd-placement}

您可以通过向选件库API发出GET请求（请求路径中包含该ID）来查找特定扩展。

**API格式**

```http
GET /{ENDPOINT_PATH}/exd-placements/{ID}
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要查找的实体的ID。 | `placement1234` |

**请求**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19c5fa7448c6fcab' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}'
```

**响应**

成功的响应将返回扩展位置的详细信息。

```json
{
    "created": "2024-11-14T20:56:45.540Z",
    "modified": "2024-11-14T20:56:45.540Z",
    "etag": 1,
    "schemas": [
        "exd-placement"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:exd-placement:19c5fa7448c6fcab",
    "name": "Test Exd Placement1 Car",
    "description": "brand panel",
    "tags": [
        "3d75b849-b344-402b-9d9e-5d750bd46884"
    ],
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "channelConfiguration": "530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
    "status": "active"
}            
```
