---
solution: Journey Optimizer
product: journey optimizer
title: 模拟内容变体
description: 了解如何在重新设计的模拟内容变体体验中并排预览所有内容变体、从底部操作栏管理这些变体，以及切换到经典体验。
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
exl-id: d9f7e0a3-b8c2-4e5f-92a1-3c1d7e8a4f65
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ea831b383982d312357e1d7893675818650325e
workflow-type: tm+mt
source-wordcount: 843
ht-degree: 1%

---


# 模拟内容变体 {#simulate-content-variations}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;在并排网格中预览所有内容变体，从合并的底部操作栏管理它们，并随时切换回经典体验。

>[!ENDSHADEBOX]

已重新设计&#x200B;**[!UICONTROL 模拟内容变体]**&#x200B;体验，以便更快速、更轻松地测试和比较变体。 现在，所有变体都在一个可滚动的网格中一起呈现，并且您需要的每个控件都可从单个底部操作栏中获得。

若要访问新体验，请在内容中单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;以打开内容模拟屏幕。 如果变体已经可用，则会立即显示预览网格。 如果尚不存在任何变体，则会显示一个空白变体，您可以使用下面描述的任何方法开始创建它们。

如果您更喜欢以前的布局，可随时在底部操作栏中单击&#x200B;**[!UICONTROL 切换到经典体验]**。 经典体验文档位于[模拟内容变体（经典体验）](simulate-sample-input.md)。

## 创建和管理变体 {#manage-variants}

可以通过不同的方式创建变体：逐个手动创建，或通过导入文件、使用人工智能生成变体或选择现有的模拟用户来手动创建。 您最多可以手动或通过文件上传添加30个变体。 在使用AI生成时，根据内容的复杂性，最多可以创建40个变体。

### 手动添加变体 {#add-variants}

要手动添加空白变体，请单击底部操作栏中的&#x200B;**[!UICONTROL +]**。 将添加新的空白变体，您可以直接输入属性值。

![](assets/simulate-variations-create.png)

您还可以使用&#x200B;**[!UICONTROL ...]** > **上载变量**&#x200B;来导入CSV、JSON或JSONLINES文件，其中每个行或条目都成为变量。 从上传对话框下载文件模板以使用正确的格式。

![](assets/simulate-variations-upload.png)

### 自动生成变体 {#auto-generate}

要使用人工智能自动生成变体，请单击底部操作栏中的&#x200B;**[!UICONTROL 生成]**&#x200B;按钮。 系统将分析您的内容，标识个性化字段和条件分支，并根据需要生成任意数量的变体以用实际值覆盖它们。 AI生成的变体可以通过其卡片上显示的闪烁图标进行标识。

![](assets/simulate-variations-ai.png)

>[!CAUTION]
>
>单击&#x200B;**[!UICONTROL 生成]**&#x200B;将替换所有现有变体，包括手动添加或从文件添加的任何变体。

### 从模拟用户中选择变体 {#simulated-users}

您的变体可以基于&#x200B;**模拟用户**，这些模拟用户是可重复使用的、类似个人资料的测试实体，可以跨会话保存并可与其他用户共享。 与手动输入的变体不同，模拟用户会保留在当前浏览器会话之外。

从历程&#x200B;**[!UICONTROL 模拟]**&#x200B;功能创建和管理模拟用户。 有关完整过程，请参阅[创建和管理模拟用户](../building-journeys/simulate-journey.md#test-users)。

要将模拟用户用作变体，请执行以下操作：

1. 单击底部操作栏中的&#x200B;**[!UICONTROL 选择变体]**。
1. 从列表中选择要使用的模拟用户，然后单击&#x200B;**[!UICONTROL 选择]**。

![](assets/simulate-variations-select.png)

选定的模拟用户将作为变体添加。 您可以在本地编辑变体的属性值以进行测试，但这些更改不会保存回模拟用户记录。

### 导出变体 {#export-variants}

您可以将所有当前变体（无论是手动添加、使用AI生成还是从模拟用户中选择）导出到CSV文件。 单击底部操作栏中的&#x200B;**[!UICONTROL ...]**，然后选择&#x200B;**[!UICONTROL 导出变体]**。

![](assets/simulate-variations-upload.png)

## 预览变体 {#preview-grid}

### 在变量之间切换 {#switch-variants}

在预览模式下，所有变体将并排呈现，顶部有一个编号指示器。 要在变体之间切换，请单击数字或使用底部操作栏中的&#x200B;**&lt; >**&#x200B;导航按钮。

![](assets/simulate-variations-switch.png)

### 在预览或编辑模式下显示变体 {#edit-variants}

您可以在预览或编辑模式下显示变体，在该模式下可以直接编辑内容和属性值。 单击底部操作栏中的&#x200B;**[!UICONTROL 预览]**&#x200B;或&#x200B;**[!UICONTROL 编辑]**，在两个模式之间一次切换所有预览。

![](assets/simulate-variations-mode.png)

要单独切换单个变体，请单击其卡顶部的&#x200B;**[!UICONTROL 显示预览]**&#x200B;或&#x200B;**[!UICONTROL 显示变体详细信息]**&#x200B;按钮，或者在底部操作栏中长按其编号（或使用Alt +向上/向下键）。

![](assets/simulate-variations-unitary-switch.png)

### 更改布局 {#change-layout}

要更改变体的显示方式，请使用&#x200B;**bottom操作栏**&#x200B;在并排、垂直栈叠或环绕布局之间切换。

![](assets/simulate-variations-layout.png)

### 在桌面视图和移动设备视图之间切换 {#switch-views}

要显示变体在不同设备上的呈现方式，请单击底部操作栏中的图标以在桌面视图和移动设备视图之间切换。 预览网格将更新，以显示变体在选定设备上的外观。

![](assets/simulate-variations-device.png)

## 电子邮件渠道的其他功能 {#email-capabilities}

在模拟电子邮件内容时，顶部栏会提供其他特定于电子邮件的工具。

![](assets/simulate-variations-top-bar.png)

* **[!UICONTROL 垃圾邮件报告]** — 针对垃圾邮件过滤器分析您的电子邮件内容并获得可投放性分数。 [了解详情](../content-management/spam-report.md)
* **[!UICONTROL 呈现电子邮件]** — 预览电子邮件在常用电子邮件客户端和设备之间的呈现方式。 [了解详情](../content-management/rendering.md)
* **[!UICONTROL 发送校样]** — 向一组电子邮件收件人发送一个或多个变体的校样。 单击&#x200B;**[!UICONTROL 发送验证]**，添加最多10个收件人地址，选择要包含的变体，然后单击&#x200B;**[!UICONTROL 发送验证]**&#x200B;以进行确认。 若要查看以前发送的校样，请单击&#x200B;**[!UICONTROL 查看校样]**。 [了解详情](../content-management/proofs.md)
* **[!UICONTROL 查看配置详细信息]** — 查看应用于此内容的渠道配置。
