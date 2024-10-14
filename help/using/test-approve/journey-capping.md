---
title: 历程上限和仲裁
description: 了解如何为历程创建上限规则以及如何仲裁历程条目
role: User
level: Beginner
badge: label="有限发布版"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 2%

---


# 历程上限和仲裁 {#journey-capping}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [冲突管理和优先顺序入门](gs-conflict-prioritization.md)
* [检测历程和营销活动中的潜在冲突](conflicts.md)
* [为历程和营销活动分配优先级分数](priority-scores.md)
* **[历程上限和仲裁](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>目前，冲突管理和优先化工具仅以有限可用性的形式提供给选定用户。

历程上限可帮助您限制配置文件可注册的历程数，防止通信过载。 在Journey Optimizer中，您可以设置两种类型的上限规则：

* **条目上限**&#x200B;限制在给定时间段内配置文件进入历程的条目数。
* **并发上限**&#x200B;限制可同时注册用户档案的历程数。 如果配置文件在给定时间段内同时符合多个历程的条件，则此类上限利用历程的优先级分数来仲裁条目。

## 创建历程上限规则 {#create-rule}

要创建历程上限规则，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 业务规则(Beta)]**&#x200B;菜单以访问规则集清单。

1. 选择要添加上限规则的规则集，或创建新规则集：

   * 要使用现有规则集，请从列表中选择该规则集。 只能将历程上限规则添加到具有“journey”域的规则集。 您可以在&#x200B;**[!UICONTROL 域]**&#x200B;列的规则集列表中检查此信息。

     ![](assets/journey-capping-list.png)

   * 要在新规则集中创建上限规则，请单击&#x200B;**[!UICONTROL 创建规则集]**，为规则集指定唯一名称并从&#x200B;**[!UICONTROL 规则集域]**&#x200B;下拉列表中选择“历程”，然后单击&#x200B;**[!UICONTROL 保存]**。

     ![](assets/journey-capping-rule-set.png)

1. 在规则集屏幕中，单击&#x200B;**[!UICONTROL 添加规则]**&#x200B;按钮，然后根据需要配置规则：

   ![](assets/journey-capping-concurrency.png)

   * 为规则提供唯一的名称。

   * 在&#x200B;**[!UICONTROL 规则类型]**&#x200B;下拉列表中，指定规则的上限类型。

      * **[!UICONTROL 历程进入次数上限]**：限制配置文件在给定时间段内进入历程的条目数。
      * **[!UICONTROL 历程并发上限]**：限制可同时注册用户档案的历程数。

   * 展开以下部分以了解如何配置每种类型的上限：

     +++配置历程条目上限规则

      1. 在&#x200B;**[!UICONTROL 上限]**&#x200B;字段中，设置用户档案进入历程的最大次数。
      1. 在&#x200B;**[!UICONTROL 持续时间]**&#x200B;字段中，定义要考虑的时间段。

     在本例中，我们希望限制用户档案在一个月内进入此历程超过“5”次。

     ![](assets/journey-capping-entry-example.png)

+++

     +++配置历程并发上限规则

      1. 在&#x200B;**[!UICONTROL 上限]**&#x200B;字段中，设置用户档案可以同时注册的最大历程数。
      1. 使用&#x200B;**[!UICONTROL 优先级预视]**&#x200B;字段根据所选时段（例如，1天、7天、30天）内的优先级分数仲裁历程条目。 如果配置文件符合多个历程的条件，这有助于优先考虑进入价值更高的历程。

     在本例中，我们希望限制已注册到其他历程的用户档案进入历程。 如果未来7天内的另一个历程的优先级分数更高，则用户档案将进入此历程。

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. 当上限规则准备好应用于历程时，单击其名称旁边的省略号按钮以激活它。

   ![](assets/journey-capping-activate-rule.png)

1. 单击屏幕右上角“添加规则”按钮旁边的省略号按钮激活整个规则集。

   ![](assets/journey-capping-activate-rule-set.png){width="50%" zommable="yes"}

## 将上限规则应用于历程 {#apply-capping}

要将上限规则应用于历程，请访问历程并打开其属性。 在&#x200B;**[!UICONTROL 上限规则]**下拉列表中，选择相关的规则集。
一旦激活历程，规则集中定义的上限规则将生效。

![](assets/journey-capping-apply.png)
