---
solution: Journey Optimizer
product: journey optimizer
title: 条件活动
description: 了解条件活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活动、条件、画布、历程
exl-id: 02de069c-3009-4105-aa98-c49959d3efda
version: Journey Orchestration
hide: true
TQID: https://experienceleague.adobe.com/gbZUkOhk-3yBMdxwj3YpPbQrbpMhd6PkNf1hzl-2DFw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 2580
ht-degree: 12%

---

# 条件活动 {#condition-activity}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用条件活动，根据规则、数据和受众成员资格，将用户档案路由到不同的历程路径。

>[!ENDSHADEBOX]

使用条件活动，根据规则和数据将用户档案路由到不同的路径。

## 添加一个条件活动 {#add-condition-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_condition"
>title="条件活动"
>abstract="您可以使用&#x200B;**条件**&#x200B;活动根据特定条件创建多条路径，以定义个人在您的历程中的进展情况。 您还可以配置备用路径来处理超时或错误，以确保获得无缝的体验。"

您可以使用&#x200B;**条件**&#x200B;活动根据特定条件创建多条路径，以定义个人在您的历程中的进展情况。 您还可以配置备用路径来处理超时或错误，以确保获得无缝的体验。

![历程画布中的条件活动，带有多个路径选项](assets/journey49.png)

可以使用以下类型的条件：

