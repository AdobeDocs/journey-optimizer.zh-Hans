---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 删除收藏集
description: 集合是基于营销人员定义的预定义条件的优惠的子集，如优惠的类别。
feature: Decision Management, API, Collections
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 21%

---

# 删除收藏集 {#delete-collection}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！[了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


有时可能有必要删除(DELETE)收藏集。 通过使用要删除的集合的[!DNL Offer Library]对`id` API执行DELETE请求来做到这一点。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持久性API的端点路径。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要删除的实体的ID。 | `offerCollection1234` |

**请求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' 
```

**响应**

成功的响应返回HTTP状态200和空白正文。

您可以通过尝试向收藏集发送查找(GET)请求来确认删除。 您应该会收到HTTP状态404 （未找到），因为该集合已被删除。
