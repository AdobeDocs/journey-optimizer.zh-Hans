---
solution: Journey Optimizer
product: journey optimizer
title: 编排的活动常见问题解答
description: 有关Journey Optimizer编排的营销活动的常见问题解答
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 8205d248d986cdc1a2262705c58524c2434265f5
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 4%

---

# 常见问题 {#faq-oc}

您将找到下面有关Adobe Journey Optimizer编排营销活动的常见问题解答。

需要更多详细信息？ 使用本页底部的反馈选项提出您的问题，或与[Adobe Journey Optimizer社区](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}建立联系。

## 什么是Campaign编排？ {#what-are-oc}

Campaign Orchestration是Journey Optimizer的一项功能，它支持单步或多步工作流，这些工作流利用关系数据存储来构建和细分受众以实现批量参与。

它为Journey Optimizer带来了新的营销活动类型：**编排的营销活动**。 编排的营销活动可帮助品牌大规模运行复杂的一对多营销活动。 它们专为品牌启动的参与而设计，例如促销活动、季节性活动或基于帐户的通信。

与单次发送/操作营销活动相比，它们为出站营销带来&#x200B;**编排和排序**：受众一起通过多步工作流程，而不是接收一次性的爆炸。

## 我可以使用编排的营销活动做什么？ {#what-can-i-do}

主要功能包括：

* **按需受众**：使用关系查询即时构建和优化目标组。
* **多实体分段**：通过连接客户数据与相关实体（例如，帐户、购买、预订）来创建精确受众。
* **发送前可见性**：在启动之前查看准确的受众计数，以优化定位。
* **多步骤工作流**：运行排序的促销活动，如季节性促销活动、产品发布或忠诚度优惠。

>[!BEGINSHADEBOX]

**最佳实践**

* 在设计工作流之前定义&#x200B;**清除营销活动目标**。
* 从&#x200B;**引导受众**&#x200B;开始，在缩放之前验证计数和逻辑。
* 使分段规则&#x200B;**尽可能简单**&#x200B;以优化性能和透明度。
* 为受众和营销活动使用&#x200B;**一致的命名约定**&#x200B;以简化管理。

>[!ENDSHADEBOX]

## 如何访问Campaign业务流程？ {#access-oc}

要访问营销活动编排，您的许可证必须包括 **Journey Optimizer – 营销活动和历程**&#x200B;或 **Journey Optimizer – 营销活动**&#x200B;包。请联系 Adobe 代表，确认您的许可证并在需要时进行更新。

在[Adobe Journey Optimizer产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}中了解有关Campaign Orchestration许可模型的更多信息。

## 支持哪些渠道？ {#channels}

您可以创建协调的营销活动以发送&#x200B;**电子邮件**、**短信**&#x200B;和&#x200B;**推送通知**。


>[!BEGINSHADEBOX]

**推荐**

* 将渠道与消息的&#x200B;**性质匹配**（例如，紧急=短信，个性化优惠=电子邮件，上下文=推送）。
* 始终在激活渠道之前验证同意和订阅首选项。
* 测试跨多个设备和客户端的消息渲染，以确保一致的体验。

>[!ENDSHADEBOX]


## 编排的营销活动与历程有何不同？ {#oc-vs-journeys}

* **协调的营销活动**：最适合&#x200B;**批次、一对多**&#x200B;营销活动。 受众按计划批量进度。
* **历程**：最适合&#x200B;**实时、一对一**&#x200B;参与。 每个客户都按照自己的速度在历程中前进，这由行为或事件触发。

>[!BEGINSHADEBOX]

**最佳实践**：将它们结合使用 — 针对已触发、反应式体验的历程，以及针对计划的、基于日历的计划而编排的营销活动。

>[!ENDSHADEBOX]

## 什么是多实体分段？ {#multi-entity}

Adobe Journey Optimizer中的Campaign Orchestration使用关系数据库。 此类型的数据模型具有通过1:1或1:many关系连接的单独的数据架构。 这使用户能够启动任何架构上的查询（不仅仅是在收件人级别），然后来回切换至其他相关架构，例如购买、产品、预订或收件人详细信息，从而极大地灵活地决定如何创建区段和受众，并且
精致。

>[!BEGINSHADEBOX]

**示例** — 定向订阅在未来30天内过期的所有收件人。 在Campaign Orchestration中，查询可以从“订阅”模式开始，仅搜索该模式的“到期日期”列，并返回所有到期的订阅，然后累计到与那些特定订阅ID相关的收件人数据，这些订阅ID会比在收件人级别开始每个查询的数据模型更快地返回结果，而且效率更高。

