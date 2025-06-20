---
solution: Journey Optimizer
product: journey optimizer
title: 使用协调活动
description: 了解如何在编排的活动中使用协调活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: b5cdffa0794b3862094d8830b13bb618d94fe97f
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 36%

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
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**协调**&#x200B;活动是一个&#x200B;**定位**&#x200B;活动，它允许您定义Adobe Journey Optimizer中的数据与工作表中的数据（例如从外部文件加载的数据）之间的链接。

**扩充**&#x200B;活动允许您向编排的活动添加其他数据，例如，通过组合来自多个源的数据或链接到临时资源。 相反，**协调**&#x200B;活动用于将未识别的或外部数据与数据库中的现有资源进行匹配。

**协调**&#x200B;要求系统中已存在相关记录。 例如，如果您导入的购买文件列出了产品、时间戳和客户信息，则产品和客户都必须已存在于数据库中才能建立链接。

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
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=zh-Hans&#targeting-dimensions" text="定位维度"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="保留未协调数据"
>abstract="默认情况下，未协调的数据保留在出站过渡中，并可在工作表中使用。要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="协调属性"
>abstract="选择用于协调数据的属性，然后单击“确认”。"

按照以下步骤配置&#x200B;**协调**&#x200B;活动：

1. 将&#x200B;**协调**&#x200B;活动添加到您的编排的活动中。

1. 选择新的定位维度。通过维度，您可以定义目标群体：收件人、应用程序订阅者、操作员、订阅者等。

1. 选择要用于协调的字段。 您可以使用一个或多个协调标准。

   1. 要使用属性协调数据，请选择&#x200B;**简单属性**&#x200B;选项。 **Source**&#x200B;字段列出了输入转换中要协调的可用字段。 **目标**&#x200B;字段对应于所选定向维度的字段。 当源和目标相等时，将协调数据。 例如，选择&#x200B;**电子邮件**&#x200B;字段，以根据用户档案的电子邮件地址删除重复的用户档案。

      要添加其他协调条件，请单击&#x200B;**添加规则**&#x200B;按钮。 如果指定了多个连接条件，则必须对所有连接条件进行验证，以便将数据链接在一起。

      ![](../assets/workflow-reconciliation-criteria.png)

   1. 要使用其他属性协调数据，请选择&#x200B;**高级协调条件**&#x200B;选项。 然后，您可以使用查询建模器创建自己的协调条件。

1. 您可以使用&#x200B;**创建筛选器**&#x200B;按钮筛选要协调的数据。 这使您可以使用查询建模器创建自定义条件。

默认情况下，未协调的数据将保留在叫客过渡中，并可在工作表中供将来使用。 要删除未协调的数据，请停用&#x200B;**保留未协调的数据**&#x200B;选项。
