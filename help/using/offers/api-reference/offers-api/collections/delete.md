---
title: 删除集合
description: 集合是基于营销人员定义的预定义条件的优惠子集，如优惠的类别。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# 删除集合

有时可能需要删除(DELETE)集合。 只能删除您在租户容器中创建的集合。 通过使用要删除的集合的$id对[!DNL Offer Library] API执行DELETE请求，即可完成此操作。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
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

成功的响应返回HTTP状态202（无内容）和空白正文。

您可以通过尝试对集合进行查找(GET)请求来确认删除。 您需要在请求中包含一个“接受”标头，但应接收HTTP状态404（“未找到”），因为集合已从容器中删除。
