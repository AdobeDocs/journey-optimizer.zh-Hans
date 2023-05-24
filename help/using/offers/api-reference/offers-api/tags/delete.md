---
title: 刪除集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 5%

---

# 删除收藏集限定符 {#delete-tag}

有時可能必須移除(DELETE)集合限定詞（先前稱為「標籤」）。 只能刪除您在租使用者容器中建立的集合限定詞。 這是透過對「 」執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除之集合限定元的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合限定詞所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新的集合限定詞的執行個體識別碼。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**请求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試查詢(GET)集合限定詞來確認刪除。 您需要在要求中加入Accept標頭，但應該會收到HTTP狀態404 （找不到），因為集合限定詞已從容器中移除。
