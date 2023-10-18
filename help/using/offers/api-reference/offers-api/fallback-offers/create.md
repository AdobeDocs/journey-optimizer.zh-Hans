---
title: 创建后备优惠
description: 如果客户不符合其他优惠的条件，则会向客户发送后备优惠
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 13%

---

# 创建后备优惠 {#create-fallback-offer}

您可以通过向以下网站发出POST请求来创建后备优惠： [!DNL Offer Library] API。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Fallback Offer DPS",
    "description": "Fallback Offer description",
    "status": "approved",
    "selectionConstraint": {
        "startDate": "2022-06-10T00:30:00.000+00:00",
        "endDate": "2032-06-06T23:29:21.402+00:00",
        "profileConstraintType": "none"
    },
    "representations": [
        {
            "components": [
                {
                    "deliveryURL": "https://mysite.com",
                    "type": "imagelink",
                    "format": "image/png"
                }
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234"
        }
    ],
    "rank": {
        "priority": 1
    }
}'
```

**响应**

成功的响应会返回有关新创建的后备优惠的信息，包括其唯一的后备优惠 `id`. 您可以使用 `id` 在稍后的步骤中更新或删除您的后备优惠或创建决策（在稍后的教程中）。


```json
{
    "etag": 2,
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
