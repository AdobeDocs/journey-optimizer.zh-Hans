---
solution: Journey Optimizer
product: journey optimizer
title: 多语言内容入门
description: 了解有关 Journey Optimizer 中的多语言内容的更多信息
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: 入门、开始、内容、试验
exl-id: b57683b4-6dcc-4f6c-a8b2-4ba371d78d21
source-git-commit: 766530a2f443a2795d61161c9d08de299a5363d6
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 32%

---

# 多语言内容入门 {#multilingual-gs}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_homepage"
>title="翻译"
>abstract="多语言功能允许您在单个营销活动或历程中轻松创建多种语言的内容。通过翻译页面，您可以设置项目、选择翻译提供商或管理特定语言环境的词典"

多语言功能使您能够轻松地在单个活动或历程中以多种语言创建内容。 利用此功能，您可以在编辑活动时切换语言，简化整个编辑过程，并提高有效管理多语言内容的能力。

使用Journey Optimizer，您可以通过两种不同的方法创建多语言内容：

* **手动翻译**：直接在Email Designer中翻译您的内容或导入现有的多语言内容。 [了解详情](multilingual-manual.md)

* **自动翻译**：将内容发送到您的首选语言提供商以进行自动翻译。 [了解详情](multilingual-automated.md)

</br>

![](assets/translation_schema.png)

## 先决条件 {#prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_error"
>title="翻译错误"
>abstract="如果您无法访问翻译页面，这可能是因为未启用翻译功能。要解决此问题，您需要确保您的组织和沙盒管理员激活了翻译功能。"

Adobe Journey Optimizer目前与翻译提供商集成，这些提供商独立于Adobe Journey Optimizer提供第三方翻译服务（机器翻译或人工翻译）。

在添加所选翻译提供商之前，必须使用该适用提供商创建一个帐户。

您对翻译提供商翻译服务的使用受该适用提供商提供的其他条款和条件的约束。  作为第三方解决方案，Adobe Journey Optimizer用户可通过集成使用翻译服务。  Adobe不控制，也不负责第三方产品。

有关翻译的任何问题或协助请求，请与适用的翻译提供商联系。

对于多语言内容，必须定义以下设置：

* 要使用Journey Optimizer中的翻译功能，您需要将API分配给相应的角色。 [了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#assign-api-to-a-role)

* 要开始创建多语言内容，需要向用户授予&#x200B;**[!UICONTROL 管理语言设置]**&#x200B;权限。 对于自动流，用户还需要与&#x200B;**[!UICONTROL 翻译服务]**&#x200B;功能相关的权限。 [了解有关权限的更多信息](../administration/permissions.md)

+++ 了解如何分配与多语言相关的权限

   1. 在&#x200B;**权限**&#x200B;产品中，转到&#x200B;**角色**&#x200B;选项卡并选择所需的&#x200B;**角色**。

   1. 单击&#x200B;**编辑**，修改权限。

   1. 添加&#x200B;**翻译服务**&#x200B;资源，然后从下拉菜单中选择相应的多语言权限。

      ![](assets/multilingual-permission.png){zoomable="yes"}

   1. 单击&#x200B;**保存**&#x200B;以应用更改。

      任何已分配此角色的用户的权限都将自动更新。

   1. 要将此角色分配给新用户，请导航到&#x200B;**角色**&#x200B;仪表板中的&#x200B;**用户**&#x200B;选项卡，然后单击&#x200B;**添加用户**。

   1. 输入用户名、电子邮件地址或从列表中选择，然后单击&#x200B;**保存**。

   1. 如果之前没有创建用户，请参阅[此文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

* 如果您无法访问翻译页面，则需要启用翻译功能并获得&#x200B;**[!UICONTROL 翻译服务]**&#x200B;相关权限。 [了解详情](../administration/ootb-permissions.md)

+++ 了解如何启用翻译功能

   1. 如果您看到以下错误页面，则表示尚未启用&#x200B;**[!UICONTROL 翻译]**&#x200B;功能。 请联系您的组织和沙盒管理员以请求访问权限。

  ![](assets/multi-troubleshoot.png)

   1. 您的管理员需要导航到左侧边栏中的&#x200B;**[!UICONTROL 翻译]**&#x200B;菜单。

      系统将自动启用翻译功能。

   1. 成功启用该功能后，您将能够访问&#x200B;**[!UICONTROL 翻译]**&#x200B;页面，以及&#x200B;**[!UICONTROL 项目]**、**[!UICONTROL 提供商]**&#x200B;和&#x200B;**[!UICONTROL 区域设置]**&#x200B;选项卡。

   1. 如果此过程失败，您仍会看到相同的错误页面。 在这种情况下，请与Adobe代表联系以获取更多帮助。

+++

## 操作方法视频 {#video}

了解如何在单个活动或历程中以多种语言创建内容。

>[!VIDEO](https://video.tv.adobe.com/v/3430921/)
