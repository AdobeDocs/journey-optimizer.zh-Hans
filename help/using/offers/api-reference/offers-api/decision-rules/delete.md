---
title: 删除决策规则
description: 决策规则是添加到个性化优惠的约束，并应用于用户档案以确定资格。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 5%

---

# 删除决策规则

有时可能需要删除(DELETE)决策规则。 只能删除您在租户容器中创建的决策规则。 这是通过使用您要删除的决策规则的实例ID对[!DNL Offer Library] API执行DELETE请求来完成的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 决策规则所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新的决策规则的实例ID。 | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态202（无内容）和空白正文。

您可以通过尝试对决策规则进行查找(GET)请求来确认删除。 您需要在请求中包含一个“接受”标头，但应接收一个HTTP状态404（“未找到”），因为已从容器中删除了决策规则。
