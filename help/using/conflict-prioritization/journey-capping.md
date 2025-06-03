---
title: 历程上限和仲裁
description: 了解如何为历程创建上限规则以及如何仲裁历程条目
role: User
level: Beginner
exl-id: 4c0ee178-81fb-41ae-b7f5-22da995e6fc6
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 19%

---

# 历程上限和仲裁 {#journey-capping}

历程上限可帮助您限制配置文件可注册的历程数，防止通信过载。 在Journey Optimizer中，您可以设置两种类型的上限规则：

* **条目上限**&#x200B;限制配置文件在给定时间段内的历程条目数。
* **并发上限**&#x200B;限制可同时注册用户档案的历程数。

这两种类型的历程上限都利用优先级得分来仲裁条目。

➡️ [通过观看视频了解此功能](#video)

## 创建历程频次封顶规则 {#create-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_set_concurrency_prioritization"
>title="优先级展望"
>abstract=" 如果在此指定的时段内安排了较高优先级的历程，则将禁止客户进入此历程。对于希望按先后顺序进入历程的情况，我们建议选择“每日”展望时段，并确保当天任何其他历程的优先级分数低于该历程的优先级分数。向历程提供 100 分的优先级也可确保进入该历程。"

>[!CONTEXTUALHELP]
>id="ajo_rule_set_rule_type"
>title="规则类型"
>abstract="指定规则的频次封顶类型。**[!UICONTROL 历程入口上限]**&#x200B;限制轮廓在给定时间段内进入历程的次数，同时&#x200B;**[!UICONTROL 历程并发上限]**&#x200B;限制了一个轮廓可以同时注册的行程数量。"

要创建历程上限规则，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 业务规则]**&#x200B;菜单以访问规则集清单。

1. 选择要添加上限规则的规则集，或创建新规则集：

   * 要使用现有规则集，请从列表中选择该规则集。 只能将历程上限规则添加到具有“journey”域的规则集。 您可以在&#x200B;**[!UICONTROL 域]**&#x200B;列的规则集列表中检查此信息。

     ![](assets/journey-capping-list.png)

   * 要在新规则集中创建上限规则，请单击&#x200B;**[!UICONTROL 创建规则集]**，为规则集指定唯一名称并从&#x200B;**[!UICONTROL 规则集域]**&#x200B;下拉列表中选择“历程”，然后单击&#x200B;**[!UICONTROL 保存]**。

     ![](assets/journey-capping-rule-set.png)

1. 在规则集屏幕中，单击&#x200B;**[!UICONTROL 添加规则]**&#x200B;按钮，然后为规则提供唯一名称。

1. 在&#x200B;**[!UICONTROL 规则类型]**&#x200B;下拉列表中，指定规则的上限类型。

   * **[!UICONTROL 历程进入次数上限]**：限制配置文件在给定时间段内进入历程的条目数。
   * **[!UICONTROL 历程并发上限]**：限制可同时注册用户档案的历程数。

   ![](assets/journey-capping-concurrency.png)

1. 展开以下部分以了解如何配置每种类型的上限：

   +++配置历程条目上限规则

   1. 在&#x200B;**[!UICONTROL 上限]**&#x200B;字段中，设置配置文件可以输入的最大历程数。
   1. 在&#x200B;**[!UICONTROL 持续时间]**&#x200B;字段中，定义要考虑的时间段。 请注意，持续时间基于UTC时区。 例如，每日上限将在UTC午夜重置。

   在本例中，我们希望限制用户档案在一个月内输入超过“5”个历程。

   ![](assets/journey-capping-entry-example.png)

   >[!NOTE]
   >
   >系统将考虑应用了此规则的即将计划历程的优先级。
   >
   >在本例中，如果营销人员已输入4个历程，并且本月有另一个具有较高优先级的计划历程，则将禁止客户进入较低优先级的历程。

   +++

   +++配置历程并发上限规则

   1. 在&#x200B;**[!UICONTROL 上限]**&#x200B;字段中，设置用户档案可以同时注册的最大历程数。

   1. 使用&#x200B;**[!UICONTROL 优先级预视]**&#x200B;字段根据所选时段（例如，1天、7天、30天）内的优先级分数仲裁历程条目。 如果配置文件符合多个历程的条件，这有助于优先考虑进入价值更高的历程。

   在本例中，我们希望限制已注册到包含相同规则集的另一个历程的用户档案进入历程。 如果未来7天内的另一个历程的优先级分数更高，则用户档案不会进入此历程。

   ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

   +++

1. 重复上述步骤，根据需要向规则集添加任意数量的规则。

1. 当上限规则准备好应用于历程时，激活已添加该规则的规则和规则集。 [了解如何激活规则集](../conflict-prioritization/rule-sets.md#create)

## 将频次封顶规则应用于历程 {#apply-capping}

>[!CONTEXTUALHELP]
>id="ajo_journey_capping_rule"
>title="将规则集应用于历程"
>abstract="应用规则集，根据频率上限规则将此历程排除到部分受众。"

要将上限规则应用于历程，请访问历程并打开其属性。 在&#x200B;**[!UICONTROL 上限规则]**&#x200B;下拉列表中，选择相关的规则集。 一旦激活历程，规则集中定义的上限规则将生效。

![](assets/journey-capping-apply.png)

>[!NOTE]
>
>如果立即激活历程，则系统可能需要长达10分钟才能开始抑制客户。 因此，如果您尝试发布开始时间小于10分钟的历程，则会显示一条消息。

## 监控规则集排除项 {#monitor}

一旦旅程处于活动状态，如果规则集导致在&#x200B;**[!UICONTROL 历程排除项]**&#x200B;表中从旅程中排除任何内容，则可以签入旅程报告。 “历程排除项”表包含按规则集和规则名称对排除项的详细细分，提供了有关配置文件被丢弃原因的分析。 [了解如何使用历程报告](../reports/journey-global-report-cja.md)

![](assets/journey-report.png)

此外，您还可以利用Adobe Experience Platform **查询服务**&#x200B;生成查询，以识别导致配置文件无法进入给定历程的规则。 [此节](../reports/query-examples.md#common-queries)中提供了查询示例。

## 操作说明视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3447625?quality=12&captions=chi_hans)
