---
title: 删除排名公式
description: 排名公式允许您定义用于排名项目的评分函数。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# 删除排名公式 {#delete-selection-strategy}

有时可能有必要删除(DELETE)排名公式。 通过使用要删除的排名公式的ID向选件库API执行DELETE请求，可以完成此操作。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要删除的实体的ID。 | `rankingFormula1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对排名公式进行查找(GET)请求来确认删除操作。 您应会收到HTTP状态404（未找到），因为已删除排名公式。

