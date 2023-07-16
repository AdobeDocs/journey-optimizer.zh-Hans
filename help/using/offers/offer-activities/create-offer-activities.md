---
title: 创建决策
description: 了解如何创建决策
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: f4e4a6dfeee0205aa3d8abbd1d6b237dcf14cb10
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 1%

---

# 创建决策 {#create-offer-activities}

决策是优惠的容器，它们将利用优惠决策引擎，以便根据投放目标来选择应投放的最佳优惠。

➡️ [在此视频中了解如何创建优惠活动](#video)

决策列表可在 **[!UICONTROL 选件]** 菜单> **[!UICONTROL 决策]** 选项卡。 过滤器可帮助您根据其状态或开始和结束日期检索决策。

![](../assets/activities-list.png)

在创建决策之前，请确保已在优惠库中创建了以下组件：

* [投放位置](../offer-library/creating-placements.md)
* [收藏集](../offer-library/creating-collections.md)
* [个性化优惠](../offer-library/creating-personalized-offers.md)
* [后备优惠](../offer-library/creating-fallback-offers.md)

## 创建决策 {#create-activity}

1. 访问决策列表，然后单击 **[!UICONTROL 创建决策]**.

1. 指定决策的名称。

1. 根据需要定义开始和结束日期和时间，然后单击 **[!UICONTROL 下一个]**.

   ![](../assets/activities-name.png)

1. 要将自定义或核心数据使用标签分配给决策，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级访问控制(OLAC)的更多信息](../../administration/object-based-access.md)

## 定义决策范围 {#add-decision-scopes}

1. 从下拉列表中选择一个版面。 它将被添加到您决策中的第一个决策范围。

   ![](../assets/activities-placement.png)

1. 单击 **[!UICONTROL 添加]** 以选择此投放位置的评估标准。

   ![](../assets/activities-evaluation-criteria.png)

   每个标准都包含与资格约束关联的优惠收藏集和排名方法，以确定要在投放位置中显示的优惠。

   >[!NOTE]
   >
   >至少需要一个评估标准。

1. 选择包含要考虑的选件的选件收藏集，然后单击 **[!UICONTROL 添加]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >您可以单击 **[!UICONTROL 打开优惠收藏集]** 用于在新选项卡中显示收藏集列表的链接，通过该链接可浏览收藏集及其包含的优惠。

   选定的收藏集将添加到标准中。

   ![](../assets/activities-collection-added.png)

