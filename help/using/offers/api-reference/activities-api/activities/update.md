---
title: 更新决策
description: 决策包含通知选件选择的逻辑。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 98c5ccf9-2a7f-4129-a520-d0671a86e13d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---

# 更新决策

您可以通过向 [!DNL Offer Library] API。

有关JSON修补程序（包括可用操作）的更多信息，请参阅 [JSON修补程序文档](http://jsonpatch.com/).

## 接受和内容类型标头

下表显示构成 *Content-Type* 和 *接受* 请求标题中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 决策的实例ID。 | `f88c9be0-1245-11eb-8622-b77b60702882` |

**请求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Example Activity Name"
        }
    ]'
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 操作调用，用于定义更新连接所需的操作。 操作包括： `add`, `replace`和 `remove`. |
| `path` | 要更新的参数的路径。 |
| `value` | 要使用更新参数的新值。 |

**响应**

成功的响应会返回决策的更新详细信息，包括其唯一实例ID和决策 `@id`.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T21:28:24.284719Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
