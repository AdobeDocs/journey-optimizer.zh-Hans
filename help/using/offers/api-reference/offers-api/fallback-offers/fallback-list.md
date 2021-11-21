---
title: 列出后备优惠
description: 如果客户不符合其他选件的资格，则会向客户发送备用选件
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: dd95c040-d905-4f5a-8cc5-58e39082e57e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 4%

---

# 列出后备优惠

如果客户不符合其他选件的资格，则会向客户发送一个备用选件。 创建备用选件的步骤包括创建一个或多个表示形式，例如创建选件时。

您可以通过向 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FALLBACK_OFFER}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 备用选件所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FALLBACK_OFFER}` | 定义与后备优惠关联的架构。 | `https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1` |
| `{QUERY_PARAMS}` | 用于按筛选结果的可选查询参数。 | `limit=1` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 使用查询参数

列出资源时，您可以使用查询参数来页面和筛选结果。

### 分页

用于分页的最常见查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `q` | 要在选定字段中搜索的可选查询字符串。 查询字符串应为小写，并可以用双引号括起来，以防止其被标记化并转义特殊字符。 字符 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 具有特殊含义，在查询字符串中显示时，应使用反斜杠进行转义。 | `default` |
| `qop` | 将AND或OR运算符应用于q查询字符串参数中的值。 | `AND` / `OR` |
| `field` | 可将搜索限制为的字段列表（可选）。 此参数可以重复，如下所示：field=field1[,field=field2,...] 和（路径表达式采用点分隔路径的形式，如_instance.xdm:name） | `_instance.xdm:name` |
| `orderBy` | 按特定属性对结果排序。 添加 `-` 前标题(`orderby=-title`)将按标题以降序(Z-A)对项目进行排序。 | `-repo:createdDate` |
| `limit` | 限制返回的备用选件数量。 | `limit=5` |

**响应**

成功响应会返回一个回退选件列表，这些选件在您有权访问的容器中存在。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1",
    "requestTime": "2020-10-22T07:12:30.923768Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-17T15:18:20.657299Z",
                "repo:lastModifiedDate": "2020-10-02T02:34:48.034583Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "F1: Web fallback ",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "xdm:content": "aaa",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json",
                                    "repo:name": "aa"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201b2150d98c2"
                        },
                        {
                            "xdm:components": [
                                {
                                    "xdm:content": "bb",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                                    "dc:format": "text/html",
                                    "repo:name": "bb"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201c34354a2b4"
                        },
                        {
                            "xdm:components": [
                                {
                                    "xdm:deliveryURL": "https://mysite.com",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "dc:format": "image/png",
                                    "repo:name": "ll"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122207eddb05205a"
                        }
                    ],
                    "xdm:status": "approved",
                    "xdm:tags": [],
                    "@id": "xcore:fallback-offer:122206064e0d98df"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5#053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 5,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=053bc610-f8f9-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
