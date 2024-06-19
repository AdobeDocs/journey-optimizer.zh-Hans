---
solution: Journey Optimizer
product: journey optimizer
title: 使用表达式片段
description: 了解如何在中使用表达式片段 [!DNL Journey Optimizer] 个性化编辑器。
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式、编辑器、库、个性化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# 利用表达式片段 {#use-expression-fragments}

使用时 **个性化编辑器**，您可以利用已创建或已保存到当前沙盒的所有表达式片段。

片段是可重复使用的组件，可通过以下方式引用 [!DNL Journey Optimizer] 营销活动和历程。 此功能允许预先构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合内容。 [了解如何创建和管理片段](../content-management/fragments.md).

➡️ [在此视频中了解如何管理、创作和使用片段](../content-management/fragments.md#video-fragments)

## 使用表达式片段 {#use-expression-fragment}

要向内容添加表达式片段，请执行以下步骤。

>[!NOTE]
>
>您最多可以在给定投放中添加30个片段。 片段最多只能嵌套1级。

1. 打开 [个性化编辑器](personalization-build-expressions.md) 并选择 **[!UICONTROL 片段]** 按钮。

   该列表显示了当前沙盒上已创建或另存为片段的所有表达式片段。 它们按创建日期排序：最近添加的表达式片段首先显示在列表中。 [了解详情](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   您也可以刷新此列表。

   >[!NOTE]
   >
   >如果在编辑内容时修改或添加了某些片段，则列表将使用最新更改进行更新。

1. 单击表达式片段旁边的+图标以将相应的片段ID插入到编辑器中。

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >您可以添加任何 **草稿** 或 **实时** 片段到您的内容。 但是，如果历程或营销活动中正在使用具有草稿状态的片段，您将无法激活该历程或营销活动。 在历程或营销活动发布中，草稿片段将显示错误，您需要批准它们才能发布。
   >
   > 请注意，片段状态在Journey Optimizer 6月发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，请注意，片段不需要 **实时** 将在您的历程和营销活动中使用。

1. 添加片段ID后，如果您打开相应的表达式片段并 [编辑它](../content-management/fragments.md#edit-fragments) 从界面中，同步更改。 它们会自动传播到包含该片段ID的所有草稿或实时历程/营销活动。

1. 单击 **[!UICONTROL 更多操作]** 按钮创建片段。 从打开的上下文菜单中，选择 **[!UICONTROL 查看片段]** 以获取有关该片段的更多信息。 此 **[!UICONTROL 片段ID]** 也会显示，并且可以从此处复制。

   ![](assets/expression-fragment-view.png)

1. 您可以在另一个窗口中打开表达式片段以编辑其内容和属性 — 使用 **[!UICONTROL 打开片段]** 选项，或者从 **[!UICONTROL 片段信息]** 窗格。 [了解如何编辑片段](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 然后，您可以像往常一样使用的所有个性化和创作功能自定义和验证内容。 [个性化编辑器](personalization-build-expressions.md).

>[!NOTE]
>
>如果您创建的表达式片段包含多个换行符并将其用于 [短信](../sms/create-sms.md#sms-content) 或 [推送](../push/design-push.md) 内容，将保留换行符。 因此，请务必测试 [短信](../sms/send-sms.md) 或 [推送](../push/send-push.md) 发送之前发送的消息。

## 中断继承 {#break-inheritance}

向个性化编辑器添加片段ID时，将同步对原始表达式片段所做的更改。

但是，您也可以将表达式片段的内容粘贴到编辑器中。 从上下文菜单中，选择 **[!UICONTROL 粘贴片段]** 以插入该内容。

![](assets/expression-fragment-paste.png)

在这种情况下，来自原始片段的继承将被中断。 片段的内容将会复制到编辑器中，并且更改不再同步。

它会变成一个不再链接到原始片段的独立元素；您可以像代码中的任何其他元素一样编辑它。

