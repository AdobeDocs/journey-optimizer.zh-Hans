---
title: 创建投放位置
description: 投放位置是用于展示优惠的容器。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7b735873-86f5-466f-b079-5e84d9f03a08
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---

# 创建投放位置 {#create-placement}

您可以通过对以下网站发出POST请求来创建投放位置： [!DNL Offer Library] API。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/placements
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/placements' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "New placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": true,
    "returnMetaData": {
        "decisionName": false,
        "offerName": false,
        "offerAttributes": false,
        "offerPriority": false,
        "placementName": false,
        "channelType": false,
        "contentType": false
    }
}'
```

**响应**

成功的响应会返回新创建的投放位置和投放位置的详细信息 `id`. 您可以稍后使用它来更新或删除投放位置。 您可以使用独特的版面 `id` 在后面的教程中，这些教程用于创建决策、决策规则和后备优惠。

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
