---
title: 更新后备优惠
description: 如果客户不符合其他优惠的条件，则会向客户发送后备优惠
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f153c2ee-e789-4d8e-a03b-e914690ff354
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# 更新后备优惠 {#update-fallback-offer}

您可以通过向[!DNL Offer Library] API发出PATCH请求来修改或更新容器中的后备优惠。

有关JSON修补程序的更多信息（包括可用的操作），请参阅官方的[JSON修补程序文档](https://jsonpatch.com/)。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了请求标头中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;字段的有效值：

| 标头名称 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 后备优惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 后备优惠的实例ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**请求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`、`replace`和`remove`。 |
| `path` | 要更新的参数的路径。 |
| `value` | 要用于更新参数的新值。 |

**响应**

成功的响应将返回后备优惠的更新详细信息，包括其唯一实例`id`。

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
