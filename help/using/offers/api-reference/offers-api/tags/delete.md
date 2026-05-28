---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 删除收藏集限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-GtK6nikASk8kLb0uPAsEpaSGKYdlu3m0u-jG2qxHT0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 19%

---

# 删除收藏集限定符 {#delete-tag}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


有时可能需要移除(DELETE)收藏集限定符（以前称为“标记”）。 通过使用要删除的收藏集限定符的ID对选件库API执行DELETE请求，可以完成此操作。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `tag1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对集合限定符进行查找(GET)请求来确认删除。 您应该会收到HTTP状态404 （未找到），因为集合限定符已被删除。
