---
title: 创建收藏集限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 84f0efa5-28af-4569-994c-12d87828a277
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 12%

---

# 创建收藏集限定符 {#create-tag}

您可以创建集合限定符（以前称为“标记”），方法是在提供容器ID的同时，向[!DNL Offer Library] API发出POST请求。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了请求标头中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;字段的有效值：

| 标头名称 | 值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合限定符所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**响应**

成功的响应返回有关新创建的集合限定符的信息，包括其唯一实例ID和位置`@id`。 您可以在后面的步骤中使用实例ID来更新或删除您的集合限定词。 在以后的教程中，您可以使用唯一的收藏集限定符`@id`创建收藏集和个性化优惠。

```json
{
  "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2023-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
