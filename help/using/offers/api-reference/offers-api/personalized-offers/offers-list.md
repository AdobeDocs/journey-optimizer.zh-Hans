---
title: 列出个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# 列出个性化优惠 {#list-personalized-offers}

个性化优惠是基于资格规则和约束的可自定义营销消息。

您可以通过对以下网站执行单个GET请求，查看所有个性化优惠的列表： [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=personalized&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 用于筛选结果的可选查询参数。 | `limit=2` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 使用查询参数 {#using-query-parameters}

在列出资源时，您可以使用查询参数来分页并筛选结果。

### 分页 {#paging}

分页最常见的查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `property` | 可选的属性过滤器： <ul><li>这些属性按AND操作进行分组。</li><li>参数可以重复，如下所示：属性={PROPERTY_EXPR}[属性(&amp;P)={PROPERTY_EXPR2}...] 或属性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>属性表达式采用格式 `[!]field[op]value`，替换为 `op` 在 `[==,!=,<=,>=,<,>,~]`，支持正则表达式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制返回的投放位置数。 | `limit=5` |

**响应**

成功的响应将返回一个个性化优惠列表，这些优惠与您有权访问的那些优惠一起存在。

```json
{
    "results": [
        {
            "created": "2023-05-15T14:35:16.781+00:00",
            "modified": "2023-05-15T14:38:26.691+00:00",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "personalizedOffer1234",
            "name": "Test personalized offer with frequency constraint",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "html",
                            "format": "text/html",
                            "language": [
                                "en-us"
                            ],
                            "content": "Hello You qualify for our Discount of 60%"
                        }
                    ]
                }
            ],
            "selectionConstraint": {
                "startDate": "2022-07-27T05:00:00.000+00:00",
                "endDate": "2023-07-29T05:00:00.000+00:00",
                "profileConstraintType": "none"
            },
            "rank": {
                "priority": 0
            },
            "cappingConstraint": {},
            "frequencyCappingConstraints": [
                {
                    "enabled": false,
                    "limit": 1,
                    "startDate": "2023-05-15T14:25:49.622+00:00",
                    "endDate": "2023-05-25T14:25:49.622+00:00",
                    "scope": "global",
                    "entity": "offer",
                    "repeat": {
                        "enabled": false,
                        "unit": "month",
                        "unitCount": 1
                    }
                }
            ]
        }
    ],
    "count": 1,
    "total": 1,
    "_links": {
        "self": {
            "href": "/offers?offer-type=personalized&href={SELF_HREF}",
            "type": "application/json"
        }
    }
}
```
