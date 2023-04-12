---
solution: Journey Optimizer
product: journey optimizer
title: 使用AEM模板
description: 了解如何在AEM中创建模板并将其导出到Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informitive"
source-git-commit: 7a044f7c048ba797e7b857212f6d6b0cf2644b5d
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 2%

---

# 使用Adobe Experience Manager模板 {#aem-templates}

>[!AVAILABILITY]
>
>与Adobe Experience Manager的集成当前仅作为测试版提供给部分用户。
> 作为测试版用户，请使用 [此窗体](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} 来分享反馈。

借助Adobe Journey Optimizer，您可以通过Adobe Experience Manager网站创建自定义量身定制的消息。 首先，使用Adobe Experience Manager的内容源设计模板，然后将其发送到Adobe Journey Optimizer。 共享后，即可在Adobe Journey Optimizer的电子邮件设计工具中访问这些模板，从而简化制作消息并将其发送给所需受众的过程。

## 先决条件 {#prerequisites}

在开始使用此功能之前，请确保您符合以下要求：

* **Experience Manager设置**

   此功能在 [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   作为测试版计划的一部分，Cloud Service配置由Adobe Experience Manager中的Adobe执行，以连接到Adobe Journey Optimizer。

* **Permissions**

   要在Adobe Journey Optimizer中创建、编辑和删除内容模板，您必须具有 **[!DNL Manage Library Items]** 包含的权限 **[!DNL Content Library Manager]** 产品配置文件。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

## 护栏和限制{#aem-templates-limitations}

要进一步优化Adobe Journey Optimizer对Adobe Experience Manager的使用，请务必注意以下附加护栏和限制：

* 要使Experience Manager模板中的个性化生效，需要使用正确的Journey Optimizer语法。 [了解详情](../personalization/personalization-syntax.md)

* 当前不支持批量模板导出，必须单独导出模板。

* 当前无法在Experience Manager和Journey Optimizer之间同步。 如果在将Experience Manager模板发送到Journey Optimizer后对该模板进行了更改，则用户将需要重新导出该模板，然后将其重新发送到Journey Optimizer。

## 将模板发送到Journey Optimizer{#aem-templates-send}

要将Adobe Experience Manager模板导出到Adobe Journey Optimizer，请执行以下步骤：

1. 从Adobe Experience Manager主页中，选择 **[!UICONTROL 出站营销]**.

   ![](assets/aem-outbound-menu.png)

1. 在内容库中，您可以使用之前配置的模板或从头开始创建一个模板。 [了解详情](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. 通过将Journey Optimizer个性化语法纳入模板，您可以增强其自定义功能。 [了解详情](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. 选择要导出到Journey Optimizer的模板，然后单击 **[!UICONTROL 发送到]** 中。

   ![](assets/aem-advanced-menu.png)

1. 输入 **[!UICONTROL 名称]** ，然后选择目标 **[!UICONTROL 沙盒]**.

   ![](assets/aem-send-template-settings.png)

1. 在单击 **[!UICONTROL 发送]** 按钮，将开始导出过程。 导出完成后，您将在用户界面中看到以下消息：“模板“XX”已成功发送到AJO。

模板将添加到选定沙盒的Adobe Journey Optimizer内容模板。

## 使用和个性化Adobe Experience Manager模板{#aem-templates-perso}

在Journey Optimizer中将Experience Manager模板作为内容模板提供后，您可以识别并整合电子邮件的必需内容，包括个性化内容。

1. 在Journey Optimizer，从 **[!UICONTROL 内容模板]** 菜单访问导入的模板。

   ![](assets/aem_ajo_1.png)

1. 通过单击 **[!UICONTROL 警报]** 按钮，您可以快速检查是否缺少任何重要设置。 这将有助于确保正确配置消息，并防止出现任何潜在错误或问题。

   ![](assets/aem_ajo_2.png)

1. 在 **[!UICONTROL 模板属性]** 窗口，单击 **[!UICONTROL 管理访问权限]** 按钮来为模板分配自定义或核心数据使用情况标签。 [了解有关对象级别访问控制(OLAC)的更多信息](../administration/object-based-access.md)

1. 要进一步个性化您的Experience Manager模板并向内容中添加自定义个性化，请单击 **[!UICONTROL 编辑内容]**. 这样，您就可以轻松地进行更改并根据特定需求定制模板。 [了解详情](get-started-email-design.md)

   >[!NOTE]
   >
   > 如果要编辑和个性化模板，则只能使用兼容性模式。

1. 内容模板准备就绪后， [测试和验证](content-templates.md#test-template).

1. 定义内容后，您可以在通过浏览 **[!UICONTROL 保存的模板]** 收藏集。 然后，选择 **[!UICONTROL 使用此模板]**.

   ![](assets/aem_ajo_3.png)

1. 您现在可以编辑和个性化内容。 有关如何构建电子邮件内容的更多信息，请参阅此 [页面](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. 如果向Experience Manager模板添加了个性化内容，请单击 **[!UICONTROL 模拟内容]** 以使用测试用户档案预览消息的显示方式。

[了解有关预览和测试用户档案的更多信息](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. 查看消息预览时，任何个性化元素都会自动替换为选定测试用户档案中的相应数据。

   如果需要，可以通过 **[!UICONTROL 管理测试用户档案]** 按钮。

   ![](assets/aem_ajo_7.png)

准备好电子邮件后，完成 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md)，然后激活以发送消息。
