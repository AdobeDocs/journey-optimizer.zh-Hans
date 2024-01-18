---
title: 删除收藏集限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 删除收藏集限定符 {#delete-tag}

有时可能需要移除(DELETE)收藏集限定符（以前称为“标记”）。 通过使用要删除的收藏集限定符的ID对选件库API执行DELETE请求，可以完成此操作。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `tag1234` |

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

您可以通过尝试对集合限定符进行查找(GET)请求来确认删除。 您应该会收到HTTP状态404 （未找到），因为集合限定符已被删除。