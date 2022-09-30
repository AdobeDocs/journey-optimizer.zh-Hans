---
title: 创建动态内容
description: 了解如何在消息中添加动态消息。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---


# 创建动态内容 {#dynamic-content}

Adobe Journey Optimizer允许您利用库中创建的条件规则，将动态内容添加到消息中。

动态内容可以创建到任何字段中，您可以在其中使用表达式编辑器添加个性化。 这包括主题行、链接、推送通知内容或文本类型选件的表示形式。 [了解有关个性化上下文的更多信息](personalization-contexts.md)

此外，您还可以在Email Designer中使用条件规则创建内容组件的多个变体。

## 将动态内容添加到表达式中 {#perso-expressions}

在表达式中添加动态内容的步骤如下所示：

1. 导航到要添加动态内容的字段，然后打开表达式编辑器。

1. 选择 **[!UICONTROL 条件]** 菜单来显示可用条件规则列表。 单击规则旁边的+按钮以将其添加到当前表达式中。

   您还可以通过选择 **[!UICONTROL 新建]**. [了解如何创建条件](create-conditions.md)

   ![](assets/conditions-expression.png)

1. 在 `{%if}` 和 `{%/if}` 标记满足条件规则时要显示的内容。 您可以根据需要添加任意数量的规则，以创建表达式的多个变体。

   在以下示例中，根据收件人的首选语言，为短信内容创建了两个变体。

   ![](assets/conditions-language-sample.png)

1. 内容准备就绪后，您可以使用 **[!UICONTROL 模拟内容]** 按钮。 [了解如何测试和预览消息](../design/preview.md)

   ![](assets/conditions-preview.png)

## 将动态内容添加到电子邮件中 {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="条件内容"
>abstract="使用条件规则为内容组件创建多个变体。 如果发送消息时不满足任何条件，则将显示“默认”变体中的内容。"

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="条件内容"
>abstract="使用保存到库中的条件规则或创建新规则。"

在Email Designer中创建内容组件变体的步骤如下所示：

1. 在Email Designer中，选择一个内容组件，然后单击 **[!UICONTROL 启用条件内容]**.

   ![](assets/conditions-enable-conditional.png)

1. 的 **[!UICONTROL 条件内容]** 窗格。 在此窗格中，您可以使用条件创建选定内容组件的多个变体。

   通过选择 **[!UICONTROL 应用条件]** 按钮。

   ![](assets/conditions-apply.png)

1. 将显示条件库。 选择要与变体关联的条件规则，然后单击 **[!UICONTROL 选择]**. 在本例中，我们希望根据收件人的首选语言来调整组件文本。

   ![](assets/conditions-select.png)

   您还可以通过单击 **[!UICONTROL 新建]**. [了解如何创建条件](create-conditions.md)

1. 条件规则与变体关联。 为了更好的可读性，我们建议通过单击椭圆菜单来重命名变体。

   现在，配置在发送消息时如果满足规则，则组件应显示的方式。 在本例中，我们希望以法语显示收件人的首选语言文本。

   ![](assets/conditions-design.png)

1. 根据需要为内容组件添加任意数量的变体。 您可以随时在不同的变体之间切换，以根据条件规则检查内容组件的显示方式。

   >[!NOTE]
   >如果在发送消息时不满足变体中定义的任何规则，则内容组件将显示 **[!UICONTROL 默认变体]**.
   >
   >将根据关联的规则评估条件内容，并按变体的显示顺序排列。 如果不满足其他条件，则始终显示默认变体。
