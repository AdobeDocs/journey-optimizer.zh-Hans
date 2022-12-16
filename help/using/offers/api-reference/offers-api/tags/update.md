---
title: 更新标记
description: 利用标记，可更好地组织和排序选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 918927e1-ad7a-4937-b652-2a0932e9efa1
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 8%

---

# 更新标记 {#update-tag}

您可以通过向 [!DNL Offer Library] API。

有关JSON修补程序（包括可用操作）的更多信息，请参阅 [JSON修补程序文档](http://jsonpatch.com/).

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示构成 *Content-Type* 和 *接受* 请求标题中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 标记所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的标记的实例ID。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**请求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
          "op": "replace",
          "path": "/_instance/xdm:name",
          "value": "Sales and promotions for the holidays"
        }
    ]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 操作调用，用于定义更新连接所需的操作。 操作包括： `add`, `replace`和 `remove`. |
| `path` | 要更新的参数的路径。 |
| `value` | 要使用更新参数的新值。 |

**响应**

成功响应会返回标记的更新详细信息，包括其唯一实例ID和标记 `@id`.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:36:31.782607Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
