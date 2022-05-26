---
title: 定义登陆页面特定的内容
description: 了解如何在Journey Optimizer中设计登陆页面特定内容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---

# 定义登陆页面特定的内容 {#lp-content}

要定义允许用户从登陆页面选择和提交其选择的特定内容，请使用 **[!UICONTROL Form]** 组件。 为此，请执行以下步骤。

>[!NOTE]
>
>您还可以创建点进登陆页面，但不 **[!UICONTROL Form]** 组件。 在这种情况下，将向用户显示登陆页面，但用户无需提交任何表单。 如果您只想显示登陆页面而无需收件人执行任何操作（如选择启用或选择禁用），或者希望提供不需要用户输入的信息，则此功能非常有用。

## 使用表单组件 {#use-form-component}

1. 拖放特定于登陆页面的 **[!UICONTROL Form]** 组件从左侧面板移入主工作区。

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Form]** 组件在同一页面上只能使用一次。

1. 选择模式。的 **[!UICONTROL Form content]** 选项卡，以编辑表单的不同字段。

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >切换到 **[!UICONTROL Form style]** 选项卡，以编辑表单组件内容的样式。 [了解详情](#define-lp-styles)

1. 从 **[!UICONTROL Checkbox 1]** 部分，则可以编辑与此复选框对应的标签。

1. 定义此复选框是否用于选择用户启用或禁用：他们是否同意接收通信或要求不再联系？

   ![](assets/lp_designer-form-update.png)

   从以下三个选项中进行选择：

   * **[!UICONTROL Opt in if checked]**:用户需要选中要同意（选择加入）的框。
   * **[!UICONTROL Opt out if checked]**:用户需要选中相应复选框以删除其同意（选择退出）。
   * **[!UICONTROL Opt in if checked, opt out if unchecked]**:此选项允许您为选择启用/选择禁用插入一个复选框。 用户需要选中复选框来表示同意（选择启用），取消选中该复选框以取消同意（选择禁用）。

1. 选择要在以下三个选项之间更新的内容：

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**:如果用户档案选中此复选框，则必须选择要更新的订阅列表。 了解详情 [订阅列表](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**:选择加入或选择退出适用于整个渠道。 例如，如果选择退出的用户档案具有两个电子邮件地址，则这两个地址将从您的所有通信中排除。

   * **[!UICONTROL Email identity]**:选择加入或选择退出仅适用于用于访问登陆页面的电子邮件地址。 例如，如果某个用户档案有两个电子邮件地址，则只有用于选择加入的用户档案才会收到来自您品牌的通信。

1. 单击 **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** 添加其他复选框。 重复上述步骤以定义其属性。

   ![](assets/lp_designer-form-checkbox-2.png)

1. 添加所有所需的复选框后，单击 **[!UICONTROL Call to action]** 以展开相应的部分。 它允许您在 **[!UICONTROL Form]** 组件。

   ![](assets/lp_designer-form-call-to-action.png)

1. 定义单击按钮后将发生的情况：

   * **[!UICONTROL Redirect URL]**:输入用户将被重定向到的页面的URL。
   * **[!UICONTROL Confirmation text]**:键入将显示的确认文本。
   * **[!UICONTROL Link to a subpage]**:配置 [子页面](create-lp.md#configure-subpages) ，然后从显示的下拉列表中选择它。

   ![](assets/lp_designer-form-confirmation-action.png)

1. 定义在发生错误时单击按钮后将发生的情况：

   * **[!UICONTROL Redirect URL]**:输入用户将被重定向到的页面的URL。
   * **[!UICONTROL Error text]**:键入将显示的错误文本。 您可以在定义 [表单样式](#define-lp-styles).

   * **[!UICONTROL Link to a subpage]**:配置 [子页面](create-lp.md#configure-subpages) ，然后从显示的下拉列表中选择它。

   ![](assets/lp_designer-form-error.png)

1. 如果要在提交表单时进行其他更新，请选择 **[!UICONTROL Opt in]** 或 **[!UICONTROL Opt out]**，并定义要更新订阅列表、渠道还是仅使用的电子邮件地址。

   ![](assets/lp_designer-form-additionnal-update.png)

1. 保存您的内容，然后单击页面名称旁边的箭头以返回到 [登陆页面属性](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## 定义登陆页面表单样式 {#lp-form-styles}

1. 要修改表单组件内容的样式，请随时切换到 **[!UICONTROL Form style]** 选项卡。

   ![](assets/lp_designer-form-style.png)

1. 展开 **[!UICONTROL Checkboxes]** 部分定义复选框和相应文本的外观。 例如，您可以调整字体系列或大小，以及复选框边框颜色。

   ![](assets/lp_designer-form-style-checkboxes.png)

1. 展开 **[!UICONTROL Buttons]** 部分修改组件表单中按钮的外观。 例如，您可以添加边框、在悬停鼠标时编辑标签颜色或调整按钮的对齐方式。

   ![](assets/lp_designer-form-style-buttons.png)

   您可以使用 **[!UICONTROL Preview]** 按钮。 了解有关测试登陆页面的更多信息 [此处](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. 展开 **[!UICONTROL Form layout]** 部分来编辑布局设置，如背景颜色、内边距或边距。

   ![](assets/lp_designer-form-style-layout.png)

1. 展开 **[!UICONTROL Form error]** 部分，以调整在出现问题时显示的错误消息的显示。 勾选相应的选项以预览表单上的错误文本。

   ![](assets/lp_designer-form-error-preview.png)

