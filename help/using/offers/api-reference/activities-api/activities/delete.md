---
title: 删除决策
description: 决策包含通知优惠选择的逻辑。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 5%

---

# 删除决策 {#delete-decision}

有时可能有必要删除(DELETE)决策。 只能删除您在租户容器中创建的决策。 DELETE这是通过对 [!DNL Offer Library] API使用要删除的备用选件的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 决策的实例ID。 | `f88c9be0-1245-11eb-8622-b77b60702882` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态202（无内容）和一个空白正文。

您可以通过尝试对决策进行查找(GET)请求来确认删除。 您需要在请求中包含“接受”标头，但应会收到HTTP状态404（未找到），因为决策已从容器中删除。
