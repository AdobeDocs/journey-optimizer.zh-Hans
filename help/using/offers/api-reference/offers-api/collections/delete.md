---
title: 删除收藏集
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# 删除收藏集 {#delete-collection}

有时可能有必要删除(DELETE)收藏集。 只能删除您在租户容器中创建的收藏集。 DELETE这是通过对 [!DNL Offer Library] 使用要删除的收藏集的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 收藏集所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的集合的实例ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态202（无内容）和一个空白正文。

您可以通过尝试对收藏集进行查找(GET)请求来确认删除。 您将需要在请求中包含“接受”标头，但应该会收到HTTP状态404（未找到），因为集合已从容器中删除。
