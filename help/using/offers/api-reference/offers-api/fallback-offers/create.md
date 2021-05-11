---
title: 创建后备优惠
description: 如果客户不符合其他优惠的资格，则会向客户发送回退优惠
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 11%

---

# 创建后备优惠

您可以通过向[!DNL Offer Library] API发出POST请求来创建回退优惠，同时提供您的容器ID。

## 接受和内容类型标题

下表显示了在请求标头中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;字段的有效值：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 回退优惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:status": "approved",
        "xdm:name": "Fallback for sales",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ]
}'
```

**响应**

成功的响应返回有关新创建的回退优惠的信息，包括其唯一实例ID和位置`@id`。 您可以在后续步骤中使用实例ID来更新或删除您的回退优惠。 您可以在稍后的教程中使用您唯一的回退优惠`@id`来创建决定。


```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2020-10-21T22:28:11.111732Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
