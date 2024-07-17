---
title: 删除个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 7%

---

# 删除个性化优惠 {#delete-personalized-offer}

有时可能有必要删除(DELETE)个性化优惠。 通过使用要删除的个性化优惠的ID向[!DNL Offer Library] API执行DELETE请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `personalizedOffer1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对个性化优惠进行查找(GET)请求来确认删除，并且由于个性化优惠已被删除，因此应该会收到HTTP状态404（未找到）。
