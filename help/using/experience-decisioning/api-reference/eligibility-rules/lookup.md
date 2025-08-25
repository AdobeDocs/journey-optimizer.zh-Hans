---
title: 查找资格规则
description: 资格规则允许您根据要定位的内容（如配置文件属性和受众）定义符合条件的候选人。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: a74f4c87-0b89-4583-97f5-df8e2a30a19b
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---

# 查找资格规则 {#list-eligibility-rule}

您可以通过对选件库API发出GET请求（请求路径中包含该ID）来查找特定资格规则。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要查找的实体的ID。 | `rule1234` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的回应将返回资格规则的详细信息。

```json
{
    "created": "2024-10-28T01:18:08.506Z",
    "modified": "2024-10-28T01:18:08.506Z",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule"
    ],
    "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
    "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
    "id": "dps:eligibility-rule:19af09a9ae45a8d3",
    "name": "dasdsa",
    "description": "",
    "exdRule": false,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
    },
    "segmentModel": {
        "lifecycleState": "published",
        "expression": {
            "isValid": true,
            "logicalOperator": "and",
            "profileAttributesContainer": {
                "exclude": false,
                "items": [
                    {
                        "comparisonType": "equals",
                        "component": {
                            "id": "profile.personalEmail.address",
                            "__entity__": true,
                            "type": "Sz"
                        },
                        "isCaseSensitive": false,
                        "isPlaceholder": false,
                        "originalLocation": [],
                        "value": [
                            "youz@adobe.com"
                        ],
                        "itemType": "segmentRule"
                    }
                ],
                "logicalOperator": "and",
                "itemType": "segmentContainer"
            },
            "xEventAttributesContainer": {
                "exclude": false,
                "items": [],
                "logicalOperator": "then",
                "itemType": "eventTypeCardContainer"
            },
            "itemType": "segmentDefinition"
        },
        "isMissingAnsibleModel": false,
        "relationalExpression": false,
        "deprecated": {
            "status": false,
            "reason": ""
        },
        "description": "",
        "evaluationInfo": {
            "batch": {
                "enabled": true
            },
            "continuous": {
                "enabled": false
            },
            "synchronous": {
                "enabled": false
            }
        },
        "labels": [],
        "tags": [],
        "canHaveFolder": true,
        "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
        "name": "dasdsa",
        "namespace": "ups"
    }
}
```