* [数据Source条件](#data_source_condition)
* [时间条件](#time_condition)
* [百分比拆分](#percentage_split)
* [日期条件](#date_condition)
* [配置文件上限](#profile_cap)

您也可以根据受众成员资格来设定条件。 请参阅以下部分：

* [在条件中使用受众](#using-a-segment) — 根据配置文件是否属于受众添加路径。
* [生成并定位受众](../audience/about-audiences.md) — 在“受众”菜单中创建并管理受众。
* [历程中的受众定位](read-audience.md#audience-targeting-in-journeys) — 在读取受众活动后，使用条件分段、排除或合并分支。

>[!NOTE]
>
>对于[配置文件存储区](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}中包含两个以上跨设备标识的配置文件，条件评估将失败。

## 添加和管理条件路径 {#about_condition}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple"
>title="关于简单表达式编辑器"
>abstract="使用简单表达式编辑器模式，您可以根据字段组合执行简单查询。 所有可用的字段都显示在屏幕的左侧。 将字段拖放到主区域中。 要组合不同元素，可将其相互嵌套以创建不同的组和/或组级别。 随后使用逻辑运算符组合处于同一级别的元素。"

在历程中使用多个条件时，您可以为每个条件定义标签，以便更轻松地对其进行识别。

如果要定义多个条件，请单击&#x200B;**[!UICONTROL 添加路径]**。 对于每个条件，都会在活动后的画布中添加一个新路径。

![在条件活动中添加路径按钮以创建其他路径](assets/journey47.png)

请注意，历程的设计会产生功能影响。 当在条件后定义多个路径时，将仅执行第一个符合条件的路径。 这意味着，可以通过将路径置于彼此上方或下方来更改路径的优先级。

我们假设两个条件：“这个人是VIP”和“这个人是男性”。 如果一个人同时满足两个条件，则选择第一条路径是因为它在第二条路径之上。 要更改此优先级，请将活动移至不同的垂直顺序。

![路径优先级显示VIP和男性条件](assets/journey48.png)

通过选中&#x200B;**[!UICONTROL 显示上述情况以外的其他情况的路径]**，可以为不符合所定义条件的受众创建其他路径。 请注意，此选项在拆分条件中不可用。 请参阅[百分比拆分](#percentage_split)。

利用简单模式，可根据字段组合执行简单查询。 所有可用的字段都显示在屏幕的左侧。 将字段拖放到主区域中。 要组合不同元素，请将它们互相联锁，以创建不同的分组和/或分组级别。 然后，您可以选择逻辑运算符来组合同一级别上的元素：

* AND：两个条件的交集。 只考虑符合所有条件的元素。
* 或：两个条件的并集。 考虑至少符合一个条件的元素。

![表达式编辑器，显示字段选择和逻辑运算符AND](assets/journey64.png)

如果您使用[[!DNL Adobe Experience Platform] 分段服务](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}创建受众，则可以在历程条件中利用它们。 请参阅[在条件](../building-journeys/condition-activity.md#using-a-segment)中使用受众。 有关如何在Journey Optimizer中生成和定位受众的详细信息，请参阅[此部分](../audience/about-audiences.md)。


>[!NOTE]
>
>使用简单编辑器无法对时间序列（例如购买列表、过去对消息的点击）执行查询。 为此，您需要使用高级编辑器。 请参阅[此页](expression/expressionadvanced.md)。



当操作或条件中发生错误时，个人历程将停止。 使其继续的唯一方法是选中框&#x200B;**[!UICONTROL 在超时或错误的情况下添加替代路径]**。 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

在简单编辑器中，您还可以在事件和数据源类别下找到历程属性类别。 此类别包含与给定用户档案的历程相关的技术字段。 这是系统从实时历程中检索到的信息，如历程 ID 或遇到的特定错误。 [了解详情](expression/journey-properties.md)

## 数据Source条件 {#data_source_condition}

使用&#x200B;**[!UICONTROL Data Source条件]**&#x200B;根据数据源中的字段或以前位于历程中的事件定义条件。 此类型的条件是使用表达式编辑器定义的。 在[本节](expression/expressionadvanced.md)中了解如何使用表达式编辑器。

例如，如果您定位的受众具有使用构成工作流或自定义上传（CSV文件）生成的扩充属性，则可以利用这些扩充属性构建条件。

>[!IMPORTANT]
>
>**处理缺少或未引入的属性**
>
>如果您的配置文件架构中定义了架构字段，但尚未为该字段引入数据，则Journey Optimizer和基础实时客户配置文件将该字段解释为`null`。 因此，检查`isEmpty()`、`isNull()`或类似函数的条件将计算为`true`，即使从未引入该属性。 如果您不知道字段没有数据，这可能会导致意外的历程行为。
>
>为避免混淆，请确保在用户档案进入历程之前，已使用实际数据摄取您在条件表达式中使用的属性。 您可以验证[实时客户配置文件](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中的属性值，以确认条件中使用的字段是否存在数据。

使用高级表达式编辑器，您可以设置更高级的条件，以处理集合或使用需要传递参数的数据源。 [了解详情](../datasource/external-data-sources.md)。

使用表达式编辑器的![数据Source条件配置](assets/journey50.png)

## 时间条件 {#time_condition}

使用&#x200B;**[!UICONTROL 时间条件]**&#x200B;根据一天中的小时和/或星期执行不同的操作。 例如，您可以决定在白天发送推送通知，在工作日夜间发送电子邮件。

>[!NOTE]
>
>* 时区并非特定于条件，而是在历程属性中的历程级别定义的。 请参阅[此页面](../building-journeys/timezone-management.md)以了解详情。
>
>* 默认情况下，**[!UICONTROL 时间条件]**&#x200B;按小时设置，从00:00到12:00。

![时间条件设置包含小时和星期几筛选器](assets/journey51.png)

提供了三个时间过滤选项：

* 小时：用于根据一天中的时间来设置条件。 然后，定义开始时间和结束时间。 个人将仅在定义的小时范围内输入路径。
* 每周时间：允许您根据每周时间设置条件。 然后，选择您希望个人输入路径的日期。
* 星期和小时：此选项将前两个选项组合在一起。

## 百分比拆分 {#percentage_split}

此选项允许您随机拆分受众，以为每个组定义不同的操作。 定义每个路径的分割数和重新分区。 拆分计算是统计性的，因为系统无法预测将在历程的这个活动中流动的人数。 因此，分割具有非常低的误差容限。 此函数基于Java随机机制（请参阅此[页面](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html){target="_blank"}）。

在测试模式下，当达到拆分时，始终选择顶部分支。 如果希望测试选择其他路径，可以重新组织拆分分支的位置。 请参见[此页面](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>请注意，在百分比拆分条件中没有用于添加路径的按钮。 路径的数量将取决于拆分的次数。 在拆分条件中，您无法为其他情况添加路径，因为它不会发生。 人们总是会走上一条不同的道路。

![具有多个路径和分布的百分比拆分配置](assets/journey52.png)

## 日期条件 {#date_condition}

这允许您根据日期定义不同的流。 例如，如果人员在“销售”期间进入该步骤，您将向他们发送一条特定消息。 一年余下时间里，您将发送另一条消息。

>[!NOTE]
>
>时区不再特定于条件，而是现在在历程属性的历程级别定义。 请参阅[此页](../building-journeys/timezone-management.md)。

![日期范围选择器的日期条件配置](assets/journey53.png)

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

![具有最大配置文件限制设置的配置文件上限条件](assets/profile-cap-condition.png)

## 在条件中使用受众 {#using-a-segment}

本节介绍如何在历程条件中使用受众。 有关受众以及如何构建受众的详细信息，请参阅[此部分](../audience/about-audiences.md)。

要在历程条件中使用受众，请执行以下步骤：

1. 打开历程，删除&#x200B;**[!UICONTROL 条件]**&#x200B;活动并选择&#x200B;**数据Source条件**。

   条件活动中的![数据Source条件选择](assets/segment3.png)

1. 单击&#x200B;**[!UICONTROL 为每个所需的额外路径添加路径]**。 对于每个路径，单击&#x200B;**[!UICONTROL 表达式]**&#x200B;字段。

1. 在左侧，展开&#x200B;**[!UICONTROL 受众]**&#x200B;节点。 拖放要用于条件的受众。 默认情况下，受众的条件为true。

   在表达式编辑器中![从受众节点中选择受众](assets/segment4.png)

   >[!NOTE]
   >
   >请注意，只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才会被视为受众成员。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍了Journey Optimizer中的条件活动，包括五种可用的条件类型（数据Source、时间、百分比拆分、日期和配置文件上限），以及如何根据规则、数据或受众成员资格将配置文件路由到不同的旅程路径。

**意图：**
* 将条件活动添加到历程并创建多个分支路径
* 使用表达式编辑器配置Data Source条件，以评估配置文件或事件属性
* 设置时间条件，以根据一天中的时间或星期几来路由用户档案
* 使用百分比拆分在路径间随机分布用户档案
* 应用配置文件上限以限制采用特定历程路径的用户档案数
* 使用受众成员资格检查作为历程路径中的条件

**术语表：**
* **条件活动**：历程活动，它根据结果&#x200B;*（产品特定）*&#x200B;评估规则并将配置文件路由到不同的路径
* **数据Source条件**：使用表达式编辑器&#x200B;*（产品特定）*&#x200B;从数据源或历程事件评估字段的条件类型
* **时间条件**：一种条件类型，用于根据&#x200B;*（产品特定）*&#x200B;的小时数、星期数或两者的组合筛选用户档案
* **百分比拆分**：使用统计Java随机机制&#x200B;*（产品特定）*&#x200B;在路径间随机分布配置文件的条件类型
* **配置文件上限**：一种条件类型，用于限制可以采用特定路径的配置文件的数量；会将其他配置文件路由到备用路径&#x200B;*（产品特定）*
* **备用路径**：当错误、超时或配置文件上限达到&#x200B;*（产品特定）*&#x200B;时，将激活备用路径

**护栏：**
* 对于配置文件存储区中具有两个以上跨设备标识的配置文件，条件评估失败
* 不包含已摄取数据的架构字段将解释为null；对于此类字段，isEmpty()和isNull()计算结果为true，这可能会导致意外行为
* 时区在历程级别而不是单个条件级别定义
* “显示其他用例的路径”选项在百分比拆分条件中不可用
* 配置文件上限默认值为1,000；在复制历程或创建新版本时，计数器会重置，但在循环历程的重复发生之间不会重置
* 对于超过10,000的上限，注入的轮廓数量为上限的1.3倍；对于低于10,000的上限，注入的轮廓数量为上限的1,000加上
* 在测试模式下不应用配置文件上限
* 简单表达式编辑器不支持时序查询（例如购买列表、过去的点击）；必须使用高级编辑器

**术语：**
* 规范名称：条件活动 — 缩写：无 — 变体：条件节点，条件步骤
* 同义词： &quot;Data Source condition&quot; = &quot;expression-based condition&quot; ；&quot;Percentage split&quot; = &quot;random split&quot;
* 请勿混淆：“百分比拆分”≠“配置文件上限”（百分比拆分随机分发所有配置文件；配置文件上限在达到计数阈值后停止路由到路径）

**常见问题解答：**
* **问：如果定义了多个路径并且配置文件满足多个条件，会发生什么情况？**  — 仅执行第一个符合条件的路径（画布上的从上到下）；路径顺序决定优先级。
* **问：我可以为不符合任何条件的配置文件添加回退路径吗？**  — 是，启用“为上述情况以外的其他情况显示路径” — 在“百分比拆分”条件中除外，在该条件中，所有用户档案始终输入其中一个拆分路径。
* **问：为什么对于希望包含数据的字段，我的isEmpty()条件计算结果为true？**  — 如果架构字段存在，但尚未为其摄取数据，则Journey Optimizer和实时客户档案会将其解释为null，因此isEmpty()和isNull()会返回true。
* **问：周期性历程是否会重置配置文件上限计数器？**  — 否，计数器不会在每次重复时重置；它仅在复制历程或创建新版本时重置。
* **问：百分比拆分在测试模式下如何工作？**  — 在测试模式下，始终选择顶部分支，而不管配置的拆分百分比如何。

+++
