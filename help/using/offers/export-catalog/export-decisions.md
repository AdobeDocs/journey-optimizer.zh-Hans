---
title: 决策数据集
description: 此部分列出了导出数据集中用于决策的所有字段
badge: label="旧版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '1531'
ht-degree: 0%

---

# 决策数据集 {#decisions-dataset}

每次修改优惠时，都会更新自动生成的决策数据集。

![](../assets/dataset-activities.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>在[本节](../export-catalog/access-dataset.md)中了解如何访问选件库每个对象的导出数据集。

以下是可用于&#x200B;**[!UICONTROL 决策对象存储库 — 决策]**&#x200B;数据集（以前称为决策对象存储库 — 活动）中的所有字段的列表。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ 标识符

**字段：**&#x200B;_id
**标题：**&#x200B;标识符
**描述：**&#x200B;记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ 体验(_E)

**字段：**&#x200B;体验(_E)
**类型：**&#x200B;对象

+++

+++ _experience > decisioning

**字段：**&#x200B;决策
**类型：**&#x200B;对象

+++

+++ _experience > decisioning >标准

**字段：**&#x200B;条件
**标题：**&#x200B;条件
**描述：**&#x200B;定义一组决策标准，其中每个标准都包含一组约束。
**类型：**&#x200B;数组

+++

+++ _experience > decisioning >标准>描述

**字段：**&#x200B;描述
**标题：**&#x200B;描述
**描述：**&#x200B;条件描述。 它用于传达关于如何构建该标准以及它如何影响决策的可读意图。
**类型：**&#x200B;字符串

+++

+++_体验>决策>标准>选项选择

**字段：**&#x200B;选项选择
**标题：**&#x200B;选项选择
**描述：**&#x200B;选项选择定义了选项在此上下文中的有效性/适用性。
**类型：**&#x200B;对象

* 描述

  **字段：**&#x200B;描述
  **标题：**&#x200B;描述
  **描述：**&#x200B;选项选择描述。 用于传达关于如何或为什么构建此选项选择和/或什么选项将匹配的可读意图。
  **类型：**&#x200B;字符串

* 选项筛选器

  **字段：**&#x200B;筛选器
  **标题：**&#x200B;选项筛选器
  **描述：**&#x200B;对基于集合限定符（以前称为“标记”）的过滤器的引用，该过滤器使用附加的集合限定符匹配清单中的选项。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/filter 。
  **类型：**&#x200B;字符串

* 配置文件约束类型

  **字段：** optionSelectionType
  **标题：**&#x200B;配置文件约束类型
  **描述：**&#x200B;确定当前是否设置了任何约束以及如何表示约束。 它可以通过过滤器查询或通过一个或多个受众成员资格。
  **类型：**&#x200B;字符串
  **可能的值：**“无”（默认）、“directList”、“筛选器”

* 选项列表

  **字段：**&#x200B;选项
  **标题：**&#x200B;选项列表
  **描述：**&#x200B;直接指定选项而不评估筛选器查询的列表。 可以指定选项列表或选项筛选器规则。
  **类型：**&#x200B;数组

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_体验>决策>标准>投放位置

**字段：**&#x200B;投放位置
**标题：**&#x200B;放置限制
**描述：**&#x200B;位置约束说明此条件仅适用于列出的位置。 仅当目标投放位置位于`xdm:placements`列表中时才会考虑选项选择。 否则，将跳过整个决策标准。 当“xdm：placements”列表被忽略或为空时，将考虑用于任何定向投放的标准。 此处列出的版位强制实施选项选择的隐式标准。 要考虑的选项必须具有目标版面的表示形式。
**类型：**&#x200B;数组

* 投放位置标识符

  **标题：**&#x200B;位置标识符
  **描述：**&#x200B;对投放实体的引用。 该值是被引用投放位置的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
  **类型：**&#x200B;字符串

+++

+++_experience > decisioning >标准> profileConstraints

**字段：**&#x200B;配置文件约束
**标题：**&#x200B;配置文件约束
**描述：**&#x200B;在此上下文中，配置文件约束决定选项选择此时是否适用于此配置文件标识。 如果轮廓约束不需要考虑每个选项的值，即它对于选项选择中的选项是不变的，则计算为“false”的轮廓约束将取消整个选项选择。 另一方面，系统会为选件选择的每个合格选件评估将选件作为参数的配置文件约束规则。
**类型：**&#x200B;对象

+++

+++_体验>决策>标准> profileConstraints >描述

**字段：**&#x200B;描述
**标题：**&#x200B;描述
**描述：**&#x200B;配置文件约束描述。 用于传达关于如何或为何构建此配置文件限制以及/或其将包含或排除哪些选项的可读意图。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >标准> profileConstraints >资格规则

**字段：**&#x200B;合格规则
**标题：**&#x200B;资格规则
**描述：**&#x200B;对决策规则的引用，对于给定的配置文件和/或其他给定的上下文XDM对象，其计算结果为true或false。 该规则用于确定该选项是否符合给定配置文件的条件。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >标准> profileConstraints >配置文件约束类型

**字段：** profileConstraintType
**标题：**&#x200B;配置文件约束类型
**描述：**&#x200B;确定当前是否设置了任何约束以及如何表示约束。 它可以通过规则或通过一个或多个受众成员资格实现。
**类型：**&#x200B;字符串
**可能的值：**
* “无”（默认）
* “eligibilityRule”：“配置文件约束表示为单个规则，在允许约束活动之前必须评估为true。”
* “anySegments”：“用户档案约束表示为一个或多个受众，并且用户档案必须是其中至少一个受众的成员，才能进行约束操作。”
* “allSegments”：“用户档案约束表示为一个或多个受众，并且用户档案必须是所有这些受众的成员，然后才能执行约束操作。”
* “规则”：“配置文件约束表示为许多不同的规则，例如适用性、适用性、适用性，在允许约束操作之前，所有这些规则都必须评估为true。”

+++

+++ _experience > decisioning >标准> profileConstraints > segmentIdentities

**字段：** segmentIdentities
**标题：**&#x200B;区段标识符
**描述：**&#x200B;受众的标识符。
**类型：**&#x200B;数组

* 标识符

  **字段：**&#x200B;_id
  **标题：**&#x200B;标识符
  **描述：**&#x200B;受众在相关命名空间中的身份。
  **类型：**&#x200B;字符串

* 命名空间

  **字段：**&#x200B;命名空间
  **标题：**&#x200B;命名空间
  **描述：**&#x200B;与`xid`属性关联的命名空间。
  **类型：**&#x200B;对象
  **必需：**“代码”

   * 代码

     **字段：**&#x200B;代码
     **标题：**&#x200B;代码
     **描述：**&#x200B;代码是易于用户识别的命名空间标识符，可用于请求用于标识图处理的技术命名空间ID。
     **类型：**&#x200B;字符串

* 体验标识符

  **字段：** xid
  **标题：**&#x200B;体验标识符
  **描述：**&#x200B;如果存在，此值表示跨命名空间标识符，该标识符在所有命名空间中的所有命名空间范围内的标识符中是唯一的。
  **类型：**&#x200B;字符串

+++

+++_体验>决策>标准>排名

**字段：**&#x200B;排名
**标题：**&#x200B;排名详细信息
**描述：**&#x200B;排名（优先级）。 定义在决策标准上下文中如何确定\“最佳选项\”。 在满足配置文件约束的所有选定选项中，排名将决定要建议的前（或前N个）选项。
**类型：**&#x200B;对象

+++

+++_体验>决策>标准>排名>订单

**字段：**&#x200B;顺序
**标题：**&#x200B;订单评估
**描述：**&#x200B;一个或多个决策选项的相对顺序的评估。 在顺序值较低的选项上，会选择顺序值较高的选项。 用这种方法求出的值可以排序，但无法测量它们之间的距离，也不能求和或计算乘积。 中间值和模式是唯一可用于顺序数据的中心趋势指标。
**类型：**&#x200B;对象

* 评分函数

  **字段：**&#x200B;函数
  **标题：**&#x200B;评分函数
  **描述：**&#x200B;对此决策选项计算数值分数的函数的引用。 然后，决策选项将按该得分排序（排名）。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
  **类型：**&#x200B;字符串

* 订单评估类型**

  **字段：** orderEvaluationType
  **标题：**&#x200B;订单评估类型
  **描述：**&#x200B;指定使用哪种顺序评估机制、决策选项的静态优先级、为每个选项计算数值的评分函数或接收排序列表的AI模型。
  **类型：**&#x200B;字符串
  **可能的值：**“静态”、“scoringFunction”、“rankingStrategy”

* 排名策略

  **字段：**&#x200B;排名策略
  **标题：**&#x200B;排名策略
  **描述：**&#x200B;对决策选项列表进行排名的策略的引用。 决策选项将按顺序返回。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
  **类型：**&#x200B;字符串

+++

+++ _experience >决策>标准>排名>优先级

**字段：**&#x200B;优先级
**标题：**&#x200B;优先级
**描述：**&#x200B;单个决策选项相对于所有其他选项的优先级。 未给出订单函数的选项将使用此属性进行优先排序。 在优先级较低的选项之前，会先选择优先级值较高的选项。 如果两个或更多合格选项共享最高优先级值，则以统一的随机方式选择一个选项用于决策建议。
**类型：**&#x200B;整数
**最小值：** 0
**默认值：** 0

+++

+++ _experience >决策>活动结束日期和时间

**字段：** endTime
**标题：**&#x200B;活动结束日期和时间
**描述：**&#x200B;决策（以前称为活动）结束日期和结束时间。 属性具有在https://schema.org/Action上定义的schema.org的“endTime”属性的语义。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>后备选项

**字段：**&#x200B;后备
**标题：**&#x200B;后备选项
**描述：**&#x200B;对此决策上下文中决策时使用的回退选项的引用不符合任何常规选项的条件（这通常发生在应用硬约束时）。 该值是引用的回退选项的URI (@id)。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >活动名称

**字段：**&#x200B;名称
**标题：**&#x200B;活动名称
**描述：**&#x200B;在各种用户界面中显示的决策（以前称为活动）名称。
**类型：**&#x200B;字符串

+++

+++_体验>决策>活动开始日期和时间

**字段：** startTime
**标题：**&#x200B;活动开始日期和时间
**描述：**&#x200B;决策（以前称为活动）开始日期和结束时间。 属性具有在https://schema.org/Action上定义的schema.org的“startTime”属性的语义。
**类型：**&#x200B;字符串

+++

+++ _repo

**字段：**&#x200B;_repo
**类型：**&#x200B;对象

+++

+++ _repo >活动ETAG

**字段：** etag
**标题：**&#x200B;活动ETag
**描述：**&#x200B;拍摄快照时决策（以前称为活动）对象的修订版本。
**类型：**&#x200B;字符串

+++
