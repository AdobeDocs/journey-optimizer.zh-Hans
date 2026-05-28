---
title: 创建扩展投放位置
description: 扩展策略包括与约束和排名方法关联的集合以确定优惠。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 72492878-550d-4ca0-be12-7eb627f75ad0
TQID: https://experienceleague.adobe.com/jwUb00RaVqC0olkYXyjsY2BLVBod-lock4XuCqLuBkM
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
source-wordcount: 107
ht-degree: 6%

---

# 创建扩展投放位置 {#create-exd-placement}

您可以通过向选件库API发出POST请求来创建扩展版面。

**接受和内容类型标头**

下表显示了组成请求标头中Content-Type字段的有效值：

| 参数 | 说明 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/exd-placements
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |

**请求**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{
  "name": "Test Exd Placement1 Pants",
  "channel": "https://ns.adobe.com/xdm/channel-types/email",
  "tags":["3d75b849-b344-402b-9d9e-5d750bd46884"],
  "channelConfiguration":"530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
  "description": "compressing alarm",
  "status":"active"
}'
```

**响应**

成功的响应会返回新创建的扩展位置的详细信息，包括ID。 您可以在后续步骤中使用ID来更新或删除扩展版面。

```json
{
    "id": "dps:exd-placement:19cb038eca47bead",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "etag": 2,
    "createdDate": "2024-11-18T18:48:56.298Z",
    "lastModifiedDate": "2024-11-18T18:57:27.457Z",
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedByClientId": "CJMTestClientACP"
}
```
