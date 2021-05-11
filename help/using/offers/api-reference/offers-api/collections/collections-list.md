---
title: 列出集合
description: 集合是基于营销人员定义的预定义条件的优惠子集，如优惠的类别。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# 列出集合

集合是基于营销人员定义的预定义条件的优惠子集，如优惠的类别。

您可以通过对[!DNL Offer Library] API执行单个GET请求，视图容器中所有集合的列表。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | 定义与集合关联的模式。 | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `{QUERY_PARAMS}` | 可选查询参数，用于筛选结果。 | `limit=1` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 使用查询参数

在列出资源时，您可以使用查询参数来页面和筛选结果。

### 分页

用于分页的最常见查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `q` | 要在所选字段中搜索的可选查询字符串。 查询字符串应为小写，并可以用多次引号括起来，以防止其被标记和转义特殊字符。 字符`+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /`具有特殊含义，在出现在查询字符串中时应使用反斜杠进行转义。 | `demo collection` |
| `qop` | 将AND或OR运算符应用于q查询字符串参数中的值。 | `AND` / `OR` |
| `field` | 可选列表字段以将搜索限制为。 可以重复此参数，如下所示：field=field1[,field=field2,...]和(路径表达式采用点分隔路径的形式，如_instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | 按特定属性对结果排序。 在标题(`orderby=-title`)之前添加`-`将按降序(Z-A)按标题对项目排序。 | `-repo:createdDate` |
| `limit` | 限制返回的集合数。 | `limit=5` |

**响应**

成功的响应会返回您有权访问的容器中存在的集合列表。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2020-10-21T21:14:19.282175Z",
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
                "repo:createdDate": "2020-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2020-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
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
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:36:29.272451Z",
                "repo:lastModifiedDate": "2020-09-17T14:36:29.272451Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:ids": [
                        "xcore:personalized-offer:1221fbedfa4d98b0"
                    ],
                    "xdm:name": "demo collection",
                    "xdm:filterType": "offers",
                    "@id": "xcore:offer-filter:1221fc71c74d98b4"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=2c54fc90-f8f3-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
