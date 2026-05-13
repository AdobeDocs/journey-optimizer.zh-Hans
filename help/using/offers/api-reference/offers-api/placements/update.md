---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 更新投放
description: 投放位置是用于展示优惠的容器。
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0Oy4Xd0F9lDuDC6A6IiTIp50LhJCfgCMgYcP4o4w8DQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# 更新投放 {#update-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]的新决策功能“决策”现在可通过基于代码的体验和电子邮件渠道使用！ [了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


您可以通过向[!DNL Offer Library] API发出PATCH请求来修改或更新投放位置。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](https://jsonpatch.com/)。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了请求标头中包含&#x200B;*Content-Type*&#x200B;字段的有效值：

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
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`、`remove`、`copy`和`test`。 |
| `path` | 要更新的参数的路径。 |
| `value` | 要用于更新参数的新值。 |

**响应**

成功响应将返回投放位置的更新详细信息，包括其唯一投放位置`id`。

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