>[!ENDSHADEBOX]


## 数据模型的工作原理是什么？ {#data-model}

营销活动使用&#x200B;**关系数据库**。 这允许您跨不同的数据集（例如，客户、产品、订阅）进行查询，并灵活地连接它们以进行高级分段。

>[!BEGINSHADEBOX]

**最佳实践**

* 组织数据集，以便&#x200B;**关系（联接）**&#x200B;反映业务逻辑。
* 请避免不必要的连接，以保持查询性能。
* 在运行大规模提取之前验证示例结果。

>[!ENDSHADEBOX]

## 我能否使用此数据使邮件个性化？ {#personalization}

可以。在Campaign Orchestration中，可以更新称为“人员实体”的收件人配置文件以及用于个性化的数据。 此外，关系数据库中链接实体的扩充数据也可用于个性化。 您可以使用客户配置文件以及链接的数据（如购买或订阅）在所有支持的渠道间个性化内容。

>[!BEGINSHADEBOX]

**推荐**

* 使用&#x200B;**事务数据和行为数据**&#x200B;使选件相关。
* 将&#x200B;**静态属性**（例如忠诚度级别）与&#x200B;**动态属性**（例如上次购买日期）相结合。
* 保持个性化简洁 — 使用数据重载消息可能会损害可读性。

>[!ENDSHADEBOX]


## 它是否与其他Adobe解决方案集成？ {#integrations}

可以。Campaign编排与以下内容原生集成：

* **Customer Journey Analytics**：营销活动编排报告可用。
* **Real-Time CDP**：可以在Real-Time CDP中读取营销活动中构建的受众。
* **联合受众合成(FAC)**：可作为加载项使用。

## 权限和同意呢？ {#permissions}

编排的营销活动和历程的权限和同意在Adobe Experience Platform中集中管理。 在发送之前，这些设置将应用于每个收件人的两个解决方案。

>[!BEGINSHADEBOX]

**最佳实践**

* 应用&#x200B;**集中管理** — 避免在营销活动级别单独管理同意。
* 定期审核同意数据以检测不一致的情况。
* 遵守&#x200B;**特定于渠道的选择退出** — 不要假定全局同意涵盖所有渠道。

>[!ENDSHADEBOX]

## 我是否可以执行临时分段？ {#ad-hoc}

在Campaign Orchestration中，我们将临时分段称为“实时分段”，您可以实时访问关系存储中的所有可用数据，在其之上构建复杂的查询，并通过出站渠道（例如：电子邮件+短信）获得即时激活结果。

>[!BEGINSHADEBOX]

**提示**

* 对&#x200B;**时效性需求**（例如，Flash促销活动）使用临时分段。
* 保存并记录有用的查询，以便将来可在营销活动中重复使用。
* 在激活之前验证受众计数，以防止发送不足或发送过多。

>[!ENDSHADEBOX]



## 这是否支持决策？ {#decisioning}

可以。决策可以使用来自编排营销活动的关系数据。 一旦关系架构与XDM架构连接，XDM数据便可用于决策中。

## 跨环境部署如何工作？ {#deployment}

在编排的营销活动中创建的对象（例如，受众、工作流）将绑定到生成这些对象的沙盒。 跨环境（开发、暂存、生产）的标准打包和部署工作流当前不适用于编排的营销活动。

>[!BEGINSHADEBOX]

**最佳实践**

* 维护&#x200B;**个单独的沙盒**&#x200B;以用于试验、QA和生产。
* 完整记录配置以根据需要启用手动复制。
* 与治理团队保持一致，以减少环境之间的配置漂移。

>[!ENDSHADEBOX]

## 大规模运行营销活动是否有推荐的实践？ {#scale}

是，请遵循以下最佳实践：

* **围绕业务日历**（产品发布、季节性高峰期）规划营销活动，以调整数量和资源。
* 发送前使用&#x200B;**受众预览**&#x200B;确认预期的大小并避免意外情况。
* 在可能的情况下，**交错发送时间**&#x200B;以避免使下游系统（例如，呼叫中心、网站）不堪重负。
* 建立&#x200B;**监视例程** — 跟踪每次发送后的投放日志、错误率和选择退出。
* 在Customer Journey Analytics中运行&#x200B;**营销活动后分析**，以优化下一个周期的定位和编排。



>[!MORELIKETHIS]
>
>* [协调的营销活动护栏和限制](../orchestrated/guardrails.md)
>* [开始使用编排的营销活动中的架构和数据集](../orchestrated/gs-schemas.md)
>* [创建您的第一个编排的营销活动](../orchestrated/gs-campaign-creation.md)
>* [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
