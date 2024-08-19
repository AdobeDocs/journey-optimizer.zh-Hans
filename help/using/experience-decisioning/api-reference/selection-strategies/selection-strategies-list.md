---
title: 列表选择策略
description: 选择策略包括与约束关联的集合以及确定优惠的排名方法。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---


# 列表选择策略 {#list-selection-strategies}

选择策略包括与资格约束关联的集合和排名方法，以确定在[决策策略](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision)中选择时要显示的优惠。

您可以通过对选件库API执行单个GET请求来查看所有选择策略的列表。

**API格式**

```http
GET /{ENDPOINT_PATH}/selection-strategies?{QUERY_PARAMS}
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
| `property` | 可选的属性过滤器： <ul><li>这些属性按AND操作进行分组。</li><li>参数可以重复，如：属性={PROPERTY_EXPR}[&amp;属性={PROPERTY_EXPR2}...]或属性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>属性表达式的格式为`[!]field[op]value`，在`[==,!=,<=,>=,<,>,~]`中包含`op`，支持正则表达式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`，`-name` |
| `limit` | 限制返回的实体数。 | `limit=5` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回您有权访问的选择策略的列表。

```json
{
    "results": [
        {
            "created": "2024-02-08T03:01:50.924Z",
            "modified": "2024-02-16T23:03:03.019Z",
            "etag": 4,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy1234",
            "name": "Selection Strategy One",
            "description": "Selection Strategy",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "static"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "eligibilityRule",
                "eligibilityRule": "offerRule1234"
            },
            "optionSelection": {
                "filter": "itemCollection1234",
            }
        },
        {
            "created": "2024-01-11T11:12:06.775Z",
            "modified": "2024-01-15T14:36:02.994Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "selectionStrategy5678",
            "name": "Selection Strategy Two",
            "rank": {
                "priority": 1,
                "order": {
                    "orderEvaluationType": "scoringFunction",
                    "function": "rankingFormula5678"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            "optionSelection": {
                "filter": "itemCollection5678"
            }
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/selection-strategies?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/selection-strategies?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
