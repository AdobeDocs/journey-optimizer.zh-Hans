---
title: 在Journey Optimizer中设计电子邮件
description: 了解如何设计电子邮件内容
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 0%

---

# 在用户界面{#create-email-content}中设计您的电子邮件内容

![](assets/do-not-localize/badge.png)

创建[消息](create-message.md)后，即可开始创建电子邮件内容。

1. 从新创建的消息中，选择&#x200B;**[!UICONTROL Edit content]**&#x200B;部分中的&#x200B;**[!UICONTROL Email designer]**。

   ![](assets/import-html_1.png)

1. 在“电子邮件设计器”主页中，从以下选项中选择您如何设计电子邮件：

   * 选择&#x200B;**[!UICONTROL Design from scratch]**&#x200B;以使用电子邮件设计器功能创建您的电子邮件内容。

   * 选择&#x200B;**[!UICONTROL Start from template]**&#x200B;以通过内置模板列表创建电子邮件。 请注意，您无法创建其他模板。

   * 选择&#x200B;**[!UICONTROL Code your own]**&#x200B;以输入或粘贴HTML原始代码。 [了解详情](existing-content.md#import-raw-html-code)。

   * 选择&#x200B;**[!UICONTROL Import HTML]**&#x200B;以导入HTML文件或.zip文件夹。 [了解详情](existing-content.md#import-html-content-from-file)。

   ![](assets/email_designer_25.png)

## 从头开始设计

要开始与电子邮件设计人员一起构建电子邮件内容，请执行以下步骤：

1. 选择&#x200B;**[!UICONTROL Design from scratch]**&#x200B;选项后，通过拖放&#x200B;**[!UICONTROL Structure components]**&#x200B;定义电子邮件布局，开始设计电子邮件内容。

   ![](assets/email_designer_2.png)

1. 从&#x200B;**[!UICONTROL Content components]**&#x200B;下拉列表中，您可以在结构组件中添加所需数量的&#x200B;**[!UICONTROL Content components]**。 [了解有关内容组件的更多信息](content-components.md)。

   ![](assets/email_designer_3.png)

1. 每个组件都可进一步使用&#x200B;**[!UICONTROL Component settings]**&#x200B;部分进行自定义。 例如，您可以更改文本样式、组件的边距或边距。 [进一步了解电子邮件编辑器中的样式](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/styles.html)。

   ![](assets/email_designer_4.png)

1. 在&#x200B;**[!UICONTROL Assets picker]**&#x200B;中，您可以直接将存储在&#x200B;**[!UICONTROL Assets library]**&#x200B;中的资产添加到您的电子邮件中。 [了解有关资产管理的更多信息](assets-essentials.md)。

   多次单击包含您的资产的文件夹，然后拖放要添加到电子邮件中的资产。

   ![](assets/email_designer_5.png)

1. 添加个性化字段以自定义来自用户档案数据的内容。 [了解有关内容个性化的更多信息](personalization/personalize.md)。

   ![](assets/email_designer_6.png)

1. 在左窗格的&#x200B;**[!UICONTROL Links]**&#x200B;选项卡中，检查要跟踪的内容的所有URL的列表。 如果需要，您可以修改其&#x200B;**[!UICONTROL Tracking Type]**、**[!UICONTROL Label]**&#x200B;和&#x200B;**[!UICONTROL Tags]**。

   ![](assets/email_designer_7.png)

1. 如果需要，您可以切换到代码编辑器，通过单击高级菜单中的&#x200B;**[!UICONTROL Switch to code editor]**&#x200B;进一步个性化您的电子邮件。 有关代码编辑器的详细信息，请参阅此[页面](existing-content.md#import-raw-html-code)。

   >[!NOTE]
   >
   >切换到代码编辑器后，您将无法使用此电子邮件的可视设计器。

   ![](assets/email_designer_26.png)

1. 单击&#x200B;**[!UICONTROL Preview]**&#x200B;检查电子邮件呈现。 您可以选择桌面或移动视图。

   ![](assets/email_designer_8.png)

