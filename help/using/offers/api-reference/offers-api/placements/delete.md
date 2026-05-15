---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 删除版面
description: 投放位置是用于展示优惠的容器。
feature: Decision Management, API
badge: label="旧版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ACEsOlaOqRgSxKAkgd-X2IK0oL8IQ7vmv4RwTwyOMTA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 0%

---

# 删除投放位置 {#delete-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]的新决策功能“决策”现在可通过基于代码的体验和电子邮件渠道使用！ [了解详情](../../../../experience-decisioning/gs-experience-decisioning.md)


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

您可以通过对投放位置尝试查找(GET)请求来确认删除，由于投放位置已被删除，因此应该会收到HTTP状态404 （未找到）。
