---
solution: Journey Optimizer
product: journey optimizer
title: 使用“重复数据删除”活动
description: 了解如何使用“重复数据删除”活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 93%

---

# 重复数据删除 {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="用于识别重复项的字段"
>abstract="在&#x200B;**用于识别重复项的字段**&#x200B;部分中，单击&#x200B;**&#x200B;添加属性&#x200B;**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。栏位的顺序可让您指定首要处理的条件。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="删除重复项活动"
>abstract="删除&#x200B;**重复项活动可让您删除**&#x200B;入站活动结果中的重复项。主要在定位活动之后且在允许使用目标数据的活动之前使用。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="删除重复项设置"
>abstract="要删除传入数据中的重复项，请在以下字段中定义删除重复项方法。默认情况下，只会保留一条记录。您还应该根据表达式或属性选择删除重复项模式。默认情况下，要避免重复的记录是随机选择的。"


+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建精心策划的营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[精心策划活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [合并](combine.md) - <b>[重复数据删除](deduplication.md)</b> - [扩充](enrichment.md) - [分叉](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

**[!UICONTROL 重复数据删除]**&#x200B;活动是一种&#x200B;**[!UICONTROL 目标选择]**&#x200B;活动。利用此活动，您可以删除入站活动结果中的重复项，例如收件人列表中重复的轮廓。通常，在目标选择活动之后且在允许使用目标数据的活动之前进行&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;活动。

## 配置“重复数据删除”活动{#deduplication-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;活动：


1. 将&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;活动添加到精心策划的营销活动中。

1. 在&#x200B;**[!UICONTROL 用于识别重复项的字段]**&#x200B;部分中，单击&#x200B;**[!UICONTROL &#x200B;添加属性&#x200B;]**&#x200B;按钮以指定允许将相同值视为重复的字段，如电子邮件地址、名字、姓氏等。栏位的顺序可让您指定首要处理的条件。

   ![](../assets/deduplication-1.png)

1. 在&#x200B;**[!UICONTROL 重复数据删除设置]**&#x200B;部分中，使用“要保留的重复项”字段选择要保留的唯一记录数量。默认值为 1，这会为每个重复组保留一个记录。将其设置为 0 可保留所有重复项。

   例如，如果记录 A 和 B 是记录 Y 的重复项，而记录 C 是记录 Z 的重复项：

   * **如果字段的值为 1**：只保留 Y 和 Z 记录。
   * **如果字段的值为 0**：保留所有记录（A、B、C、Y、Z）。
   * **如果字段的值为 2**：保留 C 和 Z，并随机保留或根据重复数据删除方法保留 A、B 和 Y 中的两个值。

1. 选择&#x200B;**[!UICONTROL 重复数据删除方法]**，这将定义系统如何确定保留每组重复项中的哪些记录：

   * **[!UICONTROL 随机选择]**：随机选择要保留的重复项记录。
   * **[!UICONTROL 使用表达式]**：根据您定义的表达式，保留具有最高值或最低值的记录。
   * **[!UICONTROL 非空值]**：保留所选字段不为空的记录，例如，仅保留电话号码不为空的轮廓。
   * **[!UICONTROL 遵循值列表]**：优先保留一个或多个字段的特定值，例如，您可以优先保留“国家/地区”设置为“法国”的记录。单击&#x200B;**[!UICONTROL 属性]**，选择字段或创建自定义表达式。使用&#x200B;**[!UICONTROL 添加按钮]**，按优先级顺序输入首选值。

   ![](../assets/deduplication-2.png)

1. 如果您想利用剩余群体的数据，可以选中&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。补集包含所有重复项。然后，一个额外的过渡将添加到活动中。

## 示例{#deduplication-example}

在以下示例中，使用&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;活动在发送投放之前从目标受众中删除重复记录。首先，对受众进行筛选，仅包含具有非空电子邮件字段的轮廓。然后，**[!UICONTROL 重复数据删除]**&#x200B;活动使用电子邮件地址来识别和排除重复项。

![](../assets/deduplication-3.png)
