---
solution: Journey Optimizer
product: journey optimizer
title: 条件
description: 在优化历程路径活动中配置条件
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活动、条件、画布、历程
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8gtrjnNNob-iRXdjSytSYOMyDswVxsrd8knipi4i1gI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: d90f0ac22c107a51967316f078f359f067b70431
workflow-type: tm+mt
source-wordcount: 2113
ht-degree: 17%

---

# 条件 {#conditions}

>[!CONTEXTUALHELP]
>id="ajo_journey_conditions"
>title="条件"
>abstract="您可以使用条件基于特定标准创建多条路径，以定义个人在您的历程中的进展情况。 您还可以配置备用路径来处理超时或错误，以确保获得无缝的体验。 请注意，现在是在优化活动中配置条件，而不是以前的条件活动。"

通过&#x200B;**条件**，您可以根据特定条件创建多个路径，以定义个人如何在您的历程中前进。 您还可以配置备用路径来处理超时或错误，以确保获得无缝的体验。

>[!NOTE]
>
>用于在历程中创建条件路径的新载体是[优化](optimize.md)活动。 它取代了以前的&#x200B;**条件**&#x200B;活动，该活动已从 UI 中移除。 现在，所有条件逻辑都可通过此页面上提供的优化活动的条件进行处理。
>
>如果您现有历程使用了&#x200B;**[!UICONTROL 条件]**&#x200B;活动，则可以继续像以前一样使用它们。 它们现在有一个新图标，显示为&#x200B;**[!UICONTROL 使用**&#x200B;[!UICONTROL &#x200B; Condition &#x200B;]&#x200B;**方法优化]**&#x200B;活动，但行为保持不变。 您在节点上设置的任何自定义标签都将保留。

## 添加条件 {#add-condition-activity}

要向历程添加条件，请执行以下步骤。

1. 将&#x200B;**[!UICONTROL 优化]**&#x200B;活动拖放到历程画布中。 [了解详情](optimize.md)

1. 添加可选标签以在报告和测试模式日志中标识活动。

