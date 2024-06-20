---
solution: Journey Optimizer
product: journey optimizer
title: 可自定义的片段
description: 了解如何通过使其某些字段可编辑来自定义片段。
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---


# 可自定义的片段 {#customizable-fragments}

在营销活动或历程操作中使用片段时，它们会因继承而默认被锁定。 这意味着对片段所做的任何更改都会自动传播到使用该片段的所有营销活动和历程。 利用可自定义的片段，在将片段添加到营销活动或历程操作时，片段中的特定字段可以定义为可编辑。 例如，假设您有一个带有横幅、一些文本和按钮的片段。 您可以将某些字段（如图像或按钮目标URL）指定为可编辑的。 这允许用户在将片段整合到其活动或历程中时修改这些元素，提供定制的体验而不影响原始片段。

可自定义的片段无需中断片段继承，这以前阻止将片段级别的集中更改传播到活动和历程。 这种方法允许在使用时调整内容部分，从而灵活地用特定于上下文的详细信息覆盖默认值。

利用可自定义的片段，您可以有效地管理和个性化内容，而无需创建全新的内容块或中断原始片段的继承。 这样可以确保在片段级别所做的更改仍会传播，同时允许在营销活动或历程级别进行必要的自定义。

可视片段和表达式片段均可以标记为可自定义。 有关如何继续处理每种类型片段的详细说明，请参阅以下部分。

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## 在可视片段中添加可编辑字段 {#visual}

要使可视片段的某些部分可编辑，请执行以下步骤：

>[!NOTE]
>
>可编辑的字段可添加到 **图像**， **文本** 和 **按钮** 组件。 对象 **HTML** 组件、可编辑字段是使用个性化编辑器添加的，类似于表达式片段。 [了解如何在HTML组件和表达式片段中添加可编辑字段](#expression)

1. 打开片段内容版本屏幕。

1. 选择片段中要配置可编辑字段的组件。

1. 组件属性窗格将在右侧打开。 选择 **可编辑的字段** 选项卡，然后切换 **启用版本** 选项。

1. 窗格中列出了可为选定组件编辑的所有字段。 可供编辑的字段取决于所选的组件类型。

   在以下示例中，我们允许编辑“单击此处”按钮URL。

   ![](assets/fragment-param-enable.png)

1. 单击 **概述** 以检查所有可编辑的字段及其默认值。

   在此示例中，按钮URL字段显示在组件中定义的默认值中。 在将片段添加到用户的内容后，用户可以自定义此值。

   ![](assets/fragment-param-preview.png)

1. 准备就绪后，保存更改以更新片段。

1. 将片段添加到电子邮件后，用户将能够自定义片段中配置的所有可编辑字段。 [了解如何自定义可视化片段中的可编辑字段](../email/use-visual-fragments.md#customize-fields)

## 在HTML组件和表达式片段中添加可编辑字段 {#expression}

要使HTML组件或表达式片段的某些部分可编辑，必须在表达式编辑器中使用特定语法。 这涉及声明 **变量** 带默认值，用户在将片段添加到其内容后可以覆盖该值。

例如，假设您要创建一个片段以添加到您的电子邮件中，并允许用户自定义在不同位置使用的特定颜色，如框架或按钮的背景颜色。 创建片段时，需要使用声明变量 **唯一标识符**，例如“颜色”，并在片段内容中要应用此颜色的所需位置调用它。 将片段添加到其内容时，用户将能够自定义在任何引用变量的位置使用的颜色。

对于HTML组件，只有特定元素才能变为可编辑字段。 展开以下部分以获取更多信息。

+++HTML组件中的可编辑元素：

以下元素可以成为HTML组件中的可编辑字段：

* 文本的一部分
* 链接或图像的完整URL（不适用于URL的一部分）
* 整个CSS属性（不适用于部分属性）

例如，在下面的代码中，每个以红色高亮显示的元素都可以成为属性：

![](assets/fragment-html.png){width=&quot;70%}

+++

要声明变量并在片段中使用它，请执行以下步骤：

1. 打开表达式片段，然后在个性化编辑器中编辑其内容。 对于HTML组件，选择片段中的组件并单击 **显示源代码** 按钮。

   ![](assets/fragment-html-edit.png)

1. 声明用户要编辑的变量。 导航至 **辅助函数** 菜单并添加 **内嵌** 辅助函数。 用于声明和调用变量的语法会自动添加到内容中。

   ![](assets/fragment-add-helper.png)

1. 替换 `"name"` 具有标识可编辑字段的唯一ID。

   >[!NOTE]
   >
   >字段ID必须是唯一的，且不能包含空格。 此ID应在您的内容中要显示变量值的任意位置使用。

1. 通过添加下表中详述的参数来调整语法以符合您的需求：

   | 操作 | 参数 | 示例 |
   | ------- | ------- | ------- |
   | 声明可编辑的字段 **默认值**. 将片段添加到内容时，如果您不自定义片段，则将使用此默认值。 | 在内联标记之间添加默认值。 | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | 定义 **标签** 用于可编辑字段。 编辑片段的字段时，此标签将显示在电子邮件Designer中。 | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | 声明包含下列内容的可编辑字段 **Image source** 需要发布的文档。 | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | 声明包含下列内容的可编辑字段 **URL** 需要跟踪的。<br/>请注意，现成的“镜像页面URL”和“取消订阅链接”预定义块不能成为可编辑的字段。 | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. 使用 `{{{name}}}` 代码中要显示可编辑字段值的每个位置的语法。 替换 `name` 使用之前定义的字段的唯一ID。

   ![](assets/fragment-call-variable.png)

1. 保存您的片段。

在将片段添加到其电子邮件内容时，用户现在可以使用所选值覆盖变量的默认值：

* 对于表达式片段，使用特定语法覆盖变量值。 [了解如何自定义表达式片段中的可编辑字段](../personalization/use-expression-fragments.md#customize-fields)

* 对于HTML组件，变量显示在电子邮件Designer的可编辑字段列表中。 [了解如何自定义可视化片段中的可编辑字段](../email/use-visual-fragments.md#customize-fields)

## 可编辑的表达式片段示例 {#example}

在以下示例中，我们正在创建一个展示新体育收藏集的表达式片段。 默认情况下，片段会显示以下内容： *正在查找更多内容？ 不要错过我们最新的运动系列！*

我们希望允许用户将本内容中的“sports”替换为他们选择的运动。 例如： *正在查找更多内容？ 不要错过我们最新的瑜伽系列！*

为实现此操作，请执行以下步骤：

1. 声明“sport”变量，并将ID设置为“sport”。

   默认情况下，如果用户在其内容中添加片段后未更改变量的值，则会显示 `{{#inline}}` 和 `{{/inline}}` 标记，即“体育”。

1. 添加 ``{{{sport}}}`` 片段内容中要显示变量值的语法，即“sports”（默认）或用户选择的值。

   ![](assets/fragment-expression-custom.png)

1. 将表达式片段添加到其内容时，用户可以直接从表达式编辑器中使用所做的选择更改变量的值。 [了解如何自定义表达式片段中的可编辑字段](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
