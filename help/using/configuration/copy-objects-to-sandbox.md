---
solution: Journey Optimizer
product: journey optimizer
title: 在沙盒之间复制Journey Optimizer对象
description: 了解如何在沙盒之间复制历程、内容模板和片段。
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 沙盒，历程，复制，环境
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# 将Journey Optimizer对象复制到另一个沙盒 {#copy-to-sandbox}

沙盒工具允许您利用包导出和导入，跨多个沙盒复制对象，如历程、内容模板或片段。 包可以包含单个对象或多个对象。包中包含的任何对象必须来自同一沙盒。

本页介绍Journey Optimizer上下文中的沙盒工具用例。 有关功能本身的更多信息，请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html)。

>[!NOTE]
>
>此功能需要&#x200B;**沙盒管理**&#x200B;功能的以下权限：管理沙盒（或查看沙盒）和管理包。 [了解详情](../administration/ootb-permissions.md)

复制过程通过源沙盒和目标沙盒之间的资源包导出和导入来执行。 以下是将历程从一个沙盒复制到另一个沙盒的常规步骤：

1. 在源沙盒中添加要作为包导出的对象。
1. 将包导出到目标沙盒。

此外，您可以利用Journey Optimizer **对象复制服务REST API**&#x200B;来管理沙盒的对象。 [了解如何使用对象复制服务REST API](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## 导出的对象和最佳实践 {#objects}

Journey Optimizer允许将历程、内容模板和片段导出到另一个沙盒。 以下部分提供了每种对象类型的信息和最佳实践。

### 一般最佳实践 {#global}

* 复制对象时，任何依赖项（如嵌套片段、历程受众或操作）都将在父对象中正确更新，从而确保目标沙盒中的正确映射。

* 如果导出的对象包含用户档案个性化，请确保目标沙盒中存在相应的架构，以避免任何个性化问题。

### 历程 {#journeys}

* 在导出旅程时，除了旅程本身外，Journey Optimizer还会复制旅程依赖的大部分对象：受众、架构、事件和操作。 有关复制对象的更多详细信息，请参阅此[部分](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects)。

* 我们不保证将所有链接的元素复制到目标沙盒。 我们强烈建议您执行彻底检查，例如在发布历程之前。 这允许您识别任何潜在的缺失对象。

* 目标沙盒中复制的对象是唯一的，不存在覆盖现有元素的风险。 历程和历程中的任何消息都会以草稿模式引入。 这允许您在目标沙盒上发布之前执行彻底验证。

* 复制过程仅复制有关历程的元数据和该历程中的对象。 在此过程中不会复制任何用户档案或数据集数据。

### 内容模板 {#content-templates}

* 在导出内容模板时，所有嵌套片段也将随该模板一起复制。

* 导出内容模板有时会导致片段重复。 例如，如果两个模板共享同一片段并在不同的包中复制，则两个模板都需要在目标沙盒中重用同一片段。 为避免重复，请在导入过程中选择“使用现有”选项。 [了解如何导入包](#import)

* 为进一步避免重复，建议导出单个包中的内容模板。 这可确保系统高效地管理重复数据删除。

### 片段 {#fragments}

* 片段可以具有多种状态，例如实时、草稿和实时草稿正在进行。 导出片段时，其最新的草稿状态会被复制到目标沙盒中。

* 导出片段时，所有嵌套片段也将随该片段一起复制。

## 将对象添加为包{#export}

要将对象复制到另一个沙盒，您首先需要将它们作为包添加到源沙盒中。 执行以下步骤：

1. 导航到存储了要复制的第一个对象的清单，如历程列表。 单击&#x200B;**更多操作**&#x200B;图标（对象名称旁边的三个圆点），然后单击&#x200B;**添加到包**。

   ![](assets/journey-sandbox1.png)

1. 在&#x200B;**添加到包**&#x200B;窗口中，选择是将对象添加到现有包还是创建新包：

   ![](assets/journey-sandbox2.png)

   * **现有包**：从下拉菜单中选择该包。
   * **创建新包**：键入包名称。 您还可以添加描述。

1. 重复这些步骤以添加要随包导出的所有对象。

>[!NOTE]
>
>对于历程导出，除了历程本身之外，Journey Optimizer还复制了历程所依赖的大多数对象：受众、架构、事件和操作。 有关历程导出的更多详细信息，请参阅[此部分](../building-journeys/copy-to-sandbox.md)。

## Publish要导出的包 {#publish}

准备好导出包后，请按照以下步骤发布包：

1. 导航到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 沙盒]**&#x200B;菜单，选择&#x200B;**包**&#x200B;选项卡。

1. 打开要导出的包，选择要导出的对象，然后单击&#x200B;**Publish**。

   在本例中，我们要导出历程、内容模板和片段。

   ![](assets/journey-sandbox4.png)

1. 从&#x200B;**[!UICONTROL 作业]**&#x200B;选项卡跟踪包发布的状态。 有关作业的更多详细信息，请从列表中选择该作业，然后单击&#x200B;**[!UICONTROL 查看导入详细信息]**&#x200B;按钮。

   ![](assets/journey-sandbox9.png)

## 在目标沙盒中导入包 {#import}

发布包后，您需要将其导入目标沙盒中。 执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 沙盒]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 浏览]**&#x200B;选项卡。

1. 搜索要在其中导入包的沙盒，然后单击其名称旁边的+图标。

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >只有您组织内的沙盒可用。

1. 在&#x200B;**目标沙盒**&#x200B;字段中，检查是否选择了正确的目标沙盒，并从&#x200B;**[!UICONTROL 包名称]**&#x200B;下拉列表中选择要导入的包。 单击&#x200B;**下一步**。

   ![](assets/journey-sandbox6.png)

1. 查看软件包对象和依赖关系。 这是已添加到资源包中的对象列表，以及依赖于受众、架构、事件或操作的其他对象历程。

   对于每个对象，您可以选择创建新对象或使用目标沙盒中的现有对象。 例如，这可让您避免在使用通用片段导入内容模板时可能会发生的片段重复。

   ![](assets/journey-sandbox7.png)

1. 单击右上角的&#x200B;**完成**&#x200B;按钮开始将包复制到目标沙盒。 复制过程因对象的复杂性和需要复制的对象数量而异。

1. 单击导入作业以查看复制结果：

   * 单击&#x200B;**查看导入的对象**&#x200B;按钮以显示每个已复制的对象。
   * 单击&#x200B;**查看导入详细信息**&#x200B;按钮以检查每个对象的导入结果。

   ![](assets/journey-sandbox8.png)

1. 访问目标沙盒并对所有复制的对象执行彻底检查。