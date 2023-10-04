---
solution: Journey Optimizer
product: journey optimizer
title: 使用表达式片段
description: 了解如何在中使用表达式片段 [!DNL Journey Optimizer] 表达式编辑器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式、编辑器、库、个性化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 4d74588b5df0afab7e56e540703891c48a94ab5f
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# 利用表达式片段 {#use-expression-fragments}

使用表达式编辑器时，您可以利用已创建或已保存到当前沙盒的所有表达式片段。

了解如何在中创建和管理片段 [本节](../content-management/fragments.md).

➡️ [在此视频中了解如何管理、创作和使用片段](../content-management/fragments.md#video-fragments)

## 使用表达式片段 {#use-expression-fragment}

要向内容添加表达式片段，请执行以下步骤。

1. 打开 [表达式编辑器](personalization-build-expressions.md) 并选择 **[!UICONTROL 片段]** 按钮。

   ![](assets/expression-fragments-pane.png)

   该列表显示了当前沙盒上已创建或另存为片段的所有表达式片段。 [了解详情](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >片段按创建日期排序：最近添加的表达式片段首先显示在列表中。

1. 您还可以刷新列表。

   >[!NOTE]
   >
   >如果在编辑内容时修改或添加了某些片段，则列表将使用最新更改进行更新。

1. 单击表达式片段旁边的+图标以将相应的片段ID插入到编辑器中。

   ![](assets/expression-fragment-add.png)

   添加片段ID后，如果您打开相应的表达式片段并 [编辑它](../content-management/fragments.md#edit-fragments) 从界面中，同步更改。 它们会自动传播到所有 **[!UICONTROL 草稿]** 包含该片段ID的历程/营销活动。

   >[!NOTE]
   >
   >更改不会传播到中使用的内容。 **[!UICONTROL 实时]** 历程或营销活动。

1. 单击 **[!UICONTROL 更多操作]** 按钮创建片段。

1. 从打开的上下文菜单中，选择 **[!UICONTROL 查看片段]** 以获取有关该片段的更多信息。 此 **[!UICONTROL 片段ID]** 也会显示，并且可以从此处复制。

   ![](assets/expression-fragment-view.png)

1. 您可以在另一个窗口中打开表达式片段以编辑其内容和属性 — 使用 **[!UICONTROL 打开片段]** 选项，或者从 **[!UICONTROL 片段信息]** 窗格。 [了解如何编辑片段](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 然后，您可以像往常一样使用的所有个性化和创作功能自定义和验证内容。 [表达式编辑器](personalization-build-expressions.md).

>[!NOTE]
>
>如果您创建的表达式片段包含多个换行符并将其用于 [短信](usi..ng/sms/create-sms.md#sms-content) 或 [推送](../push/design-push.md) 内容，将保留换行符。 因此，请确保预览并测试 [短信](../sms/send-sms.md) 或 [推送](../push/send-push.md) 发送之前发送的消息。

## 中断继承 {#break-inheritance}

向表达式编辑器添加片段ID时，将同步对原始表达式片段所做的更改。

但是，您也可以将表达式片段的内容粘贴到编辑器中。 从上下文菜单中，选择 **[!UICONTROL 粘贴片段]** 以插入该内容。

![](assets/expression-fragment-paste.png)

在这种情况下，来自原始片段的继承将被中断。 片段的内容将会复制到编辑器中，并且更改不再同步。

它会变成一个不再链接到原始片段的独立元素；您可以像代码中的任何其他元素一样编辑它。

