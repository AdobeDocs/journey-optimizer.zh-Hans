---
title: Journey Optimizer Get Started for System Admin
description: 作为系统管理员，了解如何使用Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 168579f8f560756282cb8ae8cb82a10e1227af02
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# 系统管理员入门

![管理员](assets/do-not-localize/user-2.png)

开始使用之前 [!DNL Adobe Journey Optimizer]，需要执行多个步骤来准备环境。  You must perform these steps so that the [Data Engineer](data-engineer.md) and [Journey Practicionner](marketer.md) can start working with [!DNL Adobe Journey Optimizer].


As a **系统管理员**，您需要 **了解产品配置文件和分配权限** 用于沙盒管理和渠道配置。 You also need to setup sandbox(es) and manage them for the available product profiles. 然后，您便能够将团队成员分配给产品配置文件。

These capabilities can be managed by **[!UICONTROL Product administrators]** that have access to the Admin console. [进一步了解Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/admin-guide.html){target=&quot;_blank&quot;}。

在以下页面中了解访问管理：

1. **创建沙箱** 将实例分区为单独的独立虚拟环境。 **Sandboxes** are created in [!DNL Journey Optimizer]. 在 [沙箱](../administration/sandboxes.md) 中。

   >[!NOTE]
   >As a **系统管理员**，如果您看不到 **[!UICONTROL Sandboxes]** 菜单 [!DNL Journey Optimizer]，在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 了解如何在 [本页](../administration/permissions.md#edit-product-profile).

1. **Understand product profiles**. 产品配置文件是一组统一的权限，允许用户访问界面中的特定功能或对象。 在 [开箱即用的产品配置文件](../administration/ootb-product-profiles.md) 中。

1. **设置权限** 对于产品配置文件，包括 **沙箱**，并通过将团队成员分配给不同的产品配置文件来授予他们访问权限。 此步骤在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 权限是唯一的权限，用于定义分配给的授权 **[!UICONTROL Product profile]**. 每个权限都通过历程、消息或选件等功能收集，这些功能表示 [!DNL Journey Optimizer]. 在 [权限级别](../administration/high-low-permissions.md) 中。

In addition, you must add users who need access to Assets Essentials to the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. [Read more in Assets Essentials documentation](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>For Journey Optimizer products obtained before January 6, 2022, you must deploy [!DNL Adobe Experience Manager Assets Essentials] for your organization. 在 [部署Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}部分。

When accessing [!DNL Journey Optimizer] for the first time, you are provisioned a production sandbox and allocated a certain number of IPs depending on your contract.

To be able to create your journeys and send messages, access the **ADMINISTRATION** menu. 浏览 **[!UICONTROL Channels]** 菜单来配置电子邮件消息和预设。

>[!NOTE]
>As a **System Administrator**, if you cannot see the **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer], update your permissions in the [Admin Console](https://adminconsole.adobe.com/){_blank}. 了解如何在 [本页](../administration/permissions.md#edit-product-profile).

Follow the steps listed below:

1. **Configure messages and channels**: define presets, adapt and customize email and push messages settings

   * Define **push notifications settings** in both [!DNL Adobe Experience Platform] and [!DNL Adobe Experience Platform Launch]. [了解详情](../push-gs.md)

   * Create **message presets** to configure all the technical parameters required for email and push notification messages. [了解详情](../configuration/message-presets.md)

   * 管理 **重试** 会在向抑制列表发送电子邮件地址之前执行。 [了解详情](../configuration/manage-suppression-list.md)

1. **委派子域**:对于要在Journey Optimizer中使用的任何新子域，第一步是将其委派。 [了解详情](../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Create IP pools**: improve your email deliverability and reputation by grouping together IP addresses provisioned with your instance. [了解详情](../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **管理抑制和允许列表**:通过抑制和允许列表提高投放能力

   * A [抑制列表](../suppression-list.md) 包含要从投放中排除的电子邮件地址，因为发送给这些联系人可能会损害您的发送信誉和投放率。 You can monitor all the email addresses that are automatically excluded from sending in a journey, such as invalid addresses, addresses that consistently soft-bounce, and could adversely affect your email reputation, and recipients who issue a spam complaint of some kind against one of your email messages. Learn how to manage the [suppression list](../configuration/manage-suppression-list.md) and [retries](../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * 的 [允许列表](../allow-list.md) 允许您指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。 This can prevent you from sending emails accidentally to real customer addresses when you are in a testing environment. 了解如何 [启用允许列表](../allow-list.md).
   Learn more about deliverability management in [!DNL Adobe Journey Optimizer] [in this page](../deliverability.md).
