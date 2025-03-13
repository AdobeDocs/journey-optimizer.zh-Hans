---
solution: Journey Optimizer
product: journey optimizer
title: 管理品牌
description: 了解如何创建和管理品牌指南
badge: label="Beta 版" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: d80f9309cfff4307b1b37ce44b037730a374d4a2
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 38%

---

# 创建和管理品牌 {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="开始使用品牌"
>abstract="创建并定制您自己的品牌，以塑造您独特的视觉和语言形象，同时更轻松地创作出符合您品牌风格和声音的内容。"

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="选择您的品牌"
>abstract="选择您的品牌，以确保所有 AI 生成的内容都符合您品牌的规范和指导方针。"

>[!CONTEXTUALHELP]
>id="ajo_brand_score_overview"
>title="品牌选择"
>abstract="选择您的品牌，以确保您的内容制作符合其特定的指导方针、标准和身份，从而保持一致性和品牌完整性。"

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="品牌一致性得分"
>abstract="您的品牌一致性得分衡量的是您的内容遵循品牌指导方针的程度，确保颜色、字体、徽标、图像和写作风格的一致性。"

>[!CONTEXTUALHELP]
>id="ajo_brand_colors"
>title="颜色分数"
>abstract="颜色分数"

>[!CONTEXTUALHELP]
>id="ajo_brand_fonts"
>title="字体分数"
>abstract="字体分数"

>[!CONTEXTUALHELP]
>id="ajo_brand_logos"
>title="Logos分数"
>abstract="Logos分数"

>[!CONTEXTUALHELP]
>id="ajo_brand_imagery"
>title="图像得分"
>abstract="图像得分"

>[!CONTEXTUALHELP]
>id="ajo_brand_writing_style"
>title="书写样式分数"
>abstract="书写样式分数"

>[!AVAILABILITY]
>
>此功能作为专用测试版发布。 在未来版本中，将逐步向所有客户提供。

品牌指南是一组详细的规则和标准，用于建立品牌的视觉和语言标识。 它们用作参考，以在所有营销和通信平台上保持一致的品牌代表性。

在[!DNL Journey Optimizer]中，您现在可以选择手动输入和组织品牌详细信息或上传品牌准则文档以进行自动信息提取。

## 访问品牌 {#generative-access}

要访问[!DNL Adobe Journey Optimizer]中的&#x200B;**[!UICONTROL 品牌]**&#x200B;菜单，需要向用户授予&#x200B;**[!UICONTROL 托管品牌套件]**&#x200B;或&#x200B;**[!UICONTROL 启用AI助手]**&#x200B;权限。 [了解详情](../administration/permissions.md)

+++  了解如何分配品牌相关权限

1. 在&#x200B;**权限**&#x200B;产品中，转到&#x200B;**角色**&#x200B;选项卡并选择所需的&#x200B;**角色**。

1. 单击&#x200B;**编辑**，修改权限。

1. 添加&#x200B;**AI助手**&#x200B;资源，然后从下拉菜单中选择&#x200B;**托管品牌套件**&#x200B;或&#x200B;**[!UICONTROL 启用Ai助手]**。

   请注意，**[!UICONTROL 启用Ai助手]**&#x200B;权限仅提供对&#x200B;**[!UICONTROL 品牌]**&#x200B;菜单的只读访问权限。

   ![](assets/brands-permission.png){zoomable="yes"}

1. 单击&#x200B;**保存**&#x200B;以应用更改。

   任何已分配此角色的用户的权限都将自动更新。

1. 要将此角色分配给新用户，请导航到&#x200B;**角色**&#x200B;仪表板中的&#x200B;**用户**&#x200B;选项卡，然后单击&#x200B;**添加用户**。

1. 输入用户名、电子邮件地址或从列表中选择，然后单击&#x200B;**保存**。

1. 如果之前没有创建用户，请参阅[此文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

## 创建您的品牌 {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="创建您的品牌"
>abstract="输入您的品牌名称并上传您的品牌指导方针文件。该工具会自动提取关键细节，使维护品牌身份更加容易。"

要创建和管理品牌指南，您可以自己输入详细信息，也可以上传品牌指南文档以自动提取信息：

1. 在&#x200B;**[!UICONTROL 品牌]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 创建品牌]**。

   ![](assets/brands-1.png)

1. 为您的品牌输入&#x200B;**[!UICONTROL 名称]**。

1. 拖放或选择您的文件以上传品牌指南并自动提取相关的品牌信息。 单击&#x200B;**[!UICONTROL 创建品牌]**。

   信息提取过程现在开始。 请注意，它可能需要几分钟才能完成。

   ![](assets/brands-2.png)

1. 您的内容和可视化创建标准现在将自动填充。 浏览不同的选项卡以根据需要调整信息。

1. 在&#x200B;**[!UICONTROL 写入样式]**&#x200B;选项卡中，单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加准则或排除项，包括示例。

   ![](assets/brands-3.png)

1. 在&#x200B;**[!UICONTROL 可视内容]**&#x200B;选项卡中，单击![](assets/do-not-localize/Smock_Add_18_N.svg)以添加其他准则或排除项。

1. 要添加显示正确用法的图像，请选择&#x200B;**[!UICONTROL 示例]**&#x200B;并单击&#x200B;**[!UICONTROL 选择图像]**。 您还可以添加显示不正确用法的图像作为排除示例。

   ![](assets/brands-4.png)

1. 配置完毕后，单击&#x200B;**[!UICONTROL 保存]**，然后单击&#x200B;**[!UICONTROL 发布]**，以便在AI助手中提供您的品牌指南。

1. 要对已发布的品牌进行修改，请单击&#x200B;**[!UICONTROL 编辑品牌]**。

   >[!NOTE]
   >
   >这会在编辑模式下创建一个临时副本，并在发布后替换实时版本。

   ![](assets/brands-8.png)

1. 在&#x200B;**[!UICONTROL Brands]**&#x200B;仪表板中，单击![](assets/do-not-localize/Smock_More_18_N.svg)图标打开高级菜单，以执行以下操作：

   * 查看品牌
   * Edit
   * 复制
   * 发布
   * 取消发布
   * Delete

   ![](assets/brands-6.png)

现在，可从AI助手菜单中的&#x200B;**[!UICONTROL 品牌]**&#x200B;下拉菜单访问您的品牌指南，使其生成符合您规范的内容和资产。 [了解有关AI助手的详细信息](gs-generative.md)

![](assets/brands-7.png)
