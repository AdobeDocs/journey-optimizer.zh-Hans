---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 删除后备产品建议
description: 如果客户不符合其他优惠的条件，则会向客户发送后备优惠
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 22%

---


# 删除后备产品建议 {#delete-fallback-offer}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！[了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


有时可能有必要删除(DELETE)备用选件。 通过使用要删除的备用DELETE的ID对[!DNL Offer Library] API执行选件请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `fallbackOffer1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对选件进行查找(GET)请求来确认删除，由于备用选件已删除，因此应该会收到HTTP状态404 （未找到）。
