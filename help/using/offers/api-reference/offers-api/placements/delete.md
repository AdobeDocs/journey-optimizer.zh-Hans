---
title: 删除版面
description: 投放位置是用于展示优惠的容器。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 7%

---

# 删除投放位置 {#delete-placement}

有时可能需要删除(DELETE)投放位置。 通过使用要删除的投放位置的ID向[!DNL Offer Library] API执行DELETE请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要更新的投放位置的实例ID。 | `offerPlacement1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对投放位置进行查找(GET)请求来确认删除，由于投放位置已被删除，因此应该会收到HTTP状态404 （未找到）。
