---
solution: Journey Optimizer
product: journey optimizer
title: 定义登陆页面预设
description: 了解如何配置环境以通过Journey Optimizer创建和使用登陆页面
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 5%

---

# 定义登陆页面预设 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="创建登陆页面预设"
>abstract="要构建登陆页面并通过Journey Optimizer利用该页面，您必须创建包含要使用的子域的登陆页面预设。"

When [创建登陆页面](../landing-pages/create-lp.md#create-a-lp)，则必须选择登陆页面预设才能构建登陆页面并通过该页面进行利用 **[!DNL Journey Optimizer]**.

## 访问登陆页面预设 {#access-lp-presets}

要访问登陆页面预设，请执行以下步骤。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单。

1. 选择 **[!UICONTROL 品牌策略]** > **[!UICONTROL 登陆页面预设]**.

   ![](assets/lp_presets-access.png)

1. 单击任意预设标签以访问登陆页面预设详细信息。

   ![](assets/lp_preset-details.png)

## 创建登陆页面预设 {#lp-create-preset}

要创建登陆页面预设，请执行以下步骤。

>[!NOTE]
>
>要创建预设，请确保您之前至少配置了一个登陆页面子域。 [了解如何](lp-subdomains.md)

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单，然后选择 **[!UICONTROL 品牌策略]** > **[!UICONTROL 登陆页面预设]**.

1. 选择 **[!UICONTROL 创建登陆页面预设]**.

   ![](assets/lp_create-preset-temp.png)

1. 输入预设的名称和描述。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

1. 从下拉列表中选择登陆页面子域。

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >要选择子域，请确保您之前至少配置了一个登陆页面子域。 [了解如何](#lp-subdomains)

   将显示与所选子域对应的设置。

1. 如果要为跟踪URL选择登陆页面子域，请检查 **[!UICONTROL 与登陆页面子域相同]** 选项。 [了解有关跟踪的更多信息](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登陆页面URL为“pages.mail.luma.com”，而跟踪URL为“data.mail.luma.com”，则可以选择“pages.mail.luma.com”作为跟踪子域。

1. 单击 **[!UICONTROL 提交]** 以确认创建登陆页面预设。 <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. 创建登陆页面预设后，该预设会显示在列表中，并且 **[!UICONTROL 活动]** 状态。 它已准备好用于您的登陆页面。

   ![](assets/lp-preset-active-temp.png)

您现在已准备好 [创建登陆页面](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**相关主题**：

* [登陆页面入门](../landing-pages/get-started-lp.md)
* [创建登陆页面](../landing-pages/create-lp.md#create-a-lp)