1. 当您的电子邮件准备就绪时，单击&#x200B;**[!UICONTROL Save & Close]**。

您的电子邮件内容现在可用于邮件。 [了解如何发送消息](publish-manage-message.md)。

## 定义电子邮件结构{#defining-the-email-structure}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="关于结构组件"
>abstract="结构组件定义电子邮件的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="定义电子邮件列"
>abstract="电子邮件设计器允许您通过定义列结构轻松定义电子邮件的布局。"

电子邮件设计器使您能够轻松定义电子邮件的结构。 通过使用简单的拖放操作添加和移动结构元素，您可以在几秒钟内设计电子邮件的形状。

要编辑电子邮件的结构，请执行以下操作：

1. 打开现有内容或创建新的电子邮件内容。
1. 通过选择左侧的&#x200B;**+**&#x200B;图标访问&#x200B;**[!UICONTROL Structure components]**。
1. 拖放您需要塑造电子邮件结构的结构组件。
在放置结构组件之前，蓝线将实现其确切位置。 您可以将其放在任何其他组件之上、之间或之下，但不能放在内部。

   >[!NOTE]
   >
   >请注意，列堆并非与所有电子邮件项目兼容。 不支持时，不会堆叠列。
   >
   >一旦放入电子邮件中，您便无法移动或删除您的组件，除非其中已经放置了内容组件或片段。

1. 有多个由一个或多个列组成的结构组件可用。

   选择&#x200B;**[!UICONTROL n:n column]**&#x200B;组件以定义所选列数（3到10列）。 您还可以通过移动每列底部的箭头来定义每列的宽度。

   >[!NOTE]
   >
   >每个列大小不能低于结构组件总宽度的10%。 无法删除非空列。

定义结构后，您便可以向电子邮件中添加内容片段和组件。

## 使用前标{#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="使用预头"
>abstract="通过该标题，您可以配置一个简短的摘要文本，以帮助您更好地跟踪和自定义您的电子邮件。"

标题是简短的摘要文本，在从电子邮件客户端查看电子邮件时，该文本会跟随主题行。 该标题可帮助您更好地跟踪和自定义您的电子邮件。

选择&#x200B;**[!UICONTROL Preheader]**&#x200B;编辑框并添加内容。

您可以在前标内容中添加&#x200B;**[!UICONTROL Content block]**、**[!UICONTROL Dynamic content]**&#x200B;或&#x200B;**[!UICONTROL Personalization fields]**。

>[!NOTE]
>
>请注意，前标题与所有电子邮件客户端不兼容。 如果不支持，则不显示该预头。

## 背景设置{#about-backgrounds}

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="背景设置"
>abstract="电子邮件设计器可让您个性化内容的背景颜色或背景图像。请注意，并非所有电子邮件客户都支持背景图像。"
>additional-url="https://docs.google.com/spreadsheets/d/1TLo62YKm3tThUWDOIliCQFWs3dpNjpDfw6DdTr1oGOw/edit#gid=0" text="其他信息"

在使用电子邮件设计器设置背景时，Adobe建议：

1. 根据您的设计需要，将背景色应用于电子邮件正文。
1. 在大多数情况下，在列级设置背景颜色。
1. 请尽量不要在图像或文本组件上使用背景颜色，因为它们难以管理。

以下是您可以使用的可用背景设置。

* 为整个电子邮件设置&#x200B;**[!UICONTROL Background color]**。 确保在可从左侧调色板访问的导航树中选择正文设置。

* 通过选择&#x200B;**[!UICONTROL Viewport background color]**&#x200B;为所有结构组件设置相同的背景颜色。 此选项允许您从背景颜色中选择其他设置。

* 为每个结构组件设置不同的背景颜色。 在可从左侧调色板访问的导航树中选择一个结构，以仅将特定背景颜色应用于该结构。

   请确保未设置视口背景颜色，因为它可能隐藏结构背景颜色。

