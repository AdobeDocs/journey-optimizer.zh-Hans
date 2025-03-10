---
solution: Journey Optimizer
product: journey optimizer
title: 在多步营销活动中使用更新数据活动
description: 了解如何使用更新数据活动
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 13%

---

# 更新数据 {#update-data}

**更新数据**&#x200B;活动是&#x200B;**数据管理**&#x200B;活动。 它允许您对数据库中的字段执行批量更新。 您可以通过多个选项将数据更新个性化。

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## 配置更新数据活动{#update-data-configuration}

要配置&#x200B;**更新数据**&#x200B;活动，请从将该活动添加到多步骤营销活动并定义标签开始。

![](../assets/workflow-update-data.png)

### 操作类型

**操作类型**&#x200B;字段允许您选择对数据库中的数据执行的进程：

* **插入或更新**：插入数据或更新数据（如果数据库中已存在记录）。
* **插入**：仅插入数据。 已存在的记录不会更新。如果定义了协调条件，则只会添加未协调的记录。
* **更新**：只更新数据库中已存在之记录的数据。
* **删除**：删除数据。

**批量大小**&#x200B;字段允许您选择要更新的集客过渡元素数量。 例如，如果您声明500，则处理的前500条记录将被更新。

### 记录标识

此部分允许您指定如何标识数据库中的记录：

* 如果数据条目与现有的定向维度相关，请选择&#x200B;**使用定向维度**&#x200B;选项，然后从&#x200B;**要更新的定向维度**&#x200B;字段中选择它。
* 您还可以选择&#x200B;**使用自定义链接**，并指定一个或多个用于识别数据库中数据的链接
* 如果所选操作类型需要更新，则必须使用&#x200B;**使用协调规则**&#x200B;选项。

### 要更新的字段

在要更新的&#x200B;**字段**&#x200B;部分中，添加将应用更新的字段，并根据需要添加条件以执行此更新。 为此，请使用&#x200B;**Takended account if**&#x200B;字段。 按列表顺序依次应用条件。使用右侧的箭头可更改更新的顺序。您可以多次使用同一目标字段。

您可以使用&#x200B;**自动映射**&#x200B;按钮自动链接字段。 自动链接会检测具有相同名称的字段。

在&#x200B;**插入或更新**&#x200B;操作类型期间，您可以单独选择要应用于每个字段的操作。 为此，请在&#x200B;**操作类型**&#x200B;字段中选择所需的值。

### 高级选项

通过&#x200B;**高级选项**，可指定其他选项来处理数据更新和管理重复项。

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

后两个选项允许您执行特定操作：

* **生成叫客过渡**：创建将在执行结束时激活的叫客过渡。 更新通常表示定向多步营销活动结束，因此默认不会激活选项。

* **为拒绝生成叫客过渡**：创建一个叫客过渡，其中包含更新后未正确处理的记录（例如，如果存在重复项）。 更新通常会标记定向多步骤营销活动的结尾，因此默认情况下不激活此选项。