1. 使用 **[!UICONTROL 资格]** 用于限制为此投放位置选择优惠的字段。

   此约束可以通过使用 **决策规则**，或者一个或多个 **Adobe Experience Platform受众**. 有关详情，请参阅 [本节](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * 要将优惠选择限制为Experience Platform受众的成员，请选择 **[!UICONTROL 受众]**，然后单击 **[!UICONTROL 添加受众]**.

     ![](../assets/activity_constraint_segment.png)

     从左窗格添加一个或多个受众，然后使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 逻辑运算符。

     ![](../assets/activity_constraint_segment2.png)

     了解如何在中使用受众 [本节](../../audience/about-audiences.md).

   * 如果要为决策规则添加选择约束，请使用 **[!UICONTROL 决策规则]** 选项并选择您选择的规则。

     ![](../assets/activity_constraint_rule.png)

     了解如何在中创建决策规则 [本节](../offer-library/creating-decision-rules.md).

1. 在选择受众或决策规则时，您可以查看有关预计的合格用户档案的信息。 单击 **[!UICONTROL 刷新]** 以更新数据。

   >[!NOTE]
   >
   >当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。 例如，一个资格规则，要求当前天气为≥80度。

   ![](../assets/activity_constraint-estimate.png)

1. 定义要用于为每个用户档案选择最佳选件的排名方法。 [了解详情](../offer-activities/configure-offer-selection.md)。

   ![](../assets/activity_ranking-method.png)

   * 默认情况下，如果有多个选件符合此投放位置的条件， **[!UICONTROL 优惠优先级]** 方法使用选件中定义的值：会将具有最高优先级分数的选件交付给用户。

   * 如果要使用特定的计算得分来选择要交付的合格优惠，请选择 **[!UICONTROL 公式]** 或 **[!UICONTROL AI模型]**. [了解详情](../offer-activities/configure-offer-selection.md)。

1. 单击 **[!UICONTROL 添加]** 为同一放置定义更多标准。

   ![](../assets/activity_add-collection.png)

1. 添加多个标准时，将按特定顺序评估这些标准。 将首先评估添加到序列中的第一个集合，依此类推。 [了解详情](#evaluation-criteria-order)

   要更改默认序列，您可以拖放收藏集以根据需要重新排序。

   ![](../assets/activity_reorder-collections.png)

1. 还可同时评估多个标准。 要执行此操作，请将收藏集拖放到另一个收藏集上。

   ![](../assets/activity_move-collection.png)

   它们现在具有相同的排名，因此将同时进行评估。 [了解详情](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

1. 要在此决策中添加其他优惠版面，请使用 **[!UICONTROL 新范围]** 按钮。 对每个决策范围重复上述步骤。

   ![](../assets/activity_new-scope.png)

   >[!NOTE]
   >
   >添加多个决策范围时，评估标准顺序将受到影响。 [了解详情](#multiple-scopes)

### 评估标准顺序 {#evaluation-criteria-order}

如上所述，评估标准由收集、资格约束和排名方法组成。 可以设置评估标准的评估顺序，但也可以合并多个评估标准，以便一起评估而不是单独评估。

#### 具有一个范围 {#one-scope}

在单个决策范围内，多个标准及其分组决定了标准的优先级和合格优惠的排名。 第一个条件具有最高优先级，并且在同一“组”中组合的条件具有相同的优先级。

例如，您有两个集合，一个在评估标准A中，一个在评估标准B中。请求发送回两个选件。 假设有两个符合评估标准A的优惠和三个符合评估标准B的优惠。

* 如果两个评估标准为 **未合并** 和/或按顺序（1和2），评估标准中前两个符合条件的优惠将返回第一行。 如果第一个评估标准中没有两个符合条件的优惠，则决策引擎将依次转到下一个评估标准，以查找仍需要多少优惠，并且最终将在需要时返回回退。

  ![](../assets/activity_consecutive-rank-collections.png)

* 如果两个收藏集为 **同时评估**，因为有两个来自评估标准A的合格选件和三个来自评估标准B的合格选件，所以这五个选件都将根据各自的排名方法确定的值栈叠在一起。 由于请求了两个选件，因此将返回这五个选件中符合条件的前两个选件。

  ![](../assets/activity_same-rank-collections.png)

+++ **具有多个标准的示例**

现在，让我们看一个示例，其中您对划分为不同组的单个范围有多个标准。

您定义了三个标准。 第1项和第2项准则在第1组中合并在一起，第3项准则是独立的（第2组）。

每个标准的合格优惠及其优先级（用于排名功能评估）如下：

* 第1组：
   * 标准1 — （选件1、选件2、选件3） — 优先级1
   * 标准2 — （选件3、选件4、选件5） — 优先级1

* 第2组：
   * 标准3 — （选件5，选件6） — 优先级0

首先评估优先级最高的标准选件，并将其添加到排名选件列表。

**迭代1：**

标准1和标准2选件将一起评估（选件1、选件2、选件3、选件4、选件5）。 假设结果为：

选件1 - 10选件2 - 20选件3 - 30来自标准1,45来自标准2。 两者中的最高值将被考虑在内，因此45将被考虑在内。
选件4 - 40选件5 - 50

排名后的选件现在如下所示：选件5、选件3、选件4、选件2、选件1。

**迭代2：**

评估标准3选件（选件5、选件6）。 假设结果为：

* 选件5 — 将不进行评估，因为它已存在于上述结果中。
* 选件6 - 60

排名后的选件现在如下所示：选件5 、选件3、选件4、选件2、选件1、选件6。

+++

#### 使用多个范围 {#multiple-scopes}

**如果复制关闭**

将多个决策范围添加到决策时，如果投放位置中不允许重复，则会按请求中决策范围的顺序依次选择符合条件的优惠。

>[!NOTE]
>
>此 **[!UICONTROL 允许跨投放位置复制]** 参数在放置级别设置。 如果将decisioning请求中任何投放位置的duplication设置为false，则该请求中的所有投放位置都将继承false设置。 [了解有关复制参数的更多信息](../offer-library/creating-placements.md)

让我们举一个示例，您添加了两个决策范围，例如：

* 范围1：有四个符合条件的优惠（选件1、选件2、选件3、选件4），请求将返回两个选件。
* 范围2：有四个符合条件的优惠（选件1、选件2、选件3、选件4），请求将返回两个选件。

+++ **示例 1**

选择如下：

1. 将返回范围1中符合条件的前两个选件（选件1、选件2）。
1. 将返回范围2中其余两个符合条件的优惠（选件3、选件4）。

+++

+++ **示例 2**

在此示例中，选件1已达到其频率上限。 [了解有关频率上限的更多信息](../offer-library/add-constraints.md#capping)

选择如下：

1. 将返回范围1中其余两个符合条件的优惠（选件2、选件3）。
1. 将返回范围2中剩余的合格选件（选件4）。

+++

+++ **示例 3**

在此示例中，选件1和选件3已达到其频率上限。 [了解有关频率上限的更多信息](../offer-library/add-constraints.md#capping)

选择如下：

1. 将返回范围1中其余两个符合条件的优惠（选件2、选件4）。
1. 范围2中没有剩余的合格优惠，因此 [后备优惠](#add-fallback) 会返回。

+++

**如果复制开启**

当允许跨所有投放位置重复时，可以在不同的投放位置中多次提议相同的投放内容。 如果启用，系统将为多个投放位置考虑相同的选件。 [了解有关复制参数的更多信息](../offer-library/creating-placements.md)

让我们举一个与上面相同的例子，其中您添加了两个决策范围，例如：

* 范围1：有四个符合条件的优惠（选件1、选件2、选件3、选件4），请求将返回两个选件。
* 范围2：有四个符合条件的优惠（选件1、选件2、选件3、选件4），请求将返回两个选件。

+++ **示例 1**

选择如下：

1. 将返回范围1中符合条件的前两个选件（选件1、选件2）。
1. 将返回范围2中相同的前两个符合条件的优惠（选件1、选件2）。

+++

+++ **示例 2**

在此示例中，选件1已达到其频率上限。 [了解有关频率上限的更多信息](../offer-library/add-constraints.md#capping)

选择如下：

1. 将返回范围1中其余两个符合条件的优惠（选件2、选件3）。

1. 将返回范围2中其余两个符合条件的优惠（选件2、选件3）。

+++

+++ **示例 3**

在此示例中，选件1和选件3已达到其频率上限。 [了解有关频率上限的更多信息](../offer-library/add-constraints.md#capping)

选择如下：

1. 将返回范围1中其余两个符合条件的优惠（选件2、选件4）。

1. 将返回范围2中其余两个符合条件的优惠（选件2、选件4）。

+++

## 添加后备优惠 {#add-fallback}

定义决策范围后，请定义作为最后的手段向不符合优惠资格规则和限制的客户提供的备用优惠。

为此，请从决策中定义的版面的可用备用优惠列表中选择它，然后单击 **[!UICONTROL 下一个]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>您可以单击 **[!UICONTROL 打开选件库]** 用于在新选项卡中显示优惠列表的链接。

## 查看并保存决策 {#review}

如果一切配置正确，则会显示决策属性的摘要。

1. 确保决策已准备就绪，可用于向客户提供优惠。 将显示所有决策范围及其包含的备用优惠。

   ![](../assets/review-decision.png)

1. 可以展开或折叠每个投放位置。 您可以预览每个投放位置的可用优惠、资格和排名详细信息。 您还可以显示有关预计的合格用户档案的信息。 单击 **[!UICONTROL 刷新]** 以更新数据。

   ![](../assets/review-decision-details.png)

1. 单击&#x200B;**[!UICONTROL 完成]**。
1. 选择 **[!UICONTROL 保存并激活]**.

   ![](../assets/save-activities.png)

   您还可以将决策另存为草稿，以便稍后对其进行编辑和激活。

决策显示在列表中，其中包含 **[!UICONTROL 实时]** 或 **[!UICONTROL 草稿]** 状态，具体取决于您在上一步中是否激活了该活动。

它现在可用于向客户提供优惠。

## 决策列表 {#decision-list}

从决策列表中，您可以选择决策以显示其属性。 您还可以从此处编辑和更改其状态(**草稿**， **实时**， **完成**， **已存档**)、复制决策或将其删除。

![](../assets/decision_created.png)

选择 **[!UICONTROL 编辑]** 按钮以返回到决策编辑模式，您可以在其中修改决策的 [详细信息](#create-activity)， [决策范围](#add-decision-scopes) 和 [后备优惠](#add-fallback).

>[!IMPORTANT]
>
>如果对历程消息中使用的优惠决策进行了更改，则需要取消发布历程并重新发布它。  这将确保将更改纳入历程的消息中，并且消息与最新更新一致。

选择实时决策并单击 **[!UICONTROL 取消激活]** 将决策状态设回 **[!UICONTROL 草稿]**.

要再次将状态设置为，请执行以下操作 **[!UICONTROL 实时]**，选择 **[!UICONTROL 激活]** 按钮。

![](../assets/decision_activate.png)

此 **[!UICONTROL 更多操作]** 按钮可启用下面所述的操作。

![](../assets/decision_more-actions.png)

* **[!UICONTROL 完成]**：将决策的状态设置为 **[!UICONTROL 完成]**，这意味着不能再调用该决策。 此操作仅适用于已激活的决策。 该决策仍然可以从列表中获得，但您不能将其状态重新设置为 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已批准]**. 您只能复制、删除或存档它。

* **[!UICONTROL 复制]**：创建具有相同属性、决策范围和备用优惠的决策。 默认情况下，新决策具有 **[!UICONTROL 草稿]** 状态。

* **[!UICONTROL 删除]**：从列表中删除决策。

  >[!CAUTION]
  >
  >该决策及其内容将无法再访问。 此操作无法撤销。
  >
  >如果决策用于其他对象，则无法删除该决策。

* **[!UICONTROL 存档]**：将决策状态设置为 **[!UICONTROL 已存档]**. 该决策仍然可以从列表中获得，但您不能将其状态重新设置为 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已批准]**. 您只能复制或删除它。

您还可以通过选择相应的复选框同时删除或更改多个决策的状态。

![](../assets/decision_multiple-selection.png)

如果要更改具有不同状态的多个决策的状态，则只会更改相关状态。

![](../assets/decision_change-status.png)

创建决策后，您可以从列表中单击其名称。

![](../assets/decision_click-name.png)

这样，您就可以访问该决策的详细信息。 选择 **[!UICONTROL 更改日志]** 按Tab键至 [监控所有更改](../get-started/user-interface.md#changes-log) 已做出此决定。

![](../assets/decision_information.png)

## 操作方法视频{#video}

了解如何在决策管理中创建优惠活动。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


