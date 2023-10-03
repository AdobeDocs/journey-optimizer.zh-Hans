---
title: 列出决策规则
description: 决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: a6ba9632f6de91ed7911012ec4174cb7a01f5f12
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---

# 列出决策规则 {#list-decision-rules}

决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。 您可以通过对容器执行单个GET请求，查看容器中现有决策规则的列表。 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
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
| `property` | 可选的属性过滤器： <ul><li>这些属性按AND操作进行分组。</li><li>参数可以重复，如下所示：属性={PROPERTY_EXPR}[属性(&amp;P)={PROPERTY_EXPR2}...] 或属性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>属性表达式采用格式 `[!]field[op]value`，替换为 `op` 在 `[==,!=,<=,>=,<,>,~]`，支持正则表达式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 按特定属性对结果进行排序。 在名称前添加 — (orderby=-name)将按名称以降序对项目排序(Z-A)。 路径表达式采用点分隔路径的形式。 此参数可重复，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制返回的实体数。 | `limit=5` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回您有权访问的决策规则列表。

```json
{
     "results": [
        {
            "created": "2022-09-16T18:59:53.651+00:00",
            "modified": "2022-09-16T18:59:53.651+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule1234",
            "name": "Californians with one or more purchases greater than $1000",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
                 }
        },
        {
            "created": "2023-03-06T15:11:42.178+00:00",
            "modified": "2023-03-06T15:11:42.178+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule5678",
            "name": "People born after 1981",
            "description": "Persons with the birth date after 1981",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "person.birthDate occurs after date(1981, 1, 1)"
            }
        }
    ],
    "count": 2,
    "total": 25,
    "_links": {
        "self": {
            "href": "/offer-rules?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
