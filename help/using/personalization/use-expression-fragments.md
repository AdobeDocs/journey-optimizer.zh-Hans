---
solution: Journey Optimizer
product: journey optimizer
title: 使用表达式片段
description: 了解如何在 [!DNL Journey Optimizer] 个性化编辑器中使用表达式片段。
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式、编辑器、库、个性化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 24baaa2438c6bbdddd582c71dbdd36188d12f905
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# 利用表达式片段 {#use-expression-fragments}

使用&#x200B;**个性化编辑器**&#x200B;时，您可以利用已创建或已保存到当前沙盒中的所有表达式片段。

片段是可重复使用的组件，可以在[!DNL Journey Optimizer]营销活动和历程中引用。 此功能允许预先构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合内容。 [了解有关片段的更多信息](../content-management/fragments.md)

➡️ [在此视频中了解如何管理、创作和使用片段](../content-management/fragments.md#video-fragments)

## 使用表达式片段 {#use-expression-fragment}

要向内容添加表达式片段，请执行以下步骤。

>[!NOTE]
>
>您最多可以在给定投放中添加30个片段。 片段最多只能嵌套1级。

1. 打开[个性化编辑器](personalization-build-expressions.md)，然后在左窗格中选择&#x200B;**[!UICONTROL 片段]**&#x200B;按钮。

   该列表显示了当前沙盒上已创建或另存为片段的所有表达式片段。 [了解如何创建片段](../content-management/create-fragments.md)
它们按创建日期排序：最近添加的表达式片段首先显示在列表中。

   ![](assets/expression-fragments-pane.png)

   您也可以刷新此列表。

   >[!NOTE]
   >
   >如果在编辑内容时修改或添加了某些片段，则列表将使用最新更改进行更新。

1. 单击表达式片段旁边的+图标以将相应的片段ID插入到编辑器中。

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >您可以将任何&#x200B;**草稿**&#x200B;或&#x200B;**实时**&#x200B;片段添加到您的内容中。 但是，如果历程或营销活动中正在使用&#x200B;**草稿**&#x200B;状态的片段，您将无法激活该历程或营销活动。 在历程或营销活动发布中，草稿片段将显示错误，您需要批准它们才能发布。

1. 添加片段ID后，如果您打开相应的表达式片段并从界面中[编辑它](../content-management/manage-fragments.md#edit-fragments)，则将同步更改。 它们会自动传播到包含该片段ID的所有草稿或实时历程/营销活动。

1. 单击片段旁边的&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮。 从打开的上下文菜单中，选择&#x200B;**[!UICONTROL 查看片段]**&#x200B;以获取有关该片段的更多信息。 还显示&#x200B;**[!UICONTROL 片段ID]**，可从此处复制。

   ![](assets/expression-fragment-view.png)

1. 您可以在另一个窗口中打开表达式片段以编辑其内容和属性 — 使用上下文菜单中的&#x200B;**[!UICONTROL 打开片段]**&#x200B;选项或从&#x200B;**[!UICONTROL 片段信息]**&#x200B;窗格中编辑。 [了解如何编辑片段](../content-management/manage-fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 然后，您可以使用[个性化编辑器](personalization-build-expressions.md)的所有个性化和创作功能，像往常一样自定义和验证内容。

1. 在某些情况下，您只需要计算变量，因此您可能希望隐藏表达式片段的内容。 为此，请使用`render`属性并将其设置为`false`。 例如：

   ```
   Hi {{profile.person.name.firstName|fragment id='ajo:fragmentId/variantId' mode ='inline' render=false}}
   ```

>[!NOTE]
>
>如果您创建的表达式片段包含多个换行符，并在[短信](../sms/create-sms.md#sms-content)或[推送](../push/design-push.md)内容中使用它，则将保留换行符。 因此，请确保在发送您的[短信](../sms/send-sms.md)或[推送](../push/send-push.md)消息之前对其进行测试。

## 使用隐式变量 {#implicit-variables}

隐式变量增强了现有片段功能，以提高内容重用和脚本用例的效率。 片段可以使用输入变量并创建可在营销活动和历程内容中使用的输出变量。

例如，此功能可用于根据当前营销活动或历程初始化电子邮件的跟踪参数，并将这些参数用于添加到电子邮件内容的个性化链接。

可以使用以下用例：

1. **在片段中使用输入变量。**

   当在营销活动/历程操作内容中使用片段时，它能够在片段之外利用声明的变量。 示例如下：

   ![](../personalization/assets/variable-in-a-fragment.png)

   我们可以看到，以上在营销活动内容中声明了`utm_content`变量。 当使用片段&#x200B;**主页块**&#x200B;时，将显示一个链接，其中将附加`utm_content`参数值。 最终结果为： `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`。

1. **使用片段中的输出变量。**

   在片段中计算或定义的变量可在您的内容中使用。 在以下示例中，片段&#x200B;**F1**&#x200B;声明了一组变量：

   ![](../personalization/assets/personalize-with-variables.png)

   在电子邮件内容中，您可以进行以下个性化设置：

   ![](../personalization/assets/use-fragment-variable.png)

   片段F1初始化以下变量： `utm_campaign`和`utm_content`。 然后，消息内容中的链接将会附加这些参数。 最终结果为： `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`。

>[!NOTE]
>
>在运行时，系统会扩展片段中的内容，然后从上到下解释个性化代码。 请记住，可以实现更复杂的用例。 例如，您可以有一个片段F1将变量传递给位于下方的另一个片段F2。 您还可以让可视片段F1将变量传递给嵌套表达式片段F2。


## 自定义可编辑字段 {#customize-fields}

如果表达式片段的某些部分已使用变量设置为可编辑，则可以使用特定语法覆盖其默认值。 [了解如何使您的片段可自定义](../content-management/customizable-fragments.md)

要自定义字段，请执行以下步骤：

1. 从&#x200B;**[!UICONTROL 片段]**&#x200B;菜单将片段插入到您的代码中。

1. 在语法末尾使用`<fieldId>="<value>"`代码覆盖变量的默认值。

   在以下示例中，我们将ID为“sports”的变量的值替换为“yoga”值。 只要引用“sport”变量，这就会在片段内容中显示“瑜伽”。

   ![](../content-management/assets/fragment-expression-use.png)

[此部分](../content-management/customizable-fragments.md#example)中提供了示例，说明如何在创建电子邮件时将可编辑字段添加到表达式片段并覆盖其值。

## 中断继承 {#break-inheritance}

向个性化编辑器添加片段ID时，将同步对原始表达式片段所做的更改。

但是，您也可以将表达式片段的内容粘贴到编辑器中。 从上下文菜单中，选择&#x200B;**[!UICONTROL 粘贴片段]**&#x200B;以插入该内容。

![](assets/expression-fragment-paste.png)

在这种情况下，来自原始片段的继承将被中断。 片段的内容将会复制到编辑器中，并且更改不再同步。

它会变成一个不再链接到原始片段的独立元素；您可以像代码中的任何其他元素一样编辑它。

