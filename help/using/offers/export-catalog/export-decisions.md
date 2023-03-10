---
title: 决策数据集
description: 此部分列出了导出数据集中用于决策的所有字段
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 3%

---

# 决策数据集 {#decisions-dataset}

每次修改优惠时，都会更新自动生成的决策数据集。

![](../assets/dataset-activities.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>了解如何在中访问选件库每个对象的导出数据集 [本节](../export-catalog/access-dataset.md).

以下是可在该字段中使用的所有字段的列表 **[!UICONTROL 决策对象存储库 — 决策]** 数据集（以前称为决策对象存储库 — 活动）。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ 标识符

**字段：** _id
**标题：** 标识符
**描述：** 记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ _experience（体验）

**字段：** 体验(_E)
**类型：** 对象

+++

+++ 体验>决策(_E)

**字段：** 决策
**类型：** 对象

+++

+++ _experience > decisioning >标准

**字段：** 标准
**标题：** 标准
**描述：** 定义一组决策标准，其中每个标准都包含一组约束。
**类型：** 数组

+++

+++ _experience >决策>标准>描述

**字段：** 描述
**标题：** 描述
**描述：** 条件描述。 它用于传达关于如何构建该标准以及它如何影响决策的可读意图。
**类型：**&#x200B;字符串

+++

+++_体验>决策>标准>选项选择

**字段：** optionSelection
**标题：** 选项选择
**描述：** 选项选择定义了选项在此上下文中的有效性/适用性。
**类型：** 对象

* 描述

   **字段：** 描述
   **标题：** 描述
   **描述：** 选项选择说明。 它用于传达关于如何或为什么构建此选项选择和/或哪个选项将匹配的可读意图。
   **类型：**&#x200B;字符串

* 选项筛选器

   **字段：** 过滤器
   **标题：** 选项筛选器
   **描述：** 对基于集合限定词（以前称为“标记”）的过滤器的引用，该过滤器使用附加的集合限定词匹配清单中的选项。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/filter 。
   **类型：**&#x200B;字符串

* 配置文件约束类型

   **字段：** optionSelectionType
   **标题：** 配置文件约束类型
   **描述：** 确定当前是否设置了任何约束以及如何表示约束。 它可以通过过滤器查询或通过一个或多个区段成员资格实现。
   **类型：**字符串
   **可能的值：** &quot;none&quot;（默认）、&quot;directList&quot;、&quot;filter&quot;

* 选项列表

   **字段：** options
   **标题：** 选项列表
   **描述：** 直接指定选项而不评估筛选器查询的列表。 可以指定选项列表或选项过滤器规则。
   **类型：** 数组

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_体验>决策>标准>投放位置

**字段：** 投放位置
**标题：** 置入限制
**描述：** 放置约束声明此标准仅适用于列出的放置。 仅当目标投放位置位于 `xdm:placements` list是考虑的选项选择。 否则，将跳过整个决策标准。 如果省略了&quot;xdm：placements&quot;列表或该列表为空，则对任何目标投放位置都考虑该条件。 此处列出的版面会强制实施选件的隐式标准。 要考虑的选项必须具有目标版面的表示形式。
**类型：** 数组

* 投放位置标识符

   **标题：** 投放位置标识符
   **描述：** 对放置图元的参照。 该值是被引用的投放位置的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
   **类型：**&#x200B;字符串

+++

+++_体验>决策>标准> profileConstraints

**字段：** profileConstraint
**标题：** 配置文件约束
**描述：** 在此上下文中，配置文件约束决定选项选择此时是否适用于此配置文件标识。 如果轮廓约束不需要考虑每个选项的值（即，它对于选项选择中的选项具有不变性），则计算为“false”的轮廓约束将取消整个选项选择。 另一方面，系统会为选件选择的每个合格选件评估将选件作为参数的配置文件约束规则。
**类型：** 对象

+++

+++_体验>决策>标准>用户档案约束>描述

**字段：** 描述
**标题：** 描述
**描述：** 配置文件约束描述。 它用于传达关于如何或为何构建此配置文件约束以及/或它将包含或排除什么选项的人类可读意图。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >标准> profileConstraints >资格规则

**字段：** 合格规则
**标题：** 资格规则
**描述：** 对决策规则的引用，对于给定的配置文件和/或其他给定的上下文XDM对象，其计算结果为true或false。 该规则用于确定该选项是否符合给定配置文件的条件。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >标准> profileConstraints >配置文件约束类型

**字段：** profileConstraintType
**标题：** 配置文件约束类型
**描述：** 确定当前是否设置了任何约束以及如何表示约束。 它可以通过规则或通过一个或多个区段成员资格进行。
**类型：** 字符串
**可能的值：**
* “无”（默认）
* &quot;eligibilityRule&quot;：&quot;配置文件约束表示为单个规则，在允许约束活动之前必须评估为true。&quot;
* “anySegments”：“配置文件约束表示为一个或多个区段，在允许约束操作之前，配置文件必须是至少一个区段的成员。”
* “allSegments”：“配置文件约束表示为一个或多个区段，在允许约束操作之前，配置文件必须是所有这些区段的成员。”
* &quot;rules&quot;：&quot;profile constraint表示为许多不同的规则，例如适用性、适用性、适用性，在允许约束操作之前，所有这些规则都必须评估为true。&quot;

+++

+++ _experience > decisioning >标准> profileConstraints > segmentIdentities

**字段：** segmentIdentities
**标题：** 区段标识符
**描述：** 区段的标识符。
**类型：** 数组

* 标识符

   **字段：** _id
   **标题：** 标识符
   **描述：** 区段在相关命名空间中的身份。
   **类型：**&#x200B;字符串

* namespace

   **字段：** 命名空间
   **标题：** 命名空间
   **描述：** 与关联的命名空间 `xid` 属性。
   **类型：** 对象
   **必需：** &quot;code&quot;

   * 代码

      **字段：** 代码
      **标题：** 代码
      **描述：** 该代码是易于用户识别的命名空间标识符，可用于请求用于标识图处理的技术命名空间ID。
      **类型：**&#x200B;字符串

* 体验标识符

   **字段：** xid
   **标题：** 体验标识符
   **描述：** 如果存在，则此值表示跨命名空间标识符，该标识符在所有命名空间中的所有命名空间范围内的标识符中是唯一的。
   **类型：**&#x200B;字符串

+++

+++_体验>决策>标准>排名

**字段：** 排名
**标题：** 排名详细信息
**描述：** 排名（优先级）。 定义在决策标准上下文中如何确定\“最佳选项\”。 在满足配置文件约束的所有选定选项中，排名将决定要建议的前（或前N个）选项。
**类型：** 对象

+++

+++_体验>决策>标准>排名>订单

**字段：** 订购
**标题：** 订单评估
**描述：** 一个或多个决策选项的相对顺序的评估。 在顺序值较低的任意选项上，选择顺序值较高的选项。 用这种方法确定的值可以排序，但无法测量它们之间的距离，也不能求和或计算乘积。 中间值和模式是唯一可用于顺序数据的中心趋势指标。
**类型：** 对象

* 评分功能

   **字段：** 函数
   **标题：** 评分功能
   **描述：** 对此决策选项计算数值分数的函数的引用。 然后，决策选项将按该得分排序（排名）。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
   **类型：**&#x200B;字符串

* 订单评估类型**

   **字段：** orderEvaluationType
   **标题：** 订单评估类型
   **描述：** 指定使用哪种顺序评估机制、决策选项的静态优先级、为每个选项计算数值的评分函数或接收排序列表的排名策略。
   **类型：**字符串
   **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* 排名策略

   **字段：** 排名策略
   **标题：** 排名策略
   **描述：** 对决策选项列表进行排名的策略参考。 决策选项将按有序列表返回。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
   **类型：**&#x200B;字符串

+++

+++ _experience >决策>标准>排名>优先级

**字段：** 优先级
**标题：** 优先级
**描述：** 相对于所有其他选项的单个决策选项的优先级。 未给出订单函数的选项将使用此属性进行优先排序。 在优先级较低的选项之前，会先选择优先级值较高的选项。 如果两个或多个合格选项共享最高优先级值，则以统一的随机方式选择一个选项以用于决策建议。
**类型：** 整数
**最小值：** 0
**默认值：** 0

+++

+++ _experience >决策>活动结束日期和时间

**字段：** endTime
**标题：** 活动结束日期和时间
**描述：** 决策（以前称为活动）结束日期和结束时间。 属性具有在http://schema.org/Action上定义的schema.org的“endTime”属性的语义。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>后备选项

**字段：** 回退
**标题：** 后备选项
**描述：** 引用在此决策上下文中决策时使用的回退选项不符合任何常规选项的资格（这通常发生在应用硬约束时）。 该值是引用的回退选项的URI (@id)。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>活动名称

**字段：** name
**标题：** 活动名称
**描述：** 显示在各种用户界面中的决策（以前称为活动）名称。
**类型：**&#x200B;字符串

+++

+++_体验>决策>活动开始日期和时间

**字段：** startTime
**标题：** 活动开始日期和时间
**描述：** 决策（以前称为活动）开始日期和结束时间。 属性具有在http://schema.org/Action上定义的schema.org的“startTime”属性的语义。
**类型：**&#x200B;字符串

+++

+++ 存储库(_R)

**字段：** 存储库(_R)
**类型：** 对象

+++

+++ _repo >活动ETag

**字段：** etag
**标题：** 活动ETag
**描述：** 拍摄快照时决策（以前称为活动）对象所处的修订版本。
**类型：**&#x200B;字符串

+++
