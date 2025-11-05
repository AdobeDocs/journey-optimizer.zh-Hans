---
product: journey optimizer
title: inAudience函数
description: 了解Adobe Experience Platform inAudience函数
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience，受众，函数，表达式，历程，受众，分段
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: a866442aa073c648d4455754e9945f0dddfb079d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 1%

---

# inAudience函数 {#inAudience}

`inAudience`函数是一个Adobe Experience Platform函数，可用于检查旅程中的个人是否属于特定受众。 借助这项强大的功能，您可以根据受众成员资格创建个性化的历程路径，从而在客户体验中实现复杂的分段和定位。

当您需要以下操作时，请使用`inAudience`函数：

* [基于受众成员资格的分支历程路径](../condition-activity.md#using-a-segment)
* 应用取决于配置文件是否属于特定区段的条件逻辑
* 使用个性化体验定位特定的客户组
* 评估历程条件中的实时受众参与
* 合并多个受众检查以创建复杂的定位规则

此函数实时评估受众成员资格并返回一个布尔值，使其非常适用于决策节点和条件表达式。 在[Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"}中定义和管理受众(了解有关Journey Optimizer中[使用受众](../../audience/about-audiences.md)的详细信息)，表达式编辑器提供自动完成建议以帮助您准确引用受众。

**受众状态：**

受众可以有两种参与状态：

* **已实现**：该个人符合受众定义的条件，并且是活动成员
* **已退出**：个人已离开受众，不再符合条件

只有状态为&#x200B;**已实现**&#x200B;的个人才会被视为活动受众成员。 当函数返回`true`时，它确认个人已实现状态；当函数返回`false`时，它指示退出状态。 有关受众评估的详细信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hans#interpret-segment-results){target="_blank"}。

+++句法

`inAudience(<parameter>)`

+++

+++参数

| 参数 | 描述 | 类型 |
|--- |--- |--- |
| 受众 | 受众名称 | `<string>` |

**重要约束：**

* 受众名称必须为字符串常量
* 不能是字段引用或表达式
* 在一个历程中最多可检索100个受众

+++

+++签名和返回的类型

`inAudience(<string>)`

返回布尔值：
* `true`：个人是受众的成员（已实现状态）

* `false`：个人不是受众的成员（退出状态）

+++

+++示例

`inAudience("men over 50")`

如果历程实例中的个人是名为“50岁以上的男性”的Adobe Experience Platform受众的一部分，则返回&#x200B;**true**，否则返回&#x200B;**false**。

**实际用例：**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## 护栏和限制 {#guardrails}

在您的历程中使用`inAudience`函数时，请注意以下护栏和限制：

**受众检索限制：**
* 在一个历程中最多可检索100个受众
* 表达式编辑器提供自动完成的可用受众列表，以帮助您正确引用它们

**参数约束：**
* 受众名称必须为字符串常量
* 不支持将字段引用和表达式作为参数

**受众名称更改：**
* 更改Adobe Experience Platform中现有受众的名称不会自动更新历程表达式中对该受众的任何引用
* 如果条件节点使用`inAudience('oldAudienceName')`，则必须手动编辑表达式以使用新名称
* 未能更新受众名称将导致历程条件中断，并可能导致错误的历程行为

**合并策略注意事项：**
* 通过`inAudience`函数使用多个受众时，与合并策略不一致可能会导致错误或警报
* 有关合并历程行为的详细信息，请参阅[策略属性](../journey-properties.md)

## 相关主题

了解有关在Adobe Journey Optimizer中使用受众的更多信息：

* **[关于受众](../../audience/about-audiences.md)** — 了解受众在Adobe Experience Platform和Journey Optimizer中的工作方式，包括如何创建和管理受众
* **[读取受众活动](../read-audience.md)** — 使用受众触发历程条目并使所有受众成员进入历程
* **[受众资格事件](../audience-qualification-events.md)** — 侦听受众的个人资料入口和出口，以实时触发历程操作
* **[在条件中使用受众](../condition-activity.md#using-a-segment)** — 使用条件活动，根据受众成员资格创建条件历程路径
* **[历程属性 — 合并策略](../journey-properties.md)** — 了解在inAudience函数中使用多个受众时，合并策略的工作方式

