---
title: 列出扩展投放位置
description: 扩展投放包含与约束和排名方法关联的收藏集，用于确定优惠。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---

# 列出扩展投放位置 {#list-exd-placements}

您可以通过对选件库API执行单个GET请求来查看所有扩展投放的列表。

**API格式**

```http
GET /{ENDPOINT_PATH}/exd-placements?{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |

## 使用查询参数 {#using-query-parameters}

在列出资源时，您可以使用查询参数来分页并筛选结果。 您可以按状态、渠道和channelConfiguration进行筛选。

### 分页 {#paging}

分页最常见的查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `property` | 可选的属性过滤器： <ul><li>这些属性按AND操作进行分组。</li><li>参数可以重复，如：属性={PROPERTY_EXPR}[&amp;属性={PROPERTY_EXPR2}...]或属性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>属性表达式的格式为`[!]field[op]value`，在`[==,!=,<=,>=,<,>,~]`中包含`op`，支持正则表达式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`，`-name` |
| `limit` | 限制返回的实体数。 | `limit=5` |

**请求**

```shell
curl --location --request GET 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{"query":"","variables":{}}'
```

**响应**

成功的响应将返回您有权访问的扩展投放位置列表。

```json
{
    "results": [
        {
            "created": "2024-11-14T23:30:29.820Z",
            "modified": "2024-11-14T23:30:29.820Z",
            "etag": 1,
            "schemas": [
                "exd-placement"
            ],
            "createdBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "lastModifiedBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "id": "dps:exd-placement:19c61da45ed96159",
            "name": "testing-alfa",
            "description": "atest",
            "tags": [
                "35801d6b-6371-449d-9083-d895fc120569"
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "channelConfiguration": "fb8e9621-a5e8-485f-9f3f-d040c601ebc4",
            "status": "active"
        },
        {
            "created": "2024-10-22T00:18:17.997Z",
            "modified": "2024-10-22T05:04:15.315Z",
            "etag": 2,
            "schemas": [
                ""
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps::19a7426d533db126",
            "name": "Test Exd Placement capacitor",
            "description": "Wooden system",
            "status": "archived"
        }
    ],
    "count": 2,
    "total": 2,
    "_links": {
        "self": {
            "href": "/exd-placements?orderby=-modified&limit=50",
            "type": "application/json"
        }
    }
}
```
