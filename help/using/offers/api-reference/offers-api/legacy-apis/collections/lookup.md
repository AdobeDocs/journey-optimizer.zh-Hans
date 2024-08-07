---
title: 查找收藏集
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 91317c46-d8b6-456e-8282-aef1169941af
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# 查找收藏集 {#look-up-collection}

集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。

您可以通过向[!DNL Offer Library] API发出GET请求来查找特定收藏集，请求路径中包含收藏集`@id`或收藏集名称。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 收藏集所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | 定义与收藏集关联的架构。 | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `id` | 用于匹配实体的`@id`属性的字符串。 字符串完全匹配。 参数`id`和`name`不能一起使用。 | `xcore:offer-filter:124bd44648f17ec1` |
| `name` | 用于匹配实体的xdm：name属性的字符串。 字符串与大小写完全匹配，但可以使用通配符。 参数`id`和`name`不能一起使用 | `Mobile demo` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回投放位置的详细信息，包括有关容器ID、实例ID和唯一集合`@id`的信息。

```json
{
    "containerId": "ab574eca-f7a9-38d0-b3d9-297376ca9ee2",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2023-10-21T21:29:27.329070Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
    "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
    ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2023-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:ids": [
                        "xcore:tag:124bd3de7f598dd8"
    ],
                    "xdm:name": "Mobile Demo",
                    "xdm:filterType": "anyTags",
                    "@id": "xcore:offer-filter:124bd44648f17ec1"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
