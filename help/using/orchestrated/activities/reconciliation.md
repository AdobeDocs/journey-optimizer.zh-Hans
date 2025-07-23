---
solution: Journey Optimizer
product: journey optimizer
title: 使用“协调”活动
description: 了解如何在精心策划的营销活动中使用“协调”活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 93%

---

# 协调 {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="协调活动"
>abstract="**协调**&#x200B;活动是一项&#x200B;**目标市场选择**&#x200B;活动，可用于定义 Adobe Journey Optimizer 与工作表中数据之间的关联。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="协调选择字段"
>abstract="协调选择字段"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="协调创建条件"
>abstract="协调创建条件"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="协调生成补集"
>abstract="协调生成补集"


+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建精心策划的营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[精心策划活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [合并](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分叉](fork.md) - <b>[协调](reconciliation.md)</b> - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

**[!UICONTROL 协调]**&#x200B;活动是一种&#x200B;**[!UICONTROL 目标选择]**&#x200B;活动，可使用它来定义 Adobe Journey Optimizer 中以及工作表中数据之间的关联，例如从外部文件加载的数据。

**[!UICONTROL 扩充]**&#x200B;活动可让您通过组合来自多个源的数据或关联到临时资源等方式，向精心策划的活动添加更多数据。相反，**[!UICONTROL 协调]**&#x200B;活动用于将未识别的数据或外部数据与数据库中的现有资源进行匹配。

**[!UICONTROL 协调]**&#x200B;要求相关记录已存在于系统中。例如，若导入列有产品、时间戳和客户信息的购买文件，则数据库中必须已经存有产品和客户数据，这样才能建立关联。

## 配置协调活动 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="定位维度"
>abstract="选择新的定位维度。通过维度可以定义目标群体：收件人、应用程序订阅者、运营商、订阅者等。默认情况下会选择当前的定位维度。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="协调规则"
>abstract="选择用于删除重复项的协调规则。若要使用属性，请选择&#x200B;**简单属性**&#x200B;选项，然后选择源字段和目标字段。若要使用查询建模器创建您自己的协调条件，请选择&#x200B;**高级协调条件**&#x200B;选项。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/campaign-web/v8/query-database/query-modeler-overview" text="使用查询建模器"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="选择定位维度"
>abstract="选择要协调的入站数据的定位维度。"
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?#targeting-dimensions" text="定位维度"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="保留未协调数据"
>abstract="默认情况下，未协调的数据保留在出站过渡中，并可在工作表中使用。要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="协调属性"
>abstract="选择用于协调数据的属性，然后单击“确认”。"

请按照以下步骤配置&#x200B;**[!UICONTROL 协调]**&#x200B;活动：

1. 向您的工作流添加一个&#x200B;**[!UICONTROL 协调]**&#x200B;活动。

1. 选择新的目标维度以定义您的目标选择对象，如收件人或订阅者。

1. 设置用于将传入数据与现有轮廓进行匹配的字段。

1. 要使用基本字段匹配数据，请选择&#x200B;**[!UICONTROL 简单属性]**。

1. 设置匹配字段：

   * **[!UICONTROL 源]**：列出传入数据字段。

   * **[!UICONTROL 目标]**：引用选定目标维度中的字段。

   当两个值都相同时即会进行匹配，例如，按&#x200B;**[!UICONTROL 电子邮件]**&#x200B;进行匹配以识别轮廓。

   ![](../assets/workflow-reconciliation-criteria.png)

1. 要添加更多匹配规则，请单击&#x200B;**[!UICONTROL 添加规则]**。必须满足所有条件才能进行匹配。

1. 对于更复杂的条件，请选择&#x200B;**[!UICONTROL 高级协调条件]**。使用[查询建模器](../orchestrated-rule-builder.md)定义自定义逻辑。

1. 要筛选需协调的数据，请单击&#x200B;**[!UICONTROL 创建筛选条件]**，然后在查询建模器中定义条件。

1. 默认情况下，未匹配的记录保留在出站过渡中并存储在工作表中。要移除它们，请启用&#x200B;**[!UICONTROL 保留未协调的数据]**&#x200B;选项。

## 示例 {#example-reconciliation}

此示例使用 Adobe Journey Optimizer 中的&#x200B;**[!UICONTROL 协调]**&#x200B;活动来确保仅向识别的客户发送电子邮件。数据通过&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动流入，该活动以先前下过订单的用户为目标。然后，**[!UICONTROL 协调]**&#x200B;活动使用电子邮件字段将此传入数据与数据库中的现有轮廓匹配。

![](../assets/workflow-reconciliation-sample-1.0.png)
