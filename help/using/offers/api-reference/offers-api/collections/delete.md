---
title: 删除收藏集
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 9%

---

# 删除收藏集 {#delete-collection}

有时可能有必要删除(DELETE)收藏集。 DELETE这是通过对 [!DNL Offer Library] API使用 `id` 要删除的收藏集的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要删除的实体的ID。 | `offerCollection1234` |

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

您可以通过尝试对收藏集进行查找(GET)请求来确认删除。 您应该会收到HTTP状态404 （未找到），因为该集合已被删除。
