---
title: 设计登陆页面
description: 了解如何在Journey Optimizer中设计登陆页面的内容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: c61b8d80-17e1-4fdd-a739-efcee032dc23
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 1%

---

# 设计登陆页面内容 {#design-lp-content}

开始为登陆创建内容 [主页](create-lp.md#configure-primary-page) 或 [子页面](create-lp.md#configure-subpages)，将鼠标悬停在主页面内容上并单击 **[!UICONTROL Open Designer]**. 您还可以单击右侧面板中的相应按钮。

![](assets/lp_open-designer.png)

从此处，您可以：

* **从头开始设计登陆页面** 通过内容设计器的界面，并利用 [Adobe Experience Manager Assets Essentials](../design/assets-essentials.md). 了解如何设计内容或使用内置模板 [在此部分中](../design/create-email-content.md).

* **代码或粘贴原始HTML** 直接导入内容设计器。 了解如何编码您自己的内容 [在此部分中](../design/code-content.md).

* **导入现有HTML内容** 文件或.zip文件夹中。 了解如何导入内容 [在此部分中](../design/existing-content.md).

>[!NOTE]
>
>登陆页面内容设计器与电子邮件设计器大体相似。 了解详情 [设计内容 [!DNL Journey Optimizer]](../design/design-emails.md).

## 定义登陆页面特定的内容 {#define-lp-specific-content}

要定义允许用户从登陆页面选择和提交其选择的特定内容，请执行以下步骤。

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

## 定义登陆页面表单样式 {#define-lp-styles}

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

