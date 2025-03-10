---
solution: Journey Optimizer
product: journey optimizer
title: 创建动态内容
description: 了解如何将动态添加到消息中。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，动态，内容
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 10%

---

# 创建动态内容 {#dynamic-content}

Adobe Journey Optimizer允许您利用在库中创建的条件规则，将动态内容添加到消息中。

动态内容可以创建到任何字段中，您可以使用个性化编辑器添加个性化。 这包括主题行、链接、推送通知内容或文本类型优惠的表示法。 [了解有关个性化的更多信息](personalize.md)

此外，您可以在Email Designer中使用条件规则来创建内容组件的多个变体。

## 将动态内容添加到表达式中 {#perso-expressions}

在表达式中添加动态内容的步骤如下：

1. 导航到要添加动态内容的字段，然后打开个性化编辑器。

1. 选择&#x200B;**[!UICONTROL 条件]**&#x200B;菜单以显示可用的条件规则列表。 单击规则旁边的+按钮可将其添加到当前表达式中。

   您还可以通过选择&#x200B;**[!UICONTROL 新建]**&#x200B;来创建新规则。 [了解如何创建条件](create-conditions.md)

   ![](assets/conditions-expression.png)

1. 在`{%if}`和`{%/if}`标记之间添加您要在满足条件规则时显示的内容。 您可以根据需要添加任意数量的规则，以创建表达式的多个变体。

   在下面的示例中，根据收件人的首选语言，为SMS内容创建了两个变体。

   ![](assets/conditions-language-sample.png)

1. 内容准备就绪后，您可以使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮预览不同的变体。 [了解如何测试和预览邮件](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

## 将动态内容添加到电子邮件中 {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="条件内容"
>abstract="使用条件规则创建内容组件的多个变体。如果在发送消息时不满足任何条件，则将显示默认变体中的内容。"

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="条件内容"
>abstract="使用保存在库中的条件规则或创建新规则。"

在Email Designer中创建内容组件的变体的步骤如下所示：

1. 在[电子邮件Designer](../email/content-from-scratch.md)中，选择一个内容组件，然后单击&#x200B;**[!UICONTROL 启用条件内容]**。

   ![](assets/conditions-enable-conditional.png)

1. **[!UICONTROL 条件内容]**&#x200B;窗格显示在左侧。 在此窗格中，您可以使用条件创建所选内容组件的多个变体。

   通过选择&#x200B;**[!UICONTROL 选择条件]**&#x200B;按钮配置您的第一个变体。

   ![](assets/conditions-apply.png)

1. 条件库随即显示。 选择要与变体关联的条件规则，然后单击&#x200B;**[!UICONTROL 选择]**。 在本例中，我们希望根据收件人的首选语言调整组件文本。

   ![](assets/conditions-select.png)

   您也可以通过单击&#x200B;**[!UICONTROL 新建]**&#x200B;来创建新规则。 [了解如何创建条件](create-conditions.md)

1. 条件规则已关联到变体。 为了提高可读性，请从“更多操作”图标中选择&#x200B;**[!UICONTROL 重命名]**&#x200B;操作以重命名变体。

   ![](assets/conditions-rename.png)

1. 配置在发送消息时如果满足规则应如何显示组件。 在本例中，我们希望以法文显示文本（如果它是收件人的首选语言）。

   ![](assets/conditions-design.png)

1. 根据内容组件的需要，添加任意数量的变体。 您可以随时在不同的变体之间切换，以检查内容组件将如何根据条件规则显示。

   >[!NOTE]
   >如果发送消息时未满足变体中定义的任何规则，则内容组件将显示&#x200B;**[!UICONTROL 默认变体]**&#x200B;中定义的内容。
   >
   >条件内容将按照变体的显示顺序根据关联的规则进行评估。 如果不满足其他条件，则始终显示默认变体。

1. 要删除变体，请单击所需变体旁边的“更多操作”图标，然后选择&#x200B;**[!UICONTROL 删除]**。

   ![](assets/conditions-delete.png)
