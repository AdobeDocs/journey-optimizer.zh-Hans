---
title: 列出收藏集限定符
description: 收藏集限定符允许您更好地对优惠进行组织和排序。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: bee5e067e70e065c9db14448c42224a9ec09c5bf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 6%

---

# 列出收藏集限定符 {#list-tags}

收藏集限定符（以前称为“标记”）允许您更好地对优惠进行组织和排序。 例如，您可以使用“黑色星期五”收藏集限定符来标记“黑色星期五”选件。 然后，您可以使用选件库中的搜索功能轻松找到具有此收藏集限定符的所有选件。

收藏集限定符也可用于将优惠分组为收藏集。 有关更多信息，请参阅以下教程： [创建收藏集](../../../offer-library/creating-collections.md).

您可以通过对以下对象执行单个GET请求，查看所有集合限定符的列表 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
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
| `property` | 可选的属性过滤器： <ul><li> 这些属性按AND操作进行分组。 <br><br>  — 参数可重复，如下所示：property=`<property-expr>`[属性(&amp;P)=`<property-expr2>`...] 或属性=`<property-expr1>`[和`<property-expr2>`...] <br><br>  — 属性表达式的格式为 `[!]field[op]` 值，包含运算输入 `[==,!=,'<=',>=,<,>,~]`，支持正则表达式  </li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制返回的实体数。 | `limit=5` |

**响应**

成功的响应将返回存在的集合限定符列表。

```json
{
                "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
