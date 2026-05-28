---
title: 删除决策项目
description: 决策项目是营销优惠，您可以创建这些优惠并将其组织到收藏集和目录中。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/OkPIse7NFATcyTdTT0pzNhjPMenbrvigSG2lSRatb-M
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 4%

---

# 删除决策项目 {#delete-decision-item}

要删除决策项目，请使用要删除的决策项目的ID对优惠库API执行DELETE请求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要删除的实体的ID。 | `offerItem1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对决策项目进行查找(GET)请求来确认删除。 您应该会收到HTTP状态404（未找到），因为决策项目已被删除。
