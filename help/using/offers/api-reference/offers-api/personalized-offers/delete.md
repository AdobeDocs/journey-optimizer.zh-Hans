---
title: 删除个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 6%

---

# 删除个性化优惠 {#delete-personalized-offer}

有时可能有必要删除(DELETE)个性化优惠。 只能删除您在租户容器中创建的个性化优惠。 DELETE这是通过对 [!DNL Offer Library] API使用要删除的个性化优惠的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 个性化优惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态202（无内容）和一个空白正文。

您可以通过尝试对个性化优惠进行查找(GET)请求来确认删除。 您将需要在请求中包含“接受”标头，但应该会收到HTTP状态404（未找到），因为已从容器中删除个性化优惠。
