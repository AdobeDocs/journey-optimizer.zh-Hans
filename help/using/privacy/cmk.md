---
solution: Journey Optimizer
product: journey optimizer
title: 客户托管密钥
description: 了解如何设置和管理 Adobe Journey Optimizer 的客户密钥。
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
TQID: https://experienceleague.adobe.com/yCl5CISD1-Xx6gfcK2sWdFWAeE0LicO-3r3YndB2cVQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 100%

---

# 设置和管理客户托管的密钥 {#cmk}

>[!AVAILABILITY]
>
>[!DNL Customer Managed Keys] 功能目前仅适用于已购买 [Healthcare Shield 或 Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=zh-Hans){target="_blank"} 附加产品的组织。

通过 Adobe Journey Optimizer，[Health Shield](https://www.adobe.com/trust/compliance/hipaa-ready.html){target="_blank"} 和 Privacy &amp; Security Shield 客户可以利用 Azure 客户托管密钥 (CMK) 并将其应用于数据。

Journey Optimizer 的设置过程包括两个部分，利用 Adobe Experience Platform 和 Customer Journey Analytics (CJA) 技术：

* 请按照 [Adobe Experience Platform 中的客户托管密钥](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=zh-Hans){target="_blank"}文档中列出的步骤进行操作。
* 请按照 [Customer Journey Analytics 中的客户托管密钥](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html?lang=zh-Hans){target="_blank"}文档中列出的步骤进行操作。

  即使您尚未购买 Customer Journey Analytics (CJA)，也必须完成此设置过程，因为背景会使用 CJA 的某些组件。

要完成设置过程，请参阅 [Adobe Experience Platform 中的客户托管密钥](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=zh-Hans){target="_blank"}文档的分步详细说明。

Adobe Experience Platform 和客户托管密钥在传输和存放数据时均会进行加密，从而确保数据安全。 无论您是否使用客户托管密钥，数据都会受到保护。

有关 Adobe Experience Platform 中数据加密的更多信息，请参阅数据加密[文档](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=zh-Hans){target="_blank"}。
