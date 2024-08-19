---
title: 列表项集合
description: 收藏集允许您根据自己的偏好对决策项目进行分类和分组。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 10%

---


# 列表项集合 {#list-decision-items}

收藏集（也称为项目收藏集）允许您根据首选项对决策项目进行分类和分组。 通过制定利用决策项属性的规则而创建这些类别。

您可以通过对选件库API执行单个GET请求来查看所有项目收藏集的列表。

**API格式**

```http
GET /{ENDPOINT_PATH}/item-collections?{QUERY_PARAMS}
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
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回您有权访问的项集合列表。

```json
{
    "results": [
        {
            "created": "2024-01-31T18:28:52.888Z",
            "modified": "2024-06-28T19:44:13.112Z",
            "etag": 7,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection1234",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
                }
            ],
            "tags": []
        },
        {
            "created": "2024-06-10T16:02:57.878Z",
            "modified": "2024-06-10T16:02:57.878Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection5678",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"greater than\",\"value\":{\"left\":\"_<imsOrg>.some_integer\",\"right\":100}}"
                }
            ],
            "tags": []
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/item-collections?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/item-collections?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
