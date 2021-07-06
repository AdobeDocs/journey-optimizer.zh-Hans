---
title: 导出优惠目录入门
description: 此部分列出了导出数据集中用于决策的所有字段。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 3%

---

# 决策数据集 {#decisions-dataset}

每次修改选件时，都会更新自动生成的决策数据集（以前称为活动）。

![](../../assets/dataset-activities.png)

数据集中最近一次成功的批处理将显示在右侧。 数据集架构的分层视图将显示在左窗格中。

>[!NOTE]
>
>了解如何在[此部分](../export-catalog/access-dataset.md)中访问选件库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Decisions]**&#x200B;数据集（以前称为“决策对象存储库 — 活动”）中使用的所有字段的列表。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## 标识符

**字段：** _id标
**题：** 标识
**符描述：** 记录的唯一标识符。**类型：**&#x200B;字符串

## _experience（体验）

**字段：** _experience类
**型：** 对象

### _experience > decisioning

**字段：** 决策
**类型：** 对象

#### _experience > decisioning >标准

**字段：** 标准标
**题：** 标准
**描述：** 定义一组决策标准，其中每个标准都包含一组约束。**类型：** 数组

**_experience > decisioning > criteria > descriptioning**

**字段：** 描述
**标题：** 描述
**:** 条件描述。它用于传达人类可读的意图，说明如何构建此标准或为何构建此标准以及它如何影响决策。
**类型：**&#x200B;字符串

**_experience > decisioning > criteria > optionSelection**

**字段：** 选项选
**择标题：** 选项选
**择描述：** 选项选择定义了此上下文中选项的有效性/适用性。**类型：** 对象

* **描述**

   **字段：** 描述
   **标题：** 描述
   **描述：** 选项选择描述。它用于传达人类可读的意图，说明如何构建此选项选择以及/或将匹配哪个选项。
   **类型：**&#x200B;字符串

* **选项过滤器**

   **字段：** filter
   **标题：** 选项过滤器
   **描述：** 对基于标记的过滤器的引用，该过滤器使用其附加的标记匹配库存中的选项。该值是引用的决策规则的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/filter 。
   **类型：**&#x200B;字符串

* **轮廓约束类型**

   **字段：** optionSelectionType
   **标题：** 配置文件约束类型
   **描述：** 确定当前是否设置了任何约束以及约束的表示方式。可以通过过滤器查询或通过一个或多个区段成员关系进行。
   **类型：**字符串
   **可能值：** &quot;none&quot;（默认）、&quot;directList&quot;、&quot;filter&quot;

* **选项列表**

   **字段：** 选项
   **标题：** 选项列表
   **描述：** 无需评估过滤器查询即可直接指定选项的列表。可以指定选项列表或选项筛选器规则。
   **类型：** 数组

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experience > decisioning > criteria > placements**

**字段：** 版面
**标题：** 版面限制
**描述：** 版面约束声明此条件仅适用于列出的版面。仅当目标版面位于`xdm:placements`列表中时，才考虑选择选项。 否则，将跳过整个决策标准。 如果忽略“xdm:placements”列表或将其留空，则会考虑任何定位版面的条件。 此处列出的位置对选项选择施加了隐式条件。 要考虑的选项必须具有目标版面的表示形式。
**类型：** 数组

* **版面标识符**

   **标题：** 版面标识符
   **描述：** 对放置图元的引用。值是所引用版面的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
   **类型：**&#x200B;字符串

**_experience > decisioning > criteria > profileConstraints**

**字段：** profileConstraints标题：
**** 配置文件约束
**描述：** 配置文件约束决定在此上下文中某个选项是否适合此配置文件标识。如果配置文件约束不需要考虑每个选项的值，即选项选择中的选项不变，则计算为“false”的配置文件约束会取消整个选项选择。 另一方面，将为选项选择的每个限定选项评估以选项作为参数的配置文件约束规则。
**类型：** 对象

* **_experience > decisioning > criteria > profileConstraints >描述**

   **字段：** 描述
   **标题：** 描述
   **描述：** 配置文件约束描述。它用于传达人类可读的意图，说明如何构建此用户档案约束以及/或该用户档案约束将包含或排除哪个选项。
   **类型：**&#x200B;字符串

* **_experience > decisioning > criteria > profileConstraints >资格规则**

   **字段：** igilityRule
   **标题：** 资格规则
   **描述：** 对决策规则的引用，该规则对给定用户档案和/或其他给定上下文XDM对象的计算结果为true或false。该规则用于确定选项是否符合给定用户档案的条件。 该值是引用的决策规则的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
   **类型：**&#x200B;字符串

* **_experience > decisioning > criteria > profileConstraints >配置文件约束类型**

   **字段：** profileConstraintType
   **标题：** 配置文件约束类型
   **描述：** 确定当前是否设置了任何约束以及约束的表示方式。可以通过规则或通过一个或多个区段成员关系实现。
   **类型：**字符串
   **可能值：**
   * &quot;none&quot;（默认）
   * &quot;igilityRule&quot;:“配置文件约束以单个规则表示，在允许约束操作之前，必须将其计算为true。”
   * &quot;anySegments&quot;:“配置文件约束表示为一个或多个区段，且配置文件必须是其中至少一个区段的成员，才允许执行约束操作。”
   * &quot;allSegments&quot;:“配置文件约束以一个或多个区段表示，并且配置文件必须是所有区段的成员，才允许执行约束操作。”
   * &quot;rules&quot;:“用户档案约束以许多不同的规则表示，例如资格、适用性、适用性，所有规则都必须在允许约束操作之前评估为true。”

