---
title: 删除决策
description: 决策包含通知优惠选择的逻辑。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# 删除决策 {#delete-decision}

有时可能有必要删除(DELETE)决策。 DELETE这是通过对 [!DNL Offer Library] API使用 `id` 要删除的决策。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `offerDecision1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对决策进行查找(GET)请求来确认删除。 您应会收到HTTP状态404 （未找到），因为决策已被删除。