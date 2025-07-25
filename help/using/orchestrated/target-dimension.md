---
solution: Journey Optimizer
product: journey optimizer
title: 创建定位维度
description: 了解如何将关系架构映射到客户配置文件
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 70d397614dc0e5b5ce94cc4221a28d47dc9b476d
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 11%

---


# 配置定位维度 {#configuration}

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[配置Target维度](target-dimension.md) | <b>[创建和计划营销活动](create-orchestrated-campaign.md)</b><br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

在许多情况下，单个客户配置文件可以链接到多个相关实体，例如订阅、服务合同或设备，每个实体具有自己的唯一标识符和通信需求。

通过&#x200B;**协调的营销活动**，您现在可以使用&#x200B;**Adobe Experience Platform的关系架构功能**&#x200B;在实体级别设计和提供目标通信。 这样，您就可以按实体而不是收件人进行分段、个性化和报告。

## 创建定位维度 {#targeting-dimension}

单个客户配置文件可以与多个相关实体（如合同、设备或订阅）关联，每个实体都有自己的唯一标识符。 通过此设置，可分别针对每个实体进行定位、划分和报告。

首先，通过将关系架构映射到客户配置文件来设置活动编排。

1. 从&#x200B;**[!UICONTROL 管理]**，访问&#x200B;**[!UICONTROL 配置]**&#x200B;菜单并选择&#x200B;**[!UICONTROL Campaign Target Dimension]**。

   ![](assets/target-dimension-1.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;开始创建您的&#x200B;**[!UICONTROL 定向维度]**。

1. 从下拉列表中选择您[之前配置&#x200B;的架构](gs-schemas.md)。

1. 选择表示要定位的实体的&#x200B;**[!UICONTROL 标识值]**。

   在此示例中，客户个人资料链接到多个订阅，每个订阅在`crmID`架构中由唯一的`Recipient`表示。 通过将&#x200B;**[!UICONTROL Target Dimension]**&#x200B;设置为使用`Recipient`架构及其`crmID`标识，您可以在订阅级别发送消息，而不是发送到主要客户个人资料，从而确保每个合同或行都会收到其自己的个性化消息。

   [在 Adobe Experience Platform 文档中了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/schema/composition#identity)。

   ![](assets/target-dimension-2.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以完成设置。

配置&#x200B;**[!UICONTROL 目标Dimension]**&#x200B;后，继续创建和设置您的&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。

## 配置渠道配置 {#channel-configuration}

在设置&#x200B;**[!UICONTROL Target Dimension]**&#x200B;后，您需要配置电子邮件或短信&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。 这可以确保使用正确的标识和定向逻辑发送消息。

1. 首先创建和配置您的&#x200B;**[!UICONTROL 渠道配置]**。

   您还可以更新现有的&#x200B;**[!UICONTROL 渠道配置]**。

   ➡️ [按照此页面中详述的步骤操作](../email/surface-personalization.md)

1. 从&#x200B;**[!UICONTROL 渠道配置]**&#x200B;的&#x200B;**[!UICONTROL 执行详细信息]**&#x200B;部分，访问&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;选项卡。

   ![](assets/target-dimension-3.png)

1. 单击&#x200B;**[!UICONTROL 已启用]**&#x200B;以使其与编排的营销活动兼容。

1. 选择您的交付方式：

   * **[!UICONTROL 定位Dimension]**：发送给主要实体，例如recipient。

   * **[!UICONTROL 目标+辅助Dimension]**：使用主要实体和辅助实体发送，例如，收件人+合同。

1. 从下拉菜单中选择您之前创建的[目标Dimension](#targeting-dimension)。

   ![](assets/target-dimension-4.png)

1. 在&#x200B;**[!UICONTROL 执行地址]**&#x200B;部分下，选择应使用哪个&#x200B;**[!UICONTROL Source]**&#x200B;获取投放地址，如电子邮件地址或电话号码：

   * **[!UICONTROL 配置文件]**：如果投放地址（如电子邮件）直接存储在主客户配置文件中，请选择此选项。

     在将消息发送到主客户而不是特定的关联实体时非常有用。

   * **[!UICONTROL 目标Dimension]**：如果投放地址存储在相关实体（例如，收件人或订阅）中，请选择此选项。

     当每个收件人都有自己的投放地址（如不同的电子邮件或电话号码）时，此变量将非常有用。

1. 从&#x200B;**[!UICONTROL 传递地址]**&#x200B;字段中，单击![编辑图标](assets/do-not-localize/edit.svg)以选择要用于邮件传递的特定字段。

   ![](assets/target-dimension-4.png)

1. 配置完毕后，单击&#x200B;**[!UICONTROL 提交]**。

您的渠道现已准备好与编排的营销活动结合使用，将根据所选的目标维度投放消息。
