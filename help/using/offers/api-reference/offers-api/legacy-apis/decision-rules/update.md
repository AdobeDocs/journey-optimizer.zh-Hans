---
title: 更新决策规则
description: 决策规则是添加到个性化优惠并应用于用户档案以确定资格的约束。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 33da2c42-0c6c-49d3-bad8-1a85a5172cd8
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 9%

---

# 更新决策规则 {#update-decision-rule}

您可以通过向以下网站发出POST请求来创建后备优惠： [!DNL Offer Library] API，同时提供容器ID。

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *Content-Type* 和 *Accept* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策规则所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的决策规则的实例ID。 | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**请求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
        "op": "replace",
        "path": "/_instance/xdm:name",
        "value": "Sales and discounts rule"
        }
    ]'
```

**响应**

成功的响应会返回决策规则的更新详细信息，包括其唯一实例ID和决策规则 `@id`.


```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:25:43.705861Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
