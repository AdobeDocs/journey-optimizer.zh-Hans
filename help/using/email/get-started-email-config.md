---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件配置入门
description: 了解有关  [!DNL Journey Optimizer] 中电子邮件配置的更多信息
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: 电子邮件、配置、表面、子域
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 电子邮件配置入门 {#get-starte-email-config}

要在 [!DNL Journey Optimizer] 中通过历程和营销活动发送电子邮件，需要完成多个配置步骤。

1. 为确保最佳投放效果并保护声誉，请首先&#x200B;**委派给 Adobe 您要用于通过 [!DNL Journey Optimizer] 发送电子邮件的子域**。这些子域将确定要跟踪的网页和镜像页面 URL 等元素。[了解详情](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 创建 IP 池，将使用实例设置的 **IP 地址分组在一起**。[了解详情](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 创建&#x200B;**渠道配置**，然后选择&#x200B;**[!UICONTROL 电子邮件]**&#x200B;渠道。[了解详情](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每个电子邮件渠道配置中，配置发送电子邮件所需的所有&#x200B;**技术参数**。[了解详情](email-settings.md)

   * 在这里，您可以选择要用于发送电子邮件的子域，以及要与配置关联的 IP 池。[了解详情](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * **[!UICONTROL 发件人电子邮件]**&#x200B;和&#x200B;**[!UICONTROL 错误电子邮件]**&#x200B;地址必须使用当前选定的委派子域。[了解详情](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. 当 Adobe Experience Platform 中有多个地址可用时，确定要优先为收件人使用的&#x200B;**执行字段**。[了解详情](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理在将电子邮件地址发送到禁止列表之前执行&#x200B;**重试**&#x200B;的天数。[了解详情](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
