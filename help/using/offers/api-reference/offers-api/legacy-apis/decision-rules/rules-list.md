---
title: 列出决策规则
description: 决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 600aea10-3675-47b7-8f4b-f378308afd69
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 5%

---

# 列出决策规则 {#list-decision-rules}

决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。 您可以通过对容器执行单个GET请求，查看容器中现有决策规则的列表。 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策规则所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | 定义与决策规则关联的架构。 | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `{QUERY_PARAMS}` | 用于筛选结果的可选查询参数。 | `limit=1` |

## 使用查询参数 {#using-query-parameters}

在列出资源时，您可以使用查询参数来分页并筛选结果。

### 分页 {#paging}

分页最常见的查询参数包括：

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `q` | 在选定字段中搜索的可选查询字符串。 查询字符串应当小写，并且可以用双引号括起来，以防止对其进行标记化并对特殊字符进行转义。 字符 `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 具有特殊含义，在查询字符串中出现时应使用反斜杠进行转义。 | `default` |
| `qop` | 对q查询字符串参数中的值应用AND或OR运算符。 | `AND` / `OR` |
| `field` | 将搜索限制到的可选字段列表。 此参数可重复，如下所示：field=field1[，字段=字段2，...] 和（路径表达式采用点分隔路径形式，如_instance.xdm：name） | `_instance.xdm:name` |
| `orderBy` | 按特定属性对结果进行排序。 添加 `-` 在标题之前(`orderby=-title`)将按标题降序对项目排序(Z-A)。 | `-repo:createdDate` |
| `limit` | 限制返回的决策规则数。 | `limit=5` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回决策规则列表，这些规则位于您有权访问的容器中。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2020-10-22T04:14:12.676802Z",
    "_embedded": {
     "results": [
        {
                "instanceId": "36693c30-0377-11eb-9dd8-d781cc064407",
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-30T23:46:51.379003Z",
                "repo:lastModifiedDate": "2020-10-02T05:06:36.780806Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Qualified for mortgage products",
                    "offerui:segmentModel": {
                        "name": "Qualified for mortgage products",
                        "canHaveFolder": true,
                        "isMissingAnsibleModel": false,
                        "description": "",
                        "deprecated": {
                            "reason": "",
                            "status": false
                        },
                        "schema": {
                            "name": "_xdm.context.profile",
                            "id": "some id"
                        },
                        "schemaName": "",
                        "expression": {
                            "xEventAttributesContainer": {
                                "itemType": "eventTypeCardContainer",
                                "logicalOperator": "then",
                                "exclude": false,
                                "items": []
                            },
                            "logicalOperator": "and",
                            "isValid": true,
                            "profileAttributesContainer": {
                                "itemType": "segmentContainer",
                                "logicalOperator": "and",
                                "exclude": false,
                                "items": [
                                    {
                                        "component": {
                                            "__entity__": true,
                                            "id": "profile._xcoree2etesting.productCategory",
                                            "type": "n"
                                        },
                                        "isPlaceholder": false,
                                        "comparisonType": "equals",
                                        "value": [
                                            "mortgage"
                                        ]
                                    }
                                ]
                 }
        },
                        "mergePolicyId": "3558157a-19cb-40b4-ba13-a5f5ce31b011",
                        "namespace": "ups"
                    },
                    "xdm:condition": {
                        "xdm:format": "pql/text",
                        "xdm:type": "PQL",
                        "xdm:value": "_xcoree2etesting.productCategory.equals(\"mortgage\", false)"
                    },
                    "xdm:definedOn": {},
                    "xdm:description": "",
                    "@id": "xcore:eligibility-rule:12333714edbf49e6"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#36693c30-0377-11eb-9dd8-d781cc064407",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/36693c30-0377-11eb-9dd8-d781cc064407",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 8,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=36693c30-0377-11eb-9dd8-d781cc064407&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
