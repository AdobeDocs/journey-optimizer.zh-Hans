---
title: 删除标记
description: 利用标记，可更好地组织和排序选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 删除标记 {#delete-tag}

有时可能需要删除(DELETE)标记。 只能删除您在租户容器中创建的标记。 这是通过向执行DELETE请求来完成的 [!DNL Offer Library] 使用您要删除的标记的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 标记所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的标记的实例ID。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应会返回HTTP状态202（无内容）和空白正文。

您可以通过尝试对标记进行查找(GET)请求来确认删除。 您需要在请求中包含接受标头，但应会收到HTTP状态404（未找到），因为标记已从容器中删除。
