---
title: 刪除個人化優惠
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 6%

---

# 删除个性化优惠 {#delete-personalized-offer}

有時可能必須移除(DELETE)個人化優惠方案。 只能刪除您在租使用者容器中建立的個人化優惠。 這是透過對「 」執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除的個人化優惠的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個人化優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試對個人化優惠進行查詢(GET)請求，以確認刪除。 您需要在請求中加入Accept標頭，但應該會收到HTTP狀態404 （找不到），因為個人化優惠已從容器中移除。
