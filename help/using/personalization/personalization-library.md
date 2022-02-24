---
title: 使用保存的表达式
description: 了解如何使用 [!DNL Journey Optimizer] 库。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 163211f95436a37dee7deffea9ced1a3fa09dc34
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 使用保存的表达式 {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="关于表达式库"
>abstract="[!DNL Journey Optimizer] 提供一个库，您可以在其中访问已由管理员用户配置的保存个性化表达式。 "

[!DNL Journey Optimizer] 提供了一个库，您可以在其中访问之前保存的由管理员用户添加的个性化表达式。

1. 要访问保存的表达式，请单击 **[!UICONTROL Library]** 按钮。 该列表显示管理员用户保存的所有表达式(请参阅 [将表达式保存到库](#save-expressions))。

   >[!NOTE]
   >
   >您可以使用“信息”按钮获取有关已保存表达式内容的更多信息。 如果您具有管理库项目的适当权限，则“信息”按钮将显示在椭圆菜单中。

   ![](assets/library-list.png)

1. 单击+以将表达式插入编辑器。 然后，您可以像往常一样自定义和验证个性化内容。 [了解详情](../personalization/personalization-build-expressions.md)

   ![](assets/library-add.png)

## 将表达式保存到库 {#save-expressions}

[!DNL Journey Optimizer] 允许管理员用户将个性化表达式保存到库。 随后，所有用户都可以使用这些表达式来构建个性化内容。

要将表达式保存到库，请执行以下步骤：

1. 在编辑器界面中，生成表达式，然后单击 **[!UICONTROL Add to library]**.

   >[!NOTE]
   >
   >如果按钮不可见，请在Admin Console中确认您拥有所需的权限(请参阅 [权限级别](../administration/high-low-permissions.md))。

   ![](assets/library-save.png)

1. 在右侧窗格中，输入表达式的标题和说明，以帮助用户更轻松地找到它，然后单击 **[!UICONTROL Add]**.

   ![](assets/add-expression.png)

1. 表达式即会添加到库中。 现在，用户将能够使用它构建其个性化内容。


>[!NOTE]
>
>* 您在库中最多保存40个表达式。
>
>* 表达式不能超过200KB。
>
>* 保存的表达式按创建日期排序：最近添加的表达式将首先显示在列表中。



要编辑现有表达式，请将其添加到编辑器中，然后根据需要对其进行修改。 单击 **[!UICONTROL Add to library]** 验证语法并保存表达式。

要删除表达式，请单击椭圆按钮，然后单击 **[!UICONTROL Delete]**.
