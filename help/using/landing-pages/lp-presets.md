---
solution: Journey Optimizer
product: journey optimizer
title: 定义登陆页面预设
description: 了解如何配置环境以通过Journey Optimizer创建和使用登陆页面
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: 登录，登陆页面，配置，环境，子域，预设
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8e5a904f9310385f5a8186159dedde9942624268
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 15%

---

# 定义登陆页面预设 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="创建登陆页面预设"
>abstract="为了生成登陆页面并通过 Journey Optimizer 使用它，您必须创建一个登陆页面预设，在其中包含要使用的子域。"

## 登陆页面预设入门 {#gs-lp-presets}

在[创建登陆页面](../landing-pages/create-lp.md#create-a-lp)时，您必须选择一个登陆页面预设，以便能够构建登陆页面并通过&#x200B;**[!DNL Journey Optimizer]**&#x200B;利用它。 预设包含用于基于此预设的登陆页面的子域。

在创建预设之前，请确保您之前已配置至少一个登陆页面子域。 [了解如何创建登陆页面子域](lp-subdomains.md)。

## 访问登陆页面预设 {#access-lp-presets}

要访问登陆页面预设，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单。

1. 选择&#x200B;**[!UICONTROL 登陆页面设置]** > **[!UICONTROL 登陆页面预设]**。

   ![](assets/lp_presets-access.png)

1. 单击任何预设标签可访问登陆页面预设详细信息。

   ![](assets/lp_preset-details.png)

## 创建登陆页面预设 {#lp-create-preset}

要创建登陆页面预设，请执行以下步骤：

1. 浏览&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 登陆页面设置]** > **[!UICONTROL 登陆页面预设]**。

1. 选择&#x200B;**[!UICONTROL 创建登陆页面预设]**。

   ![](assets/lp_create-preset-temp.png)

1. 输入预设的名称和描述。

   名称必须以字母(A-Z)开头，并且只包含字母数字字符、下划线`_`、点`.`和连字符`-`字符。

1. 从下拉列表中选择一个登陆页面子域。

   ![](assets/lp_preset-subdomain.png)

   要能够选择子域，请确保您之前已配置至少一个登陆页面子域。 [了解如何操作](#lp-subdomains)

   此时将显示与所选子域对应的设置。

1. 通过选中&#x200B;**[!UICONTROL 与登陆页面子域]**&#x200B;相同选项，可以为跟踪URL选择登陆页面子域。 [了解有关跟踪的更多信息](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登陆页面URL是“pages.mail.luma.com”，而跟踪URL是“data.mail.luma.com”，则可以选择将“pages.mail.luma.com”用作跟踪子域。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以确认创建登陆页面预设。<!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. 创建登陆页面预设后，该预设将显示在状态为&#x200B;**[!UICONTROL 活动]**&#x200B;的列表中。 该页面已准备好用于您的登陆页面。

您现在可以在[!DNL Journey Optimizer]中[创建登陆页面](../landing-pages/create-lp.md)。
<!--
>[!NOTE]
>
>Learn how to create channel configurations for push notifications and emails in [this section](channel-surfaces.md).-->

**相关主题**：

* [登陆页面入门](../landing-pages/get-started-lp.md)
* [创建登陆页面](../landing-pages/create-lp.md#create-a-lp)
