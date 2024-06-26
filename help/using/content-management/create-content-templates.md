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
ht-degree: 14%

---


# 创建内容模板 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="定义您自己的内容模板"
>abstract="从头开始创建独立的自定义模板，这样您的内容便可在多个历程和营销活动中重复使用。"

创建内容模板的方法有两种：

* 使用左边栏从头开始创建内容模板 **[!UICONTROL 内容模板]** 菜单。 [了解如何操作](#create-template-from-scratch)

* 在营销活动或历程中设计内容时，请将其另存为模板。 [了解如何操作](#save-as-template)

保存后，您的内容模板即可用于营销活动或历程。 现在，无论是从头开始还是从上一个内容创建，您都可以在中构建任何内容时使用此模板 [!DNL Journey Optimizer]. [了解如何操作](#use-content-templates)

>[!NOTE]
>
>* 无论对内容模板所做的更改是实时的还是草稿的，都不会传播到营销活动或历程。
>
>* 同样，在营销策划或历程中使用模板时，您对营销策划和历程内容进行的任何编辑都不会影响以前使用的内容模板。

## 从头开始制定模板 {#create-template-from-scratch}

要从头开始创建内容模板，请执行以下步骤。

1. 通过以下方式访问内容模板列表 **[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]** 左侧菜单。

1. 选择 **[!UICONTROL 创建模板]**.

1. 填写模板详细信息并选择所需的渠道。

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >目前，除Web渠道外，所有渠道均可用。

1. 选择 **[!UICONTROL 类型]** 所选渠道的。

   ![](assets/content-template-type.png)

   * 对象 **[!UICONTROL 电子邮件]**，如果您选择 **[!UICONTROL 内容]**，您可以定义 [主题行](../email/create-email.md#define-email-content) 作为模板的一部分。 如果您选择 **[!UICONTROL HTML]**&#x200B;时，您只能定义电子邮件正文的内容。

   * 对象 **[!UICONTROL 短信]**， **[!UICONTROL 推送]**， **[!UICONTROL 应用程序内]** 和 **[!UICONTROL 直邮]**，则只有默认类型对当前渠道可用。 您仍需要选择它。

1. 从中选择或创建Adobe Experience Platform标记 **[!UICONTROL 标记]** 用于对模板进行分类以改进搜索的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 要向模板分配自定义或核心数据使用标签，您可以选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 单击 **[!UICONTROL 创建]** 并根据需要设计内容，就像您对历程或营销活动中的任何内容所做的那样 — 根据您选择的渠道。

   ![](assets/content-template-edition.png)

   请在以下部分中了解如何为不同渠道创建内容：
   * [定义电子邮件内容](../email/get-started-email-design.md)
   * [定义推送内容](../push/design-push.md)
   * [定义短信内容](../sms/create-sms.md#sms-content)
   * [定义直邮内容](../direct-mail/create-direct-mail.md)
   * [定义应用程序内内容](../in-app/design-in-app.md)

1. 如果您要创建 **[!UICONTROL 电子邮件]** 模板和 **[!UICONTROL HTML]** 键入，您可以测试您的内容。 [了解如何操作](#test-template)

1. 模板准备就绪后，单击 **[!UICONTROL 保存]**.

1. 单击模板名称旁边的箭头可返回 **[!UICONTROL 详细信息]** 屏幕。

   ![](assets/content-template-back.png)

现在，在中构建任何内容时，可使用此模板 [!DNL Journey Optimizer]. [了解如何操作](#use-content-templates)

## 将内容另存为内容模板 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何迁移您的消息"
>abstract="从 2022 年 7 月 25 日开始，消息菜单取消，现在直接在历程中创作消息。如果您重用历程中的旧消息，则需要将它们另存为模板。"

在营销活动或历程中设计任何内容时，您可以保存它以供将来重复使用。 为此，请执行以下步骤。

1. 从消息 **[!UICONTROL 编辑内容]** 屏幕上，单击 **[!UICONTROL 内容模板]** 按钮。

1. 选择 **[!UICONTROL 另存为内容模板]** 从下拉菜单中。

   ![](assets/content-template-button-save.png)

   如果您在 [向Designer发送电子邮件](../email/get-started-email-design.md)，您还可以从 **[!UICONTROL 更多]** 屏幕右上方的下拉列表。

   ![](assets/content-template-more-button-save.png)

1. 添加此模板的名称和描述。

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >当前渠道和类型会自动填充，且无法编辑。 对于从创建的电子邮件模板 [向Designer发送电子邮件](../email/get-started-email-design.md)， **[!UICONTROL HTML]** 类型被自动选中。

1. 从中选择或创建Adobe Experience Platform标记 **标记** 用于对模板进行分类的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 要向模板分配自定义或核心数据使用标签，您可以选择 **[!UICONTROL 管理访问权限]**. [了解详情](../administration/object-based-access.md)。

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 模板将保存到 **[!UICONTROL 内容模板]** 列表，可从访问 [!DNL Journey Optimizer] 专用菜单。 它会变成一个独立的内容模板，可以像该列表中的任何其他项目一样访问、编辑和删除该模板。 [了解详情](#access-manage-templates)

现在，在中构建任何内容时，都可以使用此模板 [!DNL Journey Optimizer]. [了解如何操作](#use-content-templates)

>[!NOTE]
>
>对该新模板所做的任何更改都不会传播到该模板所来自的内容。 同样，在该内容中编辑原始内容时，不会修改新模板。
