---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件配置快速入门
description: 了解有关  [!DNL Journey Optimizer] 中电子邮件配置的更多信息
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: 电子邮件、配置、表面、子域
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 84%

---

# 电子邮件配置快速入门 {#get-starte-email-config}

要在 [!DNL Journey Optimizer] 中通过历程和营销活动发送电子邮件，需要完成多个配置步骤。

1. 为确保最佳投放效果并保护声誉，请首先&#x200B;**委派给 Adobe 您要用于通过 [!DNL Journey Optimizer] 发送电子邮件的子域**。 这些子域将确定要跟踪的网页和镜像页面 URL 等元素。 [了解详情](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 创建 IP 池，将使用实例设置的 **IP 地址分组在一起**。 [了解详情](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 创建&#x200B;**渠道配置**，然后选择&#x200B;**[!UICONTROL 电子邮件]**&#x200B;渠道。 [了解详情](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每个电子邮件渠道配置中，配置发送电子邮件所需的所有&#x200B;**技术参数**。 [了解详情](email-settings.md)

   * 在这里，您可以选择要用于发送电子邮件的子域，以及要与配置关联的 IP 池。 [了解详情](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * **[!UICONTROL 来自电子邮件前缀]**&#x200B;和&#x200B;**[!UICONTROL 错误电子邮件前缀]**&#x200B;使用当前选定的[委派的子域](../configuration/about-subdomain-delegation.md)。 或者，**[!UICONTROL 发件人姓名]**&#x200B;和&#x200B;**[!UICONTROL 发件人电子邮件]**&#x200B;可以识别其他传输方（完整的&#x200B;**发件人**&#x200B;地址，不与该子域后缀关联）。 [了解详情](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. 当 Adobe Experience Platform 中有多个地址可用时，确定要优先为收件人使用的&#x200B;**执行字段**。 [了解详情](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理在将电子邮件地址发送到禁止列表之前执行&#x200B;**重试**&#x200B;的天数。 [了解详情](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
