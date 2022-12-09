---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件配置入门
description: 了解有关 [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 电子邮件配置入门 {#get-starte-email-config}

能够在 [!DNL Journey Optimizer]，则需要完成许多配置步骤。

1. 要确保最佳投放能力并保护您的声誉，请首先将用于通过发送电子邮件的子域委派给Adobe [!DNL Journey Optimizer]. 这些子域将确定要跟踪的网页和镜像页面URL等元素。 [了解更多](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 通过将随实例配置的IP地址分组在一起，提高电子邮件投放能力和声誉。 [了解更多](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 创建通道曲面并选取 **[!UICONTROL Email]** 渠道。 [了解更多](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每个电子邮件渠道表面中，配置发送电子邮件所需的所有技术参数。 [了解更多](email-settings.md)

   * 在这里，您选择要用于发送电子邮件的子域，以及要与表面关联的IP池。 [了解更多](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * 的 **[!UICONTROL Sender email]** 和 **[!UICONTROL Error email]** 地址必须使用当前选定的委派子域。 [了解更多](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. 当Adobe Experience Platform中有多个地址可用时，请确定要优先为收件人使用的电子邮件地址。 [了解更多](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理在向抑制列表发送电子邮件地址之前执行重试的天数。 [了解更多](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
