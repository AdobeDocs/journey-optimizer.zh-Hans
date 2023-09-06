---
title: 创建收藏集限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 9b9ca28b185a342d908eeb53d772f9d011105aba
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 12%

---

# 创建收藏集限定符 {#create-tag}

您可以通过对以下对象发出POST请求，来创建集合限定符（以前称为“标记”）： [!DNL Offer Library] API。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/tags
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**响应**

成功的响应将返回有关新创建的集合限定符的信息，包括其 `id`. 您可以在后面的步骤中使用它来更新或删除您的收集限定词。 您可以使用唯一的集合限定词 `id` ，以创建收藏集和个性化优惠。

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