* **_experience > decisioning > criteria > profileConstraints > segmentIdentities**

   **字段：** segmentIdentities
   **标题：** 区段标识符
   **描述：** 区段的标识符。
   **类型：** 数组

   * **标识符**

      **字段：** _id
      **标题：** 标识符
      **描述：** 相关命名空间中区段的标识。
      **类型：**&#x200B;字符串

   * **namespace**

      **字段：** 命名空间
      **标题：** 命名空间
      **描述：** 与属性关联的命名 `xid` 空间。
      **类型：** 对象
      **必需：** &quot;code&quot;

      * **代码**

         **字段：** 代码
         **标题：** 代码
         **描述：** 代码是命名空间的可读标识符，可用于请求用于身份图处理的技术命名空间ID。
         **类型：**&#x200B;字符串
   * **体验标识符**

      **字段：** xid
      **标题：** 体验标识符
      **描述：** 如果存在，则此值表示跨命名空间标识符，该标识符在所有命名空间中所有命名空间范围内的标识符中都是唯一的。
      **类型：**&#x200B;字符串


**_experience > decisioning > criteria > riferiang**

**字段：** 排名
**标题：** 排名详细
**信息描述：** 排名（优先级）。定义在决策标准的上下文下如何确定\&quot;最佳选项\&quot;。 在满足用户档案约束的所有选定选项中，排名将决定要建议的前（或前N）个选项。
**类型：** 对象

* **_experience > decisioning >标准>排名>顺序**

   **字段：** 顺序
   **标题：** 订单评估
   **描述：** 评估一个或多个决策选项的相对顺序。对于具有较低序数值的任何选项，都会选择具有较高序数值的选项。 该方法确定的值可以按顺序排列，但它们之间的距离无法测量，并且既不能求和也不能计算乘积。 中值和模式是唯一可用于顺序数据的中心趋势度量。
   **类型：** 对象

   * **评分功能**

      **字段：** 函数
      **标题：** 评分函数
      **描述：** 对用于计算此决策选项的数值得分的函数的引用。然后，将根据该分数对决策选项进行排序（排名）。 此属性的值是要一次通过on选项调用的函数的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
      **类型：**&#x200B;字符串

   * **订单评估类型**

      **字段：** orderEvaluationType
      **标题：** 订单评估类型
      **描述：** 指定使用的订单评估机制、决策选项的静态优先级、用于计算每个选项的数值的评分函数或接收列表以进行排序的排名策略。
      **类型：**字符串
      **可能值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

   * **排名策略**

      **字段：** rankingStrategy
      **标题：** 排名策略
      **描述：** 对对决策选项列表进行排名的策略的引用。决策选项将在有序列表中返回。 此属性的值是要一次通过on选项调用的函数的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
      **类型：**&#x200B;字符串

* **_experience > decisioning > criteria > rifirary > priority**

   **字段：** 优先级
   **标题：** 优先级
   **描述：** 单个决策选项相对于所有其他选项的优先级。使用此属性时，将按优先顺序排列未提供订单函数的选项。 优先级值较高的选项会在优先级较低的选项之前选择。 如果两个或多个合格期权具有最高优先级值，则一个期权以统一随机方式选择并用于决策建议。
   **类型：** 整数
   **最小值：** 0
   **默认值：** 0

#### _experience > decisioning > Activity End Date and Time（活动结束日期和时间）

**字段：** 结束时间
**标题：** 活动结束日期和时间
**描述：** 决策（以前称为活动）结束日期和结束时间。该属性在http://schema.org/Action上定义了schema.org的“endTime”属性的语义。
**类型：**&#x200B;字符串

#### _experience > decisioning >回退选项

**字段：** 回退
**标题：** 回退选项
**描述：** 对回退选项的引用，该回退选项在此决策上下文中做出决策时使用，该引用不会限定任何常规选项（通常在应用硬约束时发生）。值是引用的回退选项的URI(@id)。
**类型：**&#x200B;字符串

#### _experience > decisioning >活动名称

**字段：** 名称
**标题：** 活动名称
**描述：** 在各种用户界面中显示的决策（以前称为活动）名称。**类型：**&#x200B;字符串

#### _experience > decisioning > Activity Start Date and Time

**字段：** 开始时间
**标题：** 活动开始日期和时间
**描述：** 决策（以前称为活动）开始日期和结束时间。该属性在http://schema.org/Action上定义了schema.org的“startTime”属性的语义。
**类型：**&#x200B;字符串

## _repo

**字段：** _repo
**类型：** 对象

### _repo > Activity ETag

**字段：** 标
**题：** 活动ETag
**描述：** 拍摄快照时，决策（以前称为活动）对象所在的修订版本。**类型：**&#x200B;字符串
