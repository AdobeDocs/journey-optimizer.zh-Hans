---
title: 更新后备优惠
description: 如果客户不符合其他优惠的条件，则会向客户发送后备优惠
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
source-git-commit: 118eddf540d1dfb3a30edb0b877189ca908944b1
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 10%

---

# 更新后备优惠 {#update-fallback-offer}

您可以通过对以下网站发出PATCH请求，修改或更新容器中的后备优惠： [!DNL Offer Library] API。

有关JSON补丁程序的更多信息（包括可用的操作），请参阅官方网站上的 [JSON修补程序文档](https://jsonpatch.com/).

## 接受和内容类型标头 {#accept-and-content-type-headers}

下表显示了包含 *内容类型* 和 *接受* 请求标头中的字段：

| 标头名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 备用选件所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 后备优惠的实例ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**请求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:status",
            "value": "approved"
        }
    ]
```

| 参数 | 描述 |
| --------- | ----------- |
| `op` | 用于定义更新连接所需的操作的操作调用。 操作包括： `add`， `replace`、和 `remove`. |
| `path` | 要更新的参数的路径。 |
| `value` | 您希望使用更新参数的新值。 |

**响应**

成功的响应将返回备用选件的更新详细信息，包括其唯一的实例ID和备用选件 `@id`.

```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2020-10-21T22:33:08.676919Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
