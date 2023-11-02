---
solution: Journey Optimizer
product: journey optimizer
title: 将历程复制到另一个沙盒
description: 了解如何将历程复制到另一个沙盒
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 沙盒，历程，复制，环境
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: b4fda6a0bd3e633811c16ef6dc3a3171b3b350c8
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 6%

---

# 将历程复制到另一个沙盒 {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

沙盒工具允许您利用包导出和导入跨多个沙盒复制对象。 软件包可以包含单个对象或多个对象。 包中包含的任何对象必须来自同一沙盒。

本页介绍Journey Optimizer上下文中的沙盒工具用例。 有关特征本身的更多信息，请参阅 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html).

>[!NOTE]
>
>此功能需要以下权限： manage-sandbox （或view-sandbox）和manage-package。

## 沙盒工具入门{#sandbox-gs}

可以使用 Journey Optimizer 将整个历程从一个沙盒复制到另一个沙盒。例如，您可以将历程从暂存沙盒环境复制到生产沙盒。 除了历程本身，Journey Optimizer还复制历程依赖的大部分对象：受众、架构、事件和操作。 有关复制对象的更多详细信息，请参阅此 [部分](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects).

>[!CAUTION]
>
>我们不保证将所有链接的元素复制到目标沙盒中。 我们强烈建议您在发布历程之前执行彻底检查。 这将允许您识别任何可能缺少的对象。

目标沙盒中复制的对象是唯一的，不存在覆盖现有元素的风险。 历程和历程中的任何消息都会以草稿模式引入。 这允许您在目标沙盒上发布之前执行彻底验证。 复制过程仅复制有关历程的元数据和该历程中的对象。 在此过程中不会复制任何用户档案或数据集数据。

复制过程通过源沙盒和目标沙盒之间的资源包导出和导入来执行。 以下是将历程从一个沙盒复制到另一个沙盒的常规步骤：

1. 将历程作为包添加到源沙盒中。
1. 将包导出到目标沙盒。

此外，您还可以利用Journey Optimizer **对象复制服务REST API** 以管理沙盒的对象。 [了解如何使用对象复制服务REST API](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## 将历程添加为包{#export}

要将历程复制到另一个沙盒，您首先需要将该历程作为包添加到源沙盒中。 执行以下步骤：

1. 在历程管理菜单部分，单击 **[!UICONTROL 历程]**. 将显示历程列表。

1. 搜索要复制的历程，单击 **更多操作** 图标（历程名称旁边的三个圆点）并单击 **添加到包**.

   ![](assets/journey-sandbox1.png)

   此 **添加到包** 窗口随即显示。

   ![](assets/journey-sandbox2.png)

1. 选择是要将历程添加到现有包还是创建新包：

   * **现有包**：从下拉菜单中选择资源包。
   * **创建新资源包**：键入包名称。 您还可以添加描述。

1. 在“管理”菜单部分中，单击 **[!UICONTROL 沙盒]**，选择 **包** 选项卡，然后单击要导出的资源包。

   ![](assets/journey-sandbox3.png)

1. 选择要导出的对象，然后单击 **Publish**

   ![](assets/journey-sandbox4.png)

   如果发布失败，您可以检查日志以确定失败原因。 打开包，单击 **查看失败的作业**，选择导入作业并单击 **查看导入详细信息**.

   ![](assets/journey-sandbox9.png)

## 将包导出到目标沙盒 {#import}

发布包后，您需要将其导出到目标沙盒。

1. 在源沙盒中，单击 **[!UICONTROL 沙盒]** 菜单，选择 **包** 选项卡，然后单击要导出的资源包旁边的+图标。

   ![](assets/journey-sandbox5.png)

1. 选择 **Target沙盒** ，然后单击 **下一个**. 只有您组织内的沙盒可用。

   ![](assets/journey-sandbox6.png)

1. 查看软件包对象和依赖关系。 这是在历程中使用的关联对象的列表。此列表显示名称和对象类型。 对于每个对象，您可以选择创建新对象或使用目标沙盒中的现有对象。

   ![](assets/journey-sandbox7.png)

1. 单击 **完成** 按钮，开始将包复制到target沙盒。 复制过程因历程的复杂性以及需要复制的对象数量而异。

1. 单击导入作业以查看复制结果：

   * 单击 **查看导入的对象** 显示每个复制的对象。
   * 单击 **查看导入详细信息** 检查每个对象的导入结果。

   ![](assets/journey-sandbox8.png)

1. 访问目标沙盒并对所有复制的对象执行彻底检查。
