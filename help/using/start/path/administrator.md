---
title: Journey Optimizer系统管理员入门
description: 作为系统管理员，了解如何使用Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# 系统管理员入门 {#get-started-sys-admins}

![管理员](assets/do-not-localize/user-2.png)

开始使用之前 [!DNL Adobe Journey Optimizer]，需要执行多个步骤来准备环境。  您必须执行这些步骤，以便 [数据工程师](data-engineer.md) 和 [历程实践者](marketer.md) 可以开始使用 [!DNL Adobe Journey Optimizer].


As a **系统管理员**，您需要 **了解产品配置文件和分配权限** 用于沙盒管理和渠道配置。 您还需要设置沙盒，并为可用的产品配置文件管理这些沙盒。 然后，您便能够将团队成员分配给产品配置文件。

这些功能可由 **[!UICONTROL Product administrators]** 具有Admin Console访问权限的访客。 [进一步了解Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/admin-guide.html){target=&quot;_blank&quot;}。

在以下页面中了解访问管理：

1. **创建沙箱** 将实例分区为单独的独立虚拟环境。 **沙箱** 创建于 [!DNL Journey Optimizer]. 在 [沙箱](../../administration/sandboxes.md) 中。

   >[!NOTE]
   >As a **系统管理员**，如果您看不到 **[!UICONTROL Sandboxes]** 菜单 [!DNL Journey Optimizer]，在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 了解如何在 [本页](../../administration/permissions.md#edit-product-profile).

1. **了解产品配置文件**. 产品配置文件是一组统一的权限，允许用户访问界面中的特定功能或对象。 在 [开箱即用的产品配置文件](../../administration/ootb-product-profiles.md) 中。

1. **设置权限** 对于产品配置文件，包括 **沙箱**，并通过将团队成员分配给不同的产品配置文件来授予他们访问权限。 此步骤在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 权限是唯一的权限，用于定义分配给的授权 **[!UICONTROL Product profile]**. 每个权限都通过历程、消息或选件等功能收集，这些功能表示 [!DNL Journey Optimizer]. 在 [权限级别](../../administration/high-low-permissions.md) 中。

此外，您还必须将需要访问Assets Essentials的用户添加到 **Assets Essentials消费者用户** 或/和 **Assets Essentials用户** 产品配置文件。 [有关更多信息，请参阅Assets Essentials文档](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

>[!NOTE]
>对于在2022年1月6日之前获取的Journey Optimizer产品，您必须部署 [!DNL Adobe Experience Manager Assets Essentials] 为贵组织。 在 [部署Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}部分。

访问 [!DNL Journey Optimizer] 首次配置了生产沙盒，并根据您的合同分配了特定数量的IP。

要创建您的历程并发送消息，请访问 **管理** 菜单。 浏览 **[!UICONTROL Channels]** 菜单来配置电子邮件消息和预设。

>[!NOTE]
>As a **系统管理员**，如果您看不到 **[!UICONTROL Channels]** 菜单 [!DNL Journey Optimizer]，在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 了解如何在 [本页](../../administration/permissions.md#edit-product-profile).

按照下面列出的步骤操作：

1. **配置消息和渠道**:定义预设、调整和自定义电子邮件和推送消息设置

   * 定义 **推送通知设置** 在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. [了解详情](../../messages/push-gs.md)

   * 创建 **消息预设** 配置电子邮件和推送通知消息所需的所有技术参数。 [了解详情](../../configuration/message-presets.md)

   * 管理 **重试** 会在向抑制列表发送电子邮件地址之前执行。 [了解详情](../../configuration/manage-suppression-list.md)

1. **委派子域**:对于要在Journey Optimizer中使用的任何新子域，第一步是将其委派。 [了解详情](../../configuration/about-subdomain-delegation.md)

   ![](../../assets/subdomain.png)

1. **创建IP池**:通过将与您的实例配置的IP地址分组到一起，可提高电子邮件的投放能力和声誉。 [了解详情](../../configuration/ip-pools.md)

   ![](../../assets/ip-pool.png)

1. **管理抑制和允许列表**:通过抑制和允许列表提高投放能力

   * A [抑制列表](../../messages/suppression-list.md) 包含要从投放中排除的电子邮件地址，因为发送给这些联系人可能会损害您的发送信誉和投放率。 您可以监控在历程中自动被排除在发送之外的所有电子邮件地址，例如无效地址、始终软退回的地址，并可能对您的电子邮件信誉造成不利影响的地址，以及针对您的某封电子邮件发出某种垃圾邮件投诉的收件人。 了解如何管理 [抑制列表](../../configuration/manage-suppression-list.md) 和 [重试](../../configuration/retries.md).
   ![](../../assets/suppression-list-filtering-example.png)

   * 的 [允许列表](../../messages/allow-list.md) 允许您指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。 这样可以防止您在测试环境中意外地向实际的客户地址发送电子邮件。 了解如何 [启用允许列表](../../messages/allow-list.md).
   详细了解 [!DNL Adobe Journey Optimizer] [本页](../../messages/deliverability.md).
