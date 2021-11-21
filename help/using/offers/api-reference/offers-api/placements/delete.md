---
title: 删除版面
description: 版面是用于显示选件的容器。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 删除投放位置

有时可能需要删除(DELETE)版面。 只能删除您在租户容器中创建的版面。 这是通过向执行DELETE请求来完成的 [!DNL Offer Library] 使用您要删除的版面的实例ID的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 放置位置所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的版面的实例ID。 | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应会返回HTTP状态202（无内容）和空白正文。

您可以通过尝试对版面进行查找(GET)请求来确认删除。 您需要在请求中包含接受标头，但应会收到HTTP状态404（未找到），因为已从容器中删除了版面。
