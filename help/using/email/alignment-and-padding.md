---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中调整垂直对齐和填充
description: 了解如何调整垂直对齐方式和内边距
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 垂直对齐，电子邮件编辑器，填充
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
source-git-commit: 4817b7426abf202c886b7fd63d59aa0f245e5496
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 6%

---

# 调整垂直对齐方式和间距 {#alignment-and-padding}

在本例中，我们将调整由三列组成的结构组件内的填充和垂直对齐。

1. 直接在电子邮件中或使用左侧菜单中提供的&#x200B;**[!UICONTROL 导航树]**&#x200B;选择结构组件。

1. 在工具栏中，单击&#x200B;**[!UICONTROL 选择一个列]**，然后选择要编辑的列。 也可以从结构树中选择它。

   该列的可编辑参数显示在&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡中。

   ![](assets/alignment_2.png)

1. 在&#x200B;**[!UICONTROL 对齐方式]**&#x200B;下，选择&#x200B;**[!UICONTROL 顶部]**、**[!UICONTROL 中间]**&#x200B;或&#x200B;**[!UICONTROL 底部]**。

   ![](assets/alignment_3.png)

1. 在&#x200B;**[!UICONTROL 填充]**&#x200B;下，定义所有边的填充。

   如果要微调边距，请选择&#x200B;**[!UICONTROL 每边不同的边距]**。 单击锁定图标可中断同步。

   ![](assets/alignment_4.png)

1. 以类似的方式继续调整其他列的对齐方式和内边距。

1. 保存更改。

>[!TIP]
>
>在Android设备上为Gmail设计电子邮件内容时，请确保图像和分隔符使用列边距，而不是较大的固定边距。 Android上的Gmail经常错误地呈现过大的图像和边距，导致布局溢出或分隔线减少。 使用较小的图像宽度或依靠基于列的填充来实现一致的显示。

## 使用痕迹导航管理片段填充 {#fragment-padding-breadcrumb}

在Email Designer中使用[片段](../content-management/fragments.md)时，您可能会遇到隐藏或残余填充，这些填充对移动设备渲染的影响与对桌面设备的影响不同。 当片段已解锁或[继承已中断](use-visual-fragments.md#break-inheritance)时，这种情况尤其常见，因为剩余样式可以保留在基础列或文本组件中。

要识别和编辑片段中的剩余边距，请执行以下操作：

1. 使用&#x200B;**[!UICONTROL 导航树]**&#x200B;或直接单击编辑器中的元素以选择片段中的每个父结构或列。 这有助于您找到特定于移动设备的隐藏边距或边距。

1. 在痕迹导航中选择元素后，导航到右侧的&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡。

1. 查看&#x200B;**[!UICONTROL 内边距]**&#x200B;设置，并根据需要删除或重新调整内边距，以实现正确的移动设备对齐方式。

1. 如果在重用片段时仍然存在对齐问题，请对片段中的其他列或文本组件重复此过程。

>[!NOTE]
>
>当重复插入和删除片段时，会发生此行为，因为样式规则可以累积。 始终使用痕迹导航验证填充值，尤其是在定位移动设备时。