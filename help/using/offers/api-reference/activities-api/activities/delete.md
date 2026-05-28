---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 删除决策
description: 决策包含通知优惠选择的逻辑。
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/CV9NY9PmXlHXJBjlGAvnk7RN088i1Q6gvzTO5dTCWys
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 22%

---

# 删除决策 {#delete-decision}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


有时可能有必要删除(DELETE)决策。 通过使用要删除的决策的`id`对[!DNL Offer Library] API执行DELETE请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 参数 | 说明 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 要删除的实体的ID。 | `offerDecision1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试对决策进行查找(GET)请求来确认删除。 您应会收到HTTP状态404 （未找到），因为决策已被删除。
