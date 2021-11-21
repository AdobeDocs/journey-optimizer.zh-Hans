---
title: 更新集合
description: 收藏集是基于营销人员定义的预定义条件（如选件的类别）的选件子集。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7d766f0a-4fcb-434a-bbfd-e18ade71ae56
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 7%

---

# 更新收藏集

您可以通过向 [!DNL Offer Library] API

有关JSON修补程序（包括可用操作）的更多信息，请参阅 [JSON修补程序文档](http://jsonpatch.com/).

## 接受和内容类型标头

下表显示构成 *Content-Type* 和 *接受* 请求标题中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 收藏集所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的集合的实例ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**请求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "add",
            "path": "/_instance/xdm:filterType",
            "value": "anyTags"
        },
        {
            "op": "add",
            "path": "/_instance/xdm:ids",
            "value": ["xcore:tag:124e147572cd7866"]
        }
    ]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 操作调用，用于定义更新连接所需的操作。 操作包括： `add`, `replace`和 `remove`. |
| `path` | 要更新的参数的路径。 |
| `value` | 要使用更新参数的新值。 |

**响应**

成功响应会返回集合的更新详细信息，包括其唯一实例ID和集合 `@id`.

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
