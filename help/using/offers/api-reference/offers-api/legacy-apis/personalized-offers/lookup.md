---
title: 查找个性化优惠
description: 个性化优惠是基于资格规则和约束的可自定义营销消息。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 679f2229-19c6-47f9-b293-e1c3c8dcb61e
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# 查找个性化优惠 {#look-up-personalized-offer}

个性化优惠是基于资格规则和约束的可自定义营销消息。

您可以通过向&#x200B;**优惠库** APIGET请求，在请求路径中包含个性化优惠`@id`或个性化优惠的名称，来查找特定的个性化优惠。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 个性化优惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | 定义与个性化优惠关联的架构。 | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | 用于匹配实体的`@id`属性的字符串。 字符串完全匹配。 参数“id”和“name”不能一起使用。 | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | 用于匹配实体的xdm：name属性的字符串。 字符串与大小写完全匹配，但可以使用通配符。 参数`id`和`name`不能一起使用 | `Discount offer` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应将返回投放位置的详细信息，包括有关容器ID、实例ID和唯一个性化优惠`@id`的信息。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2023-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2023-10-20T20:01:02.927874Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2023-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
