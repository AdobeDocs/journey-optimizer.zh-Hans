---
solution: Journey Optimizer
product: journey optimizer
title: 创建内容模板
description: 了解如何创建模板以在Journey Optimizer营销活动和历程中重复使用内容
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 2%

---

# 使用内容模板 {#content-templates}

为了加快和改进设计过程，您可以创建独立模板以在 [!DNL Journey Optimizer] 营销活动和历程。

此功能允许面向内容的用户在营销活动或历程之外使用模板。 然后，营销用户可以在自己的历程或营销活动中重复使用和调整这些独立的内容模板。

例如，贵公司内的用户仅负责内容，因此无权访问营销活动或历程。 但是，此用户可以创建一个电子邮件模板，贵组织的营销人员将能够选择该模板以用于所有电子邮件，作为起点。

➡️ [在此视频中了解如何创建和使用模板](#video-templates)

>[!CAUTION]
>
>要创建、编辑和删除内容模板，您必须具有 **[!DNL Manage Library Items]** 包含的权限 **[!DNL Content Library Manager]** 产品配置文件。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

## 访问和管理模板 {#access-manage-templates}

要访问内容模板列表，请选择 **[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]** 菜单中。

![](assets/content-template-list.png)

在当前沙盒上创建的所有模板 — 从历程或使用 [另存为模板](#save-as-template) 选项(从 **[!UICONTROL 内容模板]** 菜单 — 显示。

您可以按创建或修改日期对内容模板进行排序。 您还可以选择仅显示您创建或修改的项目。

![](assets/content-template-list-filters.png)

要编辑模板内容，请从列表中单击所需的项目，然后选择 **[!UICONTROL 编辑内容]**.

![](assets/content-template-list-edit.png)

要删除模板，请选择所需模板旁边的垃圾桶图标。

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>编辑或删除模板时，包括使用此模板创建的电子邮件在内的营销活动或历程将不受影响。

## 创建内容模板 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="定义您自己的内容模板"
>abstract="从头开始创建一个独立的自定义模板，以使内容可在多个历程和营销活动中重复使用。"

有两种方法可以创建内容模板：

* 使用左边栏从头开始创建内容模板 **[!UICONTROL 内容模板]** 菜单。 [了解如何](#create-template-from-scratch)

* 在营销活动或历程中设计电子邮件时，将电子邮件内容另存为模板。 [了解如何](#save-as-template)

保存后，您的内容模板即可在营销活动或历程中使用。 无论是从头开始创建，还是从以前的电子邮件创建，您现在都可以在生成任何 [电子邮件](get-started-email-design.md) within [!DNL Journey Optimizer]. [了解如何](email-templates.md)

>[!NOTE]
>
>* 对内容模板所做的更改不会传播到营销活动或历程，无论这些更改是实时模板还是草稿模板。
>
>* 同样，当在营销活动或历程中使用模板时，您对营销活动和历程内容所做的任何编辑都不会影响以前使用的内容模板。


### 从头开始创建模板 {#create-template-from-scratch}

要从头开始创建内容模板，请执行以下步骤。

1. 通过 **[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]** 菜单。

   ![](assets/content-template-list.png)

1. 选择 **[!UICONTROL 创建模板]**.

1. 填写模板详细信息。

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >当前仅 **电子邮件** 渠道和 **HTML** 类型受支持。

1. 要为模板分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级别访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 单击 **[!UICONTROL 创建]** 并从不同的选项中选择您设计电子邮件的方式：

   * [从头开始设计电子邮件](content-from-scratch.md) 通过Email Designer的界面。

   * [代码或复制粘贴原始HTML](code-content.md) 直接导入Email Designer。

   * [导入现有HTML内容](existing-content.md) 文件或.zip文件夹中。

   * 使用内置或自定义模板列表中的现有内容。 有关在电子邮件中使用内容模板的步骤，请参见 [此部分](email-templates.md).

   ![](assets/content-template-design.png)

1. 的 [Email Designer](get-started-email-design.md) 显示。 根据需要编辑内容，与根据您选择的选项对历程或营销策划内的任何电子邮件执行的操作相同。

   ![](assets/content-template-designer.png)

1. 您可以根据需要测试内容。 [了解如何](#test-template)

1. 模板准备就绪后，单击 **[!UICONTROL 保存]**.

1. 如果需要，单击模板名称旁边的箭头可返回到 **[!UICONTROL 详细信息]** 并编辑模板。

   ![](assets/content-template-designer-back.png)

现在，此模板已准备就绪，可用于在 [!DNL Journey Optimizer]. [了解如何](email-templates.md)

### 另存为模板 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何迁移消息"
>abstract="2022年7月25日，“消息”菜单消失，消息现在直接从历程创作。 如果要在历程中重复使用旧版消息，需要将其另存为模板。"

设计 [电子邮件](get-started-email-design.md) 在营销活动或历程中，您可以保存电子邮件内容以供将来重复使用。 为此，请执行以下步骤。

1. 在Email Designer中，单击屏幕右上方的省略号。

1. 选择 **[!UICONTROL 另存为内容模板]** 下拉菜单中。

   ![](assets/email_designer-save-template.png)

1. 为此模板添加名称和描述。

   ![](assets/email_designer-template-name.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 模板将保存到 **[!UICONTROL 内容模板]** 列表，可从 [!DNL Journey Optimizer] 专用菜单。 它将成为独立内容模板，可以作为该列表上的任何其他项目访问、编辑和删除该模板。 [了解详情](#access-manage-templates)

现在，您可以在构建任何 [电子邮件](get-started-email-design.md) within [!DNL Journey Optimizer]. [了解如何](email-templates.md)

>[!NOTE]
>
>对新模板所做的任何更改都不会传播到其发送电子邮件。 同样，在该电子邮件中编辑原始内容时，不会修改新模板。

## 测试内容模板 {#test-template}

无论是从头开始创建还是从电子邮件创建，您都可以测试任何电子邮件内容模板的呈现方式。 为此，请执行以下步骤。

>[!CAUTION]
>
>要模拟内容，您必须具有 **[!DNL Manage Simulate Content]** 包含的权限 **[!DNL Content Library Manager]** 产品配置文件。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

1. 通过 **[!UICONTROL 内容管理]** > **[!UICONTROL 内容模板]** 菜单，然后选择任意模板。

1. 单击 **[!UICONTROL 编辑内容]** 从 **[!UICONTROL 模板属性]**.

1. 单击 **[!UICONTROL 模拟内容]** 并选择测试用户档案以检查电子邮件渲染。 您可以选择桌面视图或移动设备视图。 [了解详情](preview.md)

   ![](assets/content-template-stimulate.png)

1. 您可以发送校样以测试内容，并在历程或营销策划中使用之前，先获得某些内部用户的批准。

   * 要执行此操作，请单击 **[!UICONTROL 发送校样]** 按钮，并按照 [此部分](preview.md#send-proofs).

   * 在发送校样之前，您必须选择 [电子邮件界面](../configuration/channel-surfaces.md) 用于测试内容。

      ![](assets/content-template-stimulate-proof-surface.png)

## 操作方法视频 {#video-templates}

了解如何在 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)