---
title: 删除决策项目
description: 决策项目是营销优惠，您可以创建这些优惠并将其组织到收藏集和目录中。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# 删除决策项目 {#delete-decision-item}

要删除决策项目，请使用要删除的决策项目的ID对优惠库API执行DELETE请求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| 参数 | 描述 | 示例 |
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

您可以通过尝试对决策项目发出查找(GET)请求来确认删除操作。 您应该会收到HTTP状态404（未找到），因为决策项目已被删除。
