---
solution: Journey Optimizer
product: journey optimizer
title: 创建内容模板
description: 了解如何创建模板以在Journey Optimizer营销活动和历程中重用内容
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 15%

---


# 创建内容模板 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="定义您自己的内容模板"
>abstract="从头开始创建独立的自定义模板，这样您的内容便可在多个历程和营销活动中重复使用。"

创建内容模板的方法有两种：

* 使用左边栏&#x200B;**[!UICONTROL 内容模板]**&#x200B;菜单从头开始创建内容模板。 [了解如何操作](#create-template-from-scratch)

* 在营销活动或历程中设计内容时，请将其另存为模板。 [了解如何操作](#save-as-template)

保存后，您的内容模板即可用于营销活动或历程。 无论是从头开始还是从上一个内容创建，您现在都可以在[!DNL Journey Optimizer]中构建任何内容时使用此模板。 [了解如何操作](#use-content-templates)

>[!NOTE]
>
>* 无论对内容模板所做的更改是实时的还是草稿的，都不会传播到营销活动或历程。
>
>* 同样，在营销策划或历程中使用模板时，您对营销策划和历程内容进行的任何编辑都不会影响以前使用的内容模板。

## 从头开始制定模板 {#create-template-from-scratch}

要从头开始创建内容模板，请执行以下步骤。

1. 通过&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]**&#x200B;左侧菜单访问内容模板列表。

1. 选择&#x200B;**[!UICONTROL 创建模板]**。

1. 填写模板详细信息并选择所需的渠道。

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >目前，除Web渠道外，所有渠道均可用。

1. 为所选渠道选择&#x200B;**[!UICONTROL 类型]**。

   ![](assets/content-template-type.png)

   * 对于&#x200B;**[!UICONTROL 电子邮件]**，如果您选择&#x200B;**[!UICONTROL 内容]**，则可以将[主题行](../email/create-email.md#define-email-content)定义为模板的一部分。 如果选择&#x200B;**[!UICONTROL HTML]**，则只能定义电子邮件正文的内容。

   * 对于&#x200B;**[!UICONTROL SMS]**、**[!UICONTROL 推送]**、**[!UICONTROL 应用程序内]**&#x200B;和&#x200B;**[!UICONTROL 直邮]**，只有默认类型可用于当前渠道。 您仍需要选择它。

1. 从&#x200B;**[!UICONTROL 标记]**&#x200B;字段中选择或创建Adobe Experience Platform标记以对您的模板进行分类，从而改进搜索。 [了解详情](../start/search-filter-categorize.md#tags)

1. 若要将自定义或核心数据使用标签分配给模板，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;并根据需要设计内容，就像根据所选渠道对历程或营销活动中的任何内容所做的那样。

   ![](assets/content-template-edition.png)

   请在以下部分中了解如何为不同渠道创建内容：
   * [定义电子邮件内容](../email/get-started-email-design.md)
   * [定义推送内容](../push/design-push.md)
   * [定义短信内容](../sms/create-sms.md#sms-content)
   * [定义直邮内容](../direct-mail/create-direct-mail.md)
   * [定义应用程序内内容](../in-app/design-in-app.md)

1. 如果您正在创建类型为&#x200B;**[!UICONTROL HTML]**&#x200B;的&#x200B;**[!UICONTROL 电子邮件]**&#x200B;模板，则可以测试您的内容。 [了解如何操作](#test-template)

1. 模板准备就绪后，单击&#x200B;**[!UICONTROL 保存]**。

1. 单击模板名称旁边的箭头可返回&#x200B;**[!UICONTROL 详细信息]**&#x200B;屏幕。

   ![](assets/content-template-back.png)

此模板现在可以在[!DNL Journey Optimizer]中构建任何内容时使用。 [了解如何操作](#use-content-templates)

## 将内容另存为内容模板 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何迁移您的消息"
>abstract="从 2022 年 7 月 25 日开始，消息菜单取消，现在直接在历程中创作消息。如果您重用历程中的旧消息，则需要将它们另存为模板。"

在营销活动或历程中设计任何内容时，您可以保存它以供将来重复使用。 为此，请执行以下步骤。

1. 在消息&#x200B;**[!UICONTROL 编辑内容]**&#x200B;屏幕中，单击&#x200B;**[!UICONTROL 内容模板]**&#x200B;按钮。

1. 从下拉菜单中选择&#x200B;**[!UICONTROL 另存为内容模板]**。

   ![](assets/content-template-button-save.png)

   如果您在[电子邮件Designer](../email/get-started-email-design.md)中，您还可以从屏幕右上角的&#x200B;**[!UICONTROL 更多]**&#x200B;下拉列表中选择此选项。

   ![](assets/content-template-more-button-save.png)

1. 添加此模板的名称和描述。

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >当前渠道和类型会自动填充，且无法编辑。 对于从[电子邮件Designer](../email/get-started-email-design.md)创建的电子邮件HTML，**[!UICONTROL 模板]**&#x200B;类型是自动选择的。

1. 从&#x200B;**标记**&#x200B;字段中选择或创建Adobe Experience Platform标记以对您的模板进行分类。 [了解详情](../start/search-filter-categorize.md#tags)

1. 若要将自定义或核心数据使用标签分配给模板，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解详情](../administration/object-based-access.md)。

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 模板已保存到&#x200B;**[!UICONTROL 内容模板]**&#x200B;列表中，可从[!DNL Journey Optimizer]专用菜单访问。 它会变成一个独立的内容模板，可以像该列表中的任何其他项目一样访问、编辑和删除该模板。 [了解详情](#access-manage-templates)

现在，在[!DNL Journey Optimizer]中构建任何内容时，您可以使用此模板。 [了解如何操作](#use-content-templates)

>[!NOTE]
>
>对该新模板所做的任何更改都不会传播到该模板所来自的内容。 同样，在该内容中编辑原始内容时，不会修改新模板。