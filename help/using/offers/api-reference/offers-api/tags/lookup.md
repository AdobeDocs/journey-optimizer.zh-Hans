---
title: 查找集合限定符
description: 使用收藏集限定符，您可以更好地组织和排序选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# 查找集合限定符 {#look-up-tag}

您可以通过向 [!DNL Offer Library] 包含集合限定符的API `@id` 或请求路径中集合限定符的名称。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合限定符所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | 定义与集合限定符关联的架构。 | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `id` | 用于匹配 `@id` 实体的属性。 字符串完全匹配。 参数 `id` 和 `name` 不能一起使用。 | `xcore:tag:124e147572cd7866` |
| `name` | 用于匹配实体的xdm:name属性的字符串。 字符串与大小写完全匹配，但可以使用通配符。 参数 `id` 和 `name` 不能一起使用 | `Holiday sales and promotions` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
```

**响应**

成功响应会返回收集限定符的详细信息，包括有关容器ID、实例ID和唯一收集限定符的信息 `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:35:28.233975Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-21T20:34:34.486296Z",
                "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Holiday sales and promotions",
                    "@id": "xcore:tag:124e147572cd7866"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#d48fd160-13dc-11eb-bc55-c11be7252432",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
