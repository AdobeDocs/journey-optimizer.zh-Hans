---
title: 删除决策
description: 决策包含通知优惠选择的逻辑。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: ef22b6183c7646cca8636f4a7e4dd87c8f88e8ce
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 8%

---


# 删除决策 {#delete-decision}

有时可能有必要删除(DELETE)决策。 只能删除您在租户容器中创建的决策。 DELETE这是通过对 [!DNL Offer Library] API使用要删除的回退选件的$id。

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
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
	@@ -37,6 +35,6 @@ curl -X DELETE \

**Response**

A successful response returns HTTP status 202 (No Content) and a blank body.

You can confirm the deletion by attempting a lookup (GET) request to the decision. You will need to include an Accept header in the request, but should receive an HTTP status 404 (Not Found) because the decision has been removed from the container.