* 为结构组件的内容设置&#x200B;**[!UICONTROL Background image]**。

   >[!NOTE]
   >
   >某些电子邮件项目不支持背景图像。 不支持时，将改用行背景颜色。 确保在无法显示图像时选择适当的回退背景颜色。

* 在列级设置背景颜色。

   >[!NOTE]
   >
   >这是最常见的用例。 Adobe建议在列级别设置背景颜色，因为这样在编辑整个电子邮件内容时就更具灵活性。

   您也可以在列级别设置背景图像，但很少使用此设置。

### 示例：调整垂直对齐和填充{#example--adjusting-vertical-alignment-and-padding}

要调整由三列组成的结构组件中的填充和垂直对齐方式。 为此，请按照以下步骤操作：

1. 直接在电子邮件中或使用左侧&#x200B;**调板**&#x200B;中提供的结构树选择结构组件。
1. 在&#x200B;**上下文工具栏**&#x200B;中，单击&#x200B;**[!UICONTROL Select a column]**&#x200B;并选择要编辑的工具栏。 也可以从结构树中选择它。

   该列的可编辑参数显示在右侧的&#x200B;**[!UICONTROL Settings]**&#x200B;窗格中。

1. 在&#x200B;**[!UICONTROL Vertical alignment]**&#x200B;下，选择&#x200B;**[!UICONTROL Up]**。

   内容组件显示在列的顶部。

1. 在&#x200B;**[!UICONTROL Padding]**&#x200B;下，定义列内的顶部填充。 单击锁定图标可中断与底部填充的同步。

   定义该列的左边距和右边距。

1. 以同样方式继续调整其他列的对齐和填充。

1. 保存更改。

## 为链接{#about-styling-links}定义样式

您可以为链接添加下划线，并在“电子邮件设计器”中选择其颜色和目标。

1. 在插入链接的组件中，选择链接的标签文本。

1. 在组件设置中，选中&#x200B;**[!UICONTROL Underline link]**&#x200B;可为链接的标签文本添加下划线。

1. 要选择在哪个浏览上下文中打开您的链接，请选择&#x200B;**[!UICONTROL Target]**。

1. 要更改链接的颜色，请单击&#x200B;**[!UICONTROL Link color]**。

1. 选择所需的颜色。

1. 保存更改。

## 添加行中样式属性{#adding-inline-styling-attributes}

在“电子邮件设计器”界面中，当您选择某个元素并在侧面板中显示其设置时，您可以自定义该特定元素的内联属性及其值。

1. 选择内容中的元素。
1. 在侧面板上，查找&#x200B;**[!UICONTROL Styles Inline]**&#x200B;设置。

1. 修改现有属性的值，或使用&#x200B;**+**&#x200B;按钮添加新属性。 您可以添加任何符合CSS的属性和值。

样式随后将应用于所选元素。 如果子元素没有定义特定的样式属性，则继承父元素的样式。


## 创建电子邮件{#generate-text-version}的文本版本

建议创建电子邮件正文的文本版本，当无法显示HTML内容时使用。

默认情况下，电子邮件设计器会创建&#x200B;**[!UICONTROL Plain text]**&#x200B;版本的电子邮件，包括个性化字段。 此版本会自动生成并与您的内容的HTML版本同步。

如果您希望对纯文本版本使用其他内容，请按照以下步骤操作：

1. 在您的电子邮件中，选择&#x200B;**[!UICONTROL Plain text]**&#x200B;选项卡。

1. 使用&#x200B;**[!UICONTROL Sync with HTML]**&#x200B;切换键可禁用同步。

   ![](assets/text_version_1.png)

1. 单击复选标记以确认您的选择。

   ![](assets/text_version_2.png)

1. 然后，您可以根据需要编辑纯文本版本。

>[!CAUTION]
>
>* 在&#x200B;**[!UICONTROL Plain text]**&#x200B;视图中所做的更改不会反映在HTML视图中。
   >
   >
* 如果在更新纯文本内容后重新启用&#x200B;**[!UICONTROL Sync with HTML]**&#x200B;选项，则更改将丢失，并替换为从HTML版本生成的文本内容。

>