1. 从&#x200B;**[!UICONTROL 方法]**&#x200B;下拉列表中选择一个条件。

   ![选择条件方法优化活动](assets/journey-optimize-condition.png){width=80%}

   可以使用以下类型的条件：

   * [数据源条件](#data_source_condition)
   * [时间条件](#time_condition)
   * [百分比拆分](#percentage_split)
   * [日期条件](#date_condition)
   * [配置文件上限](#profile_cap)
   * 您还可以在历程条件中使用受众。 [了解详情](#using-a-segment)

>[!NOTE]
>
>对于[配置文件存储区](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans#profile-data-store){target="_blank"}中包含两个以上跨设备标识的配置文件，条件评估将失败。

## 管理条件路径 {#condition_paths}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple2"
>title="关于简单表达式编辑器"
>abstract="使用简单表达式编辑器模式，您可以根据字段组合执行简单查询。 所有可用的字段都显示在屏幕的左侧。 将字段拖放到主区域中。 要组合不同的元素，它们会相互联锁，以创建不同的组和/或组级别。 然后，逻辑运算符组合同一级别上的元素。"

在历程中使用多个条件时，您可以为每个条件定义标签，以便更轻松地对其进行识别。

如果要定义多个条件，请单击&#x200B;**[!UICONTROL 添加路径]**。 对于每个条件，都会在活动后的画布中添加一个新路径。

![添加路径按钮以创建多个条件路径](assets/journey-condition-add-path.png){width=80%}

请注意，历程的设计会产生功能影响。 当在条件后定义多个路径时，将仅执行第一个符合条件的路径。 这意味着，可以通过将路径置于彼此上方或下方来更改路径的优先级。

我们假设两个条件：“这个人是VIP”和“这个人是男性”。 如果一个人同时满足两个条件，则选择第一条路径是因为它在第二条路径之上。 要更改此优先级，请将活动移至不同的垂直顺序。

![路径优先级示例显示VIP条件高于男性条件](assets/journey48.png)

通过选中&#x200B;**[!UICONTROL 显示上述情况以外的其他情况的路径]**，可以为不符合所定义条件的受众创建其他路径。

>[!NOTE]
>
>此选项在拆分条件中不可用。 [了解详情](#percentage_split)

利用简单模式，可根据字段组合执行简单查询。 所有可用的字段都显示在屏幕的左侧。 将字段拖放到主区域中。 要组合不同元素，请将它们互相联锁，以创建不同的分组和/或分组级别。 然后，您可以选择逻辑运算符来组合同一级别上的元素：

* **AND** — 两个条件的交集。 只考虑符合所有条件的元素。
* **OR** — 两个条件的并集。 考虑至少符合一个条件的元素。

![带有拖放字段和逻辑运算符的简单表达式编辑器](assets/journey64.png){width=80%}

如果您使用[Adobe Experience Platform分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}创建受众，则可以在历程条件中利用它们。 请参阅[在条件中使用受众](#using-a-segment)。

>[!NOTE]
>
>使用简单编辑器无法对时间序列（例如购买列表、过去对消息的点击）执行查询。 为此，您需要使用高级编辑器。 请参阅[此页](expression/expressionadvanced.md)。

当操作或条件中发生错误时，个人历程将停止。 使其继续的唯一方法是选中框&#x200B;**[!UICONTROL 在超时或错误的情况下添加替代路径]**。 [了解详情](../building-journeys/using-the-journey-designer.md#paths)

在简单编辑器中，您还可以在事件和数据源类别下找到历程属性类别。 此类别包含与给定用户档案的历程相关的技术字段。 这是系统从实时历程中检索到的信息，如历程 ID 或遇到的特定错误。 [了解详情](expression/journey-properties.md)

## 数据源条件 {#data_source_condition}

使用&#x200B;**[!UICONTROL 数据源条件]**&#x200B;根据来自数据源的字段或先前位于历程中的事件定义条件。 此类型的条件是使用表达式编辑器定义的。 [了解如何使用表达式编辑器](expression/expressionadvanced.md)

例如，如果您定位的受众具有使用构成工作流或自定义上传（CSV文件）生成的扩充属性，则可以利用这些扩充属性构建条件。

>[!IMPORTANT]
>
>**处理缺少或未引入的属性**
>
>如果您的配置文件架构中定义了架构字段，但尚未为该字段引入数据，则Journey Optimizer和基础实时客户配置文件将该字段解释为`null`。 因此，检查`isEmpty()`、`isNull()`或类似函数的条件将计算为`true`，即使从未引入该属性。 如果您不知道字段没有数据，这可能会导致意外的历程行为。
>
>为避免混淆，请确保在用户档案进入历程之前，已使用实际数据摄取您在条件表达式中使用的属性。 您可以验证[实时客户配置文件](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中的属性值，以确认条件中使用的字段是否存在数据。

使用高级表达式编辑器，您可以设置更高级的条件，以处理集合或使用需要传递参数的数据源。 [了解详情](../datasource/external-data-sources.md)

使用高级表达式编辑器的![数据Source条件](assets/journey50.png){width=80%}

## 日期条件 {#date_condition}

这允许您根据日期定义不同的流。 例如，如果人员在“销售”期间进入该步骤，您将向他们发送一条特定消息。 一年余下时间里，您将发送另一条消息。

>[!NOTE]
>
>时区不再特定于条件，而是现在在历程属性的历程级别定义。 [了解详情](../building-journeys/timezone-management.md)

![具有开始和结束日期字段的日期条件配置](assets/journey53.png)

## 百分比拆分 {#percentage_split}

此选项允许您随机拆分受众，以为每个组定义不同的操作。 定义每个路径的分割数和重新分区。 拆分计算是统计性的，因为系统无法预测将在历程的这个活动中流动的人数。 因此，分割具有非常低的误差容限。 此函数基于[Java随机机制](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html){target="_blank"}。

在测试模式下，当达到拆分时，始终选择顶部分支。 如果希望测试选择其他路径，可以重新组织拆分分支的位置。 [了解详情](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>请注意，在百分比拆分条件中没有用于添加路径的按钮。 路径的数量将取决于拆分的次数。 在拆分条件中，您无法为其他情况添加路径，因为它不会发生。 人们总是会走上一条不同的道路。

![百分比拆分配置，滑块显示流量分布](assets/journey52.png)

## 时间条件 {#time_condition}

使用&#x200B;**[!UICONTROL 时间条件]**&#x200B;根据一天中的小时和/或星期执行不同的操作。 例如，您可以决定在白天发送推送通知，在工作日夜间发送电子邮件。

>[!NOTE]
>
>* 时区并非特定于条件，而是在历程属性中的历程级别定义的。 [了解详情](../building-journeys/timezone-management.md)
>
>* 默认情况下，**[!UICONTROL 时间条件]**&#x200B;按小时设置，从00:00到12:00。

![具有小时范围和星期选择器的时间条件](assets/journey51.png)

提供了三个时间过滤选项：

* **小时** — 允许您根据一天中的时间设置条件。 然后，定义开始时间和结束时间。 个人将仅在定义的小时范围内输入路径。
* **星期** — 允许您根据星期设置条件。 然后，选择您希望个人输入路径的日期。
* **一周中的某天某小时** — 此选项将前两个选项组合在一起。

## 配置文件上限 {#profile_cap}

使用此条件类型可设置历程路径的最大配置文件数。 达到此限制后，输入的轮廓会采用替代路径。 这可确保您的历程不会超过定义的限制。

>[!NOTE]
>
>我们建议您定义高价值用户档案上限。 群体达到确切上限数的精度和可能性只会随着上限的增加而提高。 对于小数字（例如，50为上限），数字将不能始终匹配，因为在用户档案选择替代路径之前，可能无法达到限制。

<!--You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).-->

默认上限为1,000。

计数器仅适用于选定的历程版本。 在复制历程或创建新版本时，计数器将重置为零。 重置后，输入的配置文件再次采用名义路径，直到达到计数器限制。

在定期历程上定义用户档案上限时，计数器不会在每次定期后重置。

即使您将替代路径移动到历程画布上的名义路径上方，名义路径始终优先于替代路径。

对于实时历程，需要考虑以下阈值以确保达到限制：

* 对于大于10,000的上限，要注入的不同配置文件的数量必须至少为上限的1.3倍。
* 对于小于10,000的上限，要注入的不同配置文件的数量必须为1000加上上限。

在测试模式下不考虑用户档案上限。

![具有最大配置文件限制输入字段的配置文件上限条件](assets/profile-cap-condition.png)

## 在条件中使用受众 {#using-a-segment}

本节介绍如何在历程条件中使用受众。 有关受众以及如何构建受众的详细信息，请参阅[此部分](../audience/about-audiences.md)。

要在历程条件中使用受众，请执行以下步骤：

1. 打开历程，删除&#x200B;**[!UICONTROL 优化]**&#x200B;活动并选择&#x200B;**[!UICONTROL 数据源条件]**。

   ![在下拉菜单中选择的数据Source条件方法](assets/segment3.png)

1. 单击&#x200B;**[!UICONTROL 为每个所需的额外路径添加路径]**。 对于每个路径，单击&#x200B;**[!UICONTROL 表达式]**&#x200B;字段。

1. 在左侧，展开&#x200B;**[!UICONTROL 受众]**&#x200B;节点。 拖放要用于条件的受众。 默认情况下，受众的条件为true。

   表达式编辑器中的![受众节点，用于选择[!DNL Adobe Experience Platform]受众](assets/segment4.png){width=80%}

   >[!NOTE]
   >
   >请注意，只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才会被视为受众成员。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hans#interpret-segment-results){target="_blank"}。

➡️ **在实践中查看：**&#x200B;了解如何使用时间和星期几条件来[仅在工作日发送电子邮件](weekday-email-uc.md)。
