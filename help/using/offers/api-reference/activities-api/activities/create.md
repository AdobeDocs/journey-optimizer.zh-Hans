---
title: 创建决策
description: 决策包含通知选件选择的逻辑。
feature: 优惠
topic: 集成
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# 创建决策

在提供容器ID的同时，您可以通过向[!DNL Offer Library] API发出POST请求来创建决策（以前称为选件活动）。

## 接受和内容类型标头

下表显示了在请求标头中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;字段的有效值：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Activity 1",
        "xdm:startDate": "2020-10-01T16:00:00Z",
        "xdm:endDate": "2021-12-13T16:00:00Z",
        "xdm:status": "live",
        "xdm:criteria": [
            {
                "xdm:placements": [
                    "xcore:offer-placement:122204529514a2c0"
                ],
                "xdm:optionSelection": {
                    "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                }
            }
        ],
        "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef"
    }'
```

**响应**

成功的响应会返回有关新创建决策的信息，包括其唯一实例ID和版面`@id`。 您可以在后续步骤中使用实例ID来更新或删除您的决策。

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
