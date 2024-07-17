---
solution: Journey Optimizer
product: journey optimizer
title: 使用手动翻译创建多语言内容
description: 了解如何在Journey Optimizer中使用手动翻译创建多语言内容
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: 入门、开始、内容、试验
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="限量发布版" type="Informative"
source-git-commit: 59dee15d2952438a074db57a94b3d896b38cd4f3
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 6%

---

# 使用手动翻译创建多语言内容 {#multilingual-manual}

>[!AVAILABILITY]
>
>目前，多语言内容仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。

使用手动流程，您可以轻松地直接在电子邮件、推送通知或短信营销活动和历程中翻译内容，从而为多语言消息提供精确的控制和自定义选项。 此外，您还可以使用“导入HTML”选项轻松导入预先存在的多语言内容。

请按照以下步骤使用手动翻译创建多语言内容：

1. [创建您的区域设置](#create-locale)。

1. [创建语言设置](#create-language-settings)。

1. [创建多语言内容](#create-a-multilingual-campaign)。

## 创建区域设置 {#create-locale}

在配置语言设置时（如[创建语言设置](#language-settings)部分中所述），如果多语言内容没有特定的区域设置，则可以灵活地使用&#x200B;**[!UICONTROL 翻译]**&#x200B;菜单创建所需数量的新区域设置。

1. 从&#x200B;**[!UICONTROL 内容管理]**&#x200B;菜单，访问&#x200B;**[!UICONTROL 翻译]**。

1. 在&#x200B;**[!UICONTROL 区域设置词典]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加区域设置]**。

   ![](assets/locale_1.png)

1. 从&#x200B;**[!UICONTROL 语言]**&#x200B;列表和相关的&#x200B;**[!UICONTROL 区域]**&#x200B;中选择您的区域设置代码。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以创建您的区域设置。

   ![](assets/locale_2.png)

## 创建语言设置 {#language-settings}

在此部分中，您可以设置管理多语言内容的主要语言及其关联的区域设置。 您还可以选择要用于查找与配置文件语言相关的信息的属性

1. 从&#x200B;**[!UICONTROL 管理]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 渠道]**。

1. 在&#x200B;**[!UICONTROL 语言设置]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 创建语言设置]**。

   ![](assets/multilingual-settings-1.png)

1. 键入&#x200B;**[!UICONTROL 语言设置]**&#x200B;的名称。

1. 选择与此设置关联的&#x200B;**[!UICONTROL 区域设置]**。 您最多可以添加50个区域设置。

   如果缺少&#x200B;**[!UICONTROL 区域设置]**，您可以预先从&#x200B;**[!UICONTROL 翻译]**&#x200B;菜单或通过API手动创建它。 请参阅[创建新区域设置](#create-locale)。

   ![](assets/multilingual-settings-2.png)

1. 从&#x200B;**[!UICONTROL 发送首选项]**&#x200B;菜单中，选择要查找以查找配置文件语言信息的属性。

   ![](assets/multilingual-settings-3.png)

1. 单击&#x200B;**[!UICONTROL 区域设置]**&#x200B;旁边的&#x200B;**[!UICONTROL 编辑]**&#x200B;可进一步对其进行个性化设置并添加&#x200B;**[!UICONTROL 配置文件首选项]**。

   ![](assets/multilingual-settings-4.png)

1. 从配置文件首选项下拉列表中选择其他&#x200B;**[!UICONTROL 区域设置]**，然后单击&#x200B;**[!UICONTROL 添加配置文件]**。

1. 访问&#x200B;**[!UICONTROL 区域设置]**&#x200B;的高级菜单以定义您的&#x200B;**[!UICONTROL 主要区域设置]**，如果未指定配置文件属性，则使用默认语言。

   您还可以从此高级菜单删除区域设置。

   ![](assets/multilingual-settings-5.png)

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以创建您的&#x200B;**[!UICONTROL 语言设置]**。

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## 创建多语言内容 {#create-multilingual-campaign}

在设置多语言内容后，您可以制作活动或历程并自定义每个选定区域设置的内容。

1. 首先根据您的要求创建和配置电子邮件、短信或推送通知[营销活动](../campaigns/create-campaign.md)或[历程](../building-journeys/journeys-message.md)。

   >[!AVAILABILITY]
   >
   >我们建议每个历程仅包含一个翻译项目。

1. 创建或导入原始内容，并根据需要对其进行个性化。

1. 创建主要内容后，单击&#x200B;**[!UICONTROL 保存]**&#x200B;并返回营销活动配置屏幕。

   ![](assets/multilingual-campaign-2.png)

1. 单击&#x200B;**[!UICONTROL 添加语言]**&#x200B;并选择您之前创建的&#x200B;**[!UICONTROL 语言设置]**。 [了解详情](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. 访问&#x200B;**[!UICONTROL 区域设置]**&#x200B;菜单的高级设置，然后选择&#x200B;**[!UICONTROL 将主要区域设置复制到所有区域设置]**。

   ![](assets/multilingual-campaign-4.png)

1. 现在，您的主要内容在选定&#x200B;**[!UICONTROL 区域设置]**&#x200B;中重复，请访问每个区域设置并单击&#x200B;**[!UICONTROL 编辑电子邮件正文]**&#x200B;以翻译您的内容。

   ![](assets/multilingual-campaign-5.png)

1. 您可以通过所选区域设置的&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单选择禁用或启用区域设置。

   ![](assets/multilingual-campaign-6.png)

1. 要停用您的多语言配置，请单击&#x200B;**[!UICONTROL 添加语言]**，然后选择要保留为本地语言的语言。

   ![](assets/multilingual-campaign-7.png)

1. 单击&#x200B;**[!UICONTROL 查看以激活]**&#x200B;以显示营销活动摘要。

   利用该摘要，可根据需要修改营销策划，并检查参数是否不正确或缺失。

1. 浏览多语言内容以查看每种语言的渲染方式。

   ![](assets/multilingual-campaign-8.png)

您现在可以激活营销活动或历程。 发送后，您可以在报表中衡量多语言历程或活动的影响。

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
