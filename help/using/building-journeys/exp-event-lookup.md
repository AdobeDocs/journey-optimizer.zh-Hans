---
solution: Journey Optimizer
product: journey optimizer
title: 历程中的体验事件查找
description: 了解如何在历程中使用体验事件查找
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
source-git-commit: cee47accd4f5427f7e10015eba8b952d4e86daab
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 3%

---

# 历程中的体验事件查找 {#ee-journeys}

>[!CAUTION]
>
>从2025年7月8日开始，在新的客户组织中，历程条件中使用的表达式编辑器将不再支持使用体验事件创建表达式。 因此，[Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)中的体验事件不能用于创建表达式。 下面引用了使用体验事件创建表达式/逻辑的替代方法和最佳实践。
>
>需要更多详细信息？ [阅读常见问题解答](#faq-ee)。

本页概述可帮助您充分利用Adobe Journey Optimizer中的体验事件的常见模式和可扩展方法。 这些用例旨在帮助您解决频繁出现的挑战，例如管理选择退出、控制消息频率、根据用户行为个性化内容以及对实时信号做出反应。

利用这些策略，您可以将行为数据转化为有意义的操作 — 根据用户档案触发的事件或携带的属性禁止、限定或排除用户档案。 无论您是构建购买阈值、放弃触发器还是退回处理的逻辑，这些示例都提供了可适应您的需求的实用指南。

在评估哪种方法最合适时，请考虑用例的延迟要求以确保历程保持响应和有效。

## 选择退出抑制

要禁止已选择退出营销通信的用户档案，请使用内置的同意管理。 选择退出偏好设置会在用户档案的同意字段中自动捕获；它们可以在历程条件中直接引用，并在消息投放期间由Journey Optimizer自动实施。

了解详情：

* [管理同意](../privacy/opt-out.md)
* [电子邮件选择退出管理](../email/email-opt-out.md)
* [短信的选择退出管理](../sms/sms-opt-out.md)


## 基于退回的抑制

要排除经历过电子邮件退回的用户档案，请利用Adobe Journey Optimizer的退回地址自动禁止列表。 这种内置机制可确保将无效或不可达电子邮件从未来发送中排除，而无需自定义逻辑。

了解详情：

* [管理禁止列表](../configuration/manage-suppression-list.md)


## 常规禁止显示

要禁止显示特定行为的用户档案，请使用具有基于事件的逻辑的批量受众来捕获符合禁止标准的用户档案。 在历程条件中引用此受众。

了解详情：

* Adobe Experience Platform [区段生成器 — 事件](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [区段生成器 — 时间限制](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在条件中使用受众](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函数](../building-journeys/functions/functioninaudience.md)


## 来文收到的排除

要防止向在最近的时间范围内收到任何通信的用户档案发送消息，请执行以下操作：

* 使用具有基于时间的标准的批处理受众，并在历程条件中引用它们。
* 应用频率上限业务规则以实施每日或每周消息限制。


使用受众了解详情：

* Adobe Experience Platform [区段生成器 — 事件](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [区段生成器 — 时间限制](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在条件中使用受众](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函数](../building-journeys/functions/functioninaudience.md)


另请参阅：

* [根据渠道和通信类型设置频率上限](../conflict-prioritization/channel-capping.md)



## 特定于消息的包含/排除

要根据用户档案是否收到特定消息来包含或排除用户档案，请创建封装此逻辑并在历程条件中引用这些逻辑的批量受众。


了解详情：

* Adobe Experience Platform [区段生成器 — 事件](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [区段生成器 — 时间限制](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在条件中使用受众](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函数](../building-journeys/functions/functioninaudience.md)

## 购物车或浏览放弃个性化

要根据最新的购物车使通信个性化，或浏览多个购物车类型或产品视图中的事件，请执行以下操作：

* 如果您有权访问[Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/query/data-distiller/overview){target="_blank"}，请配置自动查询以从事件中提取所需数据，处理它以适合用例，并将其写回启用配置文件的数据集以进行激活。
* 如果可以在具有标量属性的配置文件上建模放弃数据，请考虑使用计算属性捕获最新信息，然后在历程中引用这些属性来构建通信。 [请参阅Adobe Experience Platform文档以了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## 基于行为的历程退出

要在用户档案展现特定行为时从历程中删除它们，请在收到特定事件或用户档案符合特定受众资格时，利用退出标准从历程退出用户档案。

了解详情：

* [设置历程属性 — 退出条件](journey-properties.md#exit-criteria)

## 基于购买且有价值阈值的资格鉴定

要根据购买触发历程并禁止值大于/低于阈值，请定义计算属性以汇总特定时间段的购买。 创建受众，该受众包含支出额符合特定条件的用户档案。

了解详情：

* Adobe Experience Platform [计算属性概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## 常见问题 {#faq-ee}

不再支持在历程表达式/条件中使用体验事件。 影响列于以下常见问题解答中：

+++哪些特定功能会受到影响？

只有表达式编辑器中的体验事件查找会受到影响。 以下功能&#x200B;**不受影响**，并且保持不变：

* 在配置文件UI中观察与特定配置文件关联的体验事件

* 在计算属性规则中使用体验事件并访问历程中的计算属性

* 触发具有单一或业务事件的历程

* 在表达式和个性化编辑器中使用来自触发历程的事件的历程上下文数据

* 侦听历程中的事件

* 配置事件以触发历程

* 检测最终用户对营销通信的反应事件（例如，电子邮件打开）

+++

+++此更新是否会影响我现有的Adobe组织？

仅当您尚未使用体验事件查找时，您的Adobe组织才会受到影响。 如果您已在[Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)中使用体验事件，则Adobe组织将继续支持体验事件查找。

+++

+++我拥有一家新的Adobe公司。 如何解决需要体验事件数据的用例？

上面提供了涉及体验事件的替代方法和最佳实践，以实现预期用例。

+++

+++ 如果替代方法不适用于我的用例，该怎么办？

如果您的用例无法使用上面列出的替代方法之一解决，请联系您的Adobe代表。

+++
