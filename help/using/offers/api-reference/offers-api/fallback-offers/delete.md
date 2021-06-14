---
title: 删除后备优惠
description: 如果客户不符合其他选件的资格，则会向客户发送备用选件
feature: 优惠
topic: 集成
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# 删除后备优惠

有时可能需要删除(DELETE)备用选件。 只能删除您在租户容器中创建的备用选件。 这是通过使用您要删除的备用选件的$id对[!DNL Offer Library] API执行DELETE请求来完成的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 备用选件所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 备用选件的实例ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应会返回HTTP状态202（无内容）和空白正文。

您可以通过尝试对备用选件进行查找(GET)请求来确认删除。 您需要在请求中包含接受标头，但应会收到HTTP状态404（未找到），因为回退选件已从容器中删除。
