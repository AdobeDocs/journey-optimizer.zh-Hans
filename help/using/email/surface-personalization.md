---
solution: Journey Optimizer
product: journey optimizer
title: 个性化电子邮件配置设置
description: 了解如何在电子邮件渠道配置级别为您的设置定义个性化值
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 设置，电子邮件，配置，子域
badge: label="限量发布版"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: f8a6c2a3b27d5dca422dfdc868f802c6a10b001d
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 10%

---

# 个性化电子邮件配置设置 {#surface-personalization}

为了提高电子邮件设置的灵活性和控制力，[!DNL Journey Optimizer]允许您在创建电子邮件配置时定义子域和标头<!--and URL tracking parameters-->的个性化值。

>[!AVAILABILITY]
>
>电子邮件配置个性化当前仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

## 添加动态子域 {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="个性化不可用"
>abstract="这个配置在创建时没有任何个性化属性。如果需要个性化，请参阅文档了解解决问题的步骤。"

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="启用动态子域"
>abstract="创建电子邮件配置时，您可以根据使用个性化编辑器定义的条件设置动态子域。您最多可以添加 50 个动态子域。"

创建电子邮件配置时，您可以根据特定条件设置动态子域。

例如，如果您在法律上限制每个国家/地区使用专用电子邮件地址发送消息，则可以使用动态子域。 这样，您就可以创建单个配置，其中包含多个对应于不同国家/地区的发送子域，而不是为每个国家/地区创建多个配置。 然后，您可以将基于不同国家/地区的客户整合到一个营销活动中。

要在电子邮件渠道配置中定义动态子域，请执行以下步骤。

1. 在创建配置之前，请根据您的用例设置要用于发送电子邮件的子域。 [了解如何操作](../configuration/about-subdomain-delegation.md)

   例如，假设您想为不同的国家/地区使用不同的子域：设置一个特定于美国的子域，一个特定于英国的子域，等等。

1. 创建渠道配置。 [了解如何操作](../configuration/channel-surfaces.md)

1. 选择&#x200B;**[!UICONTROL 电子邮件]**&#x200B;渠道。

1. 在&#x200B;**子域**&#x200B;部分中，启用&#x200B;**[!UICONTROL 动态子域]**&#x200B;选项。

   ![](assets/surface-email-dynamic-subdomain.png)

1. 选择第一个&#x200B;**[!UICONTROL 条件]**&#x200B;字段旁边的“编辑”图标。

1. [个性化编辑器](../personalization/personalization-build-expressions.md)打开。 在此示例中，将诸如`Country`等条件设置为`US`。

   ![](assets/surface-email-edit-condition.png)

1. 选择要与此条件关联的子域。 [了解子域的详细信息](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >由于挂起[反馈循环](../reports/deliverability.md#feedback-loops)注册，某些子域当前不可选择。 此过程可能需要长达 10 个工作日。完成后，您可以从所有可用的子域中进行选择。<!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   所有位于美国的收件人都会收到使用该国家/地区所选子域的消息，这意味着所有涉及的URL（如镜像页面、跟踪URL或取消订阅链接）都将基于该子域进行填充。

1. 根据需要设置其他动态子域。 您最多可以添加50个项目。

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the configuration. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. 定义所有其他[电子邮件设置](email-settings.md)和[提交](../configuration/channel-surfaces.md#create-channel-surface)您的配置。

将一个或多个动态子域添加到配置后，将根据此配置的已解析动态子域填充以下项目：

* 所有URL（资源URL、镜像页面URL和跟踪URL）

* [取消订阅URL](email-settings.md#list-unsubscribe)

* **来自电子邮件**&#x200B;和&#x200B;**错误电子邮件**&#x200B;后缀

>[!NOTE]
>
>如果设置动态子域，然后禁用&#x200B;**[!UICONTROL 动态子域]**&#x200B;选项，则将删除所有动态值。 选择子域并提交配置以使更改生效。

## 个性化您的标题 {#personalize-header}

您还可以对配置中定义的所有标头参数使用个性化。

例如，如果您拥有多个品牌，则可以创建单个配置并为电子邮件标头使用个性化值。 这样，您就可以确保从不同品牌发送的所有电子邮件均使用正确的&#x200B;**发件人**&#x200B;名称和电子邮件发送给每位客户。 同样，当您的收件人在其电子邮件客户端软件中点击&#x200B;**回复**&#x200B;按钮时，您希望&#x200B;**回复**&#x200B;名称和电子邮件对应于正确用户的正确品牌。

要为配置标头参数使用个性化变量，请执行以下步骤。

>[!NOTE]
>
>您可以个性化所有&#x200B;**[!UICONTROL 标头参数]**&#x200B;字段，但&#x200B;**[!UICONTROL 错误电子邮件前缀]**&#x200B;字段除外。


1. 像往常一样定义标题参数。 [了解如何操作](email-settings.md#email-header)

1. 对于每个字段，选择编辑图标。

   ![](assets/surface-email-personalize-header.png)

1. [个性化编辑器](../personalization/personalization-build-expressions.md)打开。 根据需要定义条件，然后保存更改。

   例如，设置条件，如每个收件人都会收到来自其品牌代表的电子邮件。

   >[!NOTE]
   >
   >您只能选择&#x200B;**[!UICONTROL 配置文件属性]**&#x200B;和&#x200B;**[!UICONTROL 帮助程序函数]**。

1. 对要添加个性化的每个参数重复上述步骤。

>[!NOTE]
>
>如果您将一个或多个动态子域添加到配置，则将基于已解析的[动态子域](#dynamic-subdomains)填充&#x200B;**来自电子邮件**&#x200B;和&#x200B;**错误电子邮件**&#x200B;后缀。

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## 查看配置详细信息 {#view-surface-details}

当在营销活动或配置中将配置与个性化设置结合使用时，您可以直接在营销活动或配置中显示配置详细信息。 请按照以下步骤操作。

1. 创建电子邮件[营销活动](../campaigns/create-campaign.md)或[历程](../building-journeys/journey-gs.md)。

1. 选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮。

1. 单击&#x200B;**[!UICONTROL 查看配置详细信息]**&#x200B;按钮。

   ![](assets/campaign-view-surface-details.png)

1. 将显示&#x200B;**[!UICONTROL 投放设置]**&#x200B;窗口。 您可以查看所有配置设置，包括动态子域和个性化的标头参数。

   >[!NOTE]
   >
   >此屏幕中的所有信息均为只读。

1. 选择&#x200B;**[!UICONTROL 展开]**&#x200B;以显示动态子域的详细信息。

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
