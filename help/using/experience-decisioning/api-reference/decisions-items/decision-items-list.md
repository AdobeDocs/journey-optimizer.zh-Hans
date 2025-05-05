---
title: 列出决策项目
description: 决策项目是营销优惠，您可以创建这些优惠并将其组织到收藏集和目录中。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 12%

---


# 列出决策项目 {#list-decision-items}

通过 Journey Optimizer，可创建营销优惠（称为决策项）并将其整理到集中目录和收藏集中。它们由旨在精确满足您需求的标准和自定义属性组成。 此外，它们包含配置文件约束，允许您定义决策项目可以显示给谁。

您可以通过对优惠库API执行单个GET请求来查看所有决策项的列表。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-items?{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 用于筛选结果的可选查询参数。 | `limit=2` |

## 使用查询参数 {#using-query-parameters}

在列出资源时，您可以使用查询参数来分页并筛选结果。

### 分页 {#paging}

分页最常见的查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `property` | 可选的属性过滤器： <ul><li>这些属性按AND操作进行分组。</li><li>参数可以重复，如：属性={PROPERTY_EXPR}[&amp;属性={PROPERTY_EXPR2}...]或属性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>属性表达式的格式为`[ !]field[op]value`，在`[==,!=,<=,>=,<,>,~]`中包含`op`，支持正则表达式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`，`-name` |
| `limit` | 限制返回的实体数。 | `limit=5` |

**请求**

```shell
curl -X GET '<https://platform.adobe.io/data/core/dps/offer-items?limit=2>' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**响应**

成功的响应将返回您有权访问的优惠项目列表。 `_<imsOrg>`节点包含自定义决策项属性。

```json
{
    "results": [
        {
            "created": "2024-06-10T16:00:34.014Z",
            "modified": "2024-07-09T22:59:21.507Z",
            "etag": 1,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem5678",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "draft"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-10T04:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "eligibilityRule": "rule1234",
                            "profileConstraintType": "eligibilityRule"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem5678",
                        "itemLabels": [],
                        "itemName": "Offer Item One",
                        "itemPriority": 1,
                        "itemTags": []
                    }
                }
            },
            "_<imsOrg>": {
                "some_field": "some value"
            }
        },
        {
            "created": "2024-06-04T17:51:52.849Z",
            "modified": "2024-06-28T18:29:27.951Z",
            "etag": 5,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem1234",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "frequencyCappingConstraints": [],
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "approved"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-01T07:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "profileConstraintType": "none"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem1234",
                        "itemLabels": [],
                        "itemName": "Offer Item Two",
                        "itemPriority": 2,
                        "itemTags": []
                    }
                }
            },
            "YOUR_CUSTOM_ATTRIBUTES": {
                "some_field": "some value",
                "some_boolean_field": true
            }
        }
    ],
    "count": 2,
    "total": 844,
    "_links": {
        "self": {
            "href": "/offer-items?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-items?orderby=-modified&limit=2&start=2024-06-28T03:44:15.630Z",
            "type": "application/json"
        }
    }
}
```
