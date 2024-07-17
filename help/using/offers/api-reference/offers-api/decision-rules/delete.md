---
title: 删除决策规则
description: 决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# 删除决策规则 {#delete-decision-rule}

有时可能有必要删除(DELETE)决策规则。 通过使用要删除的决策规则的`id`对[!DNL Offer Library] API执行DELETE请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要删除的实体的ID。 | `offerRule1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对决策规则进行查找(GET)请求来确认删除，由于决策规则已删除，因此应该会收到HTTP状态404 （未找到）。
