---
solution: Journey Optimizer
product: journey optimizer
title: 使用协调活动
description: 了解如何在编排的活动中使用协调活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 7de878c316e966129e7dede37f132938d2abbdf8
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 32%

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

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建编排的营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/><br/>[启动并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[并加入](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 协调]**&#x200B;活动是一个&#x200B;**[!UICONTROL 定位]**&#x200B;活动，它允许您定义Adobe Journey Optimizer中的数据与工作表中的数据（例如从外部文件加载的数据）之间的链接。

**[!UICONTROL 扩充]**&#x200B;活动允许您向编排的活动添加其他数据，例如，通过组合来自多个源的数据或链接到临时资源。 相反，**[!UICONTROL 协调]**&#x200B;活动用于将未识别的或外部数据与数据库中的现有资源进行匹配。

**[!UICONTROL 协调]**&#x200B;要求系统中已存在相关记录。 例如，如果您导入的购买文件列出了产品、时间戳和客户信息，则产品和客户都必须已存在于数据库中才能建立链接。

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

按照以下步骤配置&#x200B;**[!UICONTROL 协调]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 协调]**&#x200B;活动添加到您的工作流。

1. 选择新的定向维度以定义您的定向对象，如收件人或订阅者。

1. 设置用于匹配传入数据与现有用户档案的字段。

1. 要使用基本字段匹配数据，请选择&#x200B;**[!UICONTROL 简单属性]**。

1. 设置匹配字段：

   * **[!UICONTROL Source]**：列出传入数据字段。

   * **[!UICONTROL 目标]**：引用选定定向维度中的字段。

   当两个值都相等时，会发生匹配，例如，按&#x200B;**[!UICONTROL 电子邮件]**&#x200B;进行匹配以标识配置文件。

   ![](../assets/workflow-reconciliation-criteria.png)

1. 要添加更多匹配规则，请单击&#x200B;**[!UICONTROL 添加规则]**。 必须满足所有条件才能进行匹配。

1. 对于更复杂的条件，请选择&#x200B;**[!UICONTROL 高级协调条件]**。 使用[查询建模器](../orchestrated-rule-builder.md)定义自定义逻辑。

1. 要筛选要协调的数据，请单击&#x200B;**[!UICONTROL 创建筛选器]**，然后在查询建模器中定义条件。

1. 默认情况下，不匹配的记录将保留在叫客过渡中并存储在工作表中。 要删除这些项，请启用&#x200B;**[!UICONTROL 保留未协调的数据]**&#x200B;选项。

## 示例 {#example-reconciliation}

此示例使用Adobe Journey Optimizer中的&#x200B;**[!UICONTROL 协调]**&#x200B;活动确保仅向可识别的客户发送电子邮件。 数据通过&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动流入，该活动针对具有以前订单的用户。 然后，**[!UICONTROL 协调]**&#x200B;活动使用email字段将此传入数据与数据库中的现有用户档案匹配。

![](../assets/workflow-reconciliation-sample-1.0.png)
