---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 中的数据入门
description: 了解如何在 Journey Optimizer 中处理数据
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 数据, 管理, 平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 1ed007d5921573dce30df6faa625bb0bce5d6616
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 100%

---

# 开始在 [!DNL Journey Optimizer] 中进行数据管理 {#about-data}

定义任何客户体验解决方案的强度和成功度的关键是最终客户数据的丰富性和覆盖范围；对于任何特定的客户而言，这些数据都是不容侵犯且极具价值的。现在，技术选择在本质上内置了对数据管理能力的严格评估。

借助 [!DNL Adobe Journey Optimizer]，您可以轻松管理、保留此类数据，并将其导出到技术堆栈中所包含的平台或系统。

**我的数据，我的规则** - [!DNL Adobe Journey Optimizer]除了所有历程数据及其操作所固有的优惠数据之外，还会连续（实时）创建一组丰富的客户档案数据。从数据库中摄取的草案版本的用户数据会得到丰富并转化为高价值数据，兼顾范围和深度。您既希望这类数据安全，又希望这类数据无处不在，以便能够在整个 IT 生态系统中利用其价值。

大体上，您希望从数据中获得的灵活性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目标" src="assets/do-not-localize/dest.png" /> 
    <br>在其他目标中可用 – 当 [!DNL Adobe Journey Optimizer] 协同和集成数据以获得超个性化的客户体验时，您希望在整体技术环境中的其他系统中使用这些数据，同时寻找利用这些数据的其他方法。
    <div>
     <a href="../start/ajo-integrations.md">了解详情</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="策略" src="assets/do-not-localize/policy.png" /> 
    <br>根据商定的时间表或您的策略删除数据 – 数据删除是数据保护的一个关键方面，也是所有数据治理流程中的一个关键步骤。[!DNL Adobe Journey Optimizer] 生成的数据可能超过所需数量。此外，无论是由于实用性还是法规原因，您都希望尽量关注数据集在所需持续时间之后发生的情况。您需要实现的控制是在任意给定时间点删除数据。 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">了解详情</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform]（[!DNL Adobe Journey Optimizer] 在其上构建）可在参与期间以及参与结束时为您提供最高级别的数据控制。在 [!DNL Journey Optimizer] 内，您可以完全控制数据（[!DNL Journey Optimizer] 引入或生成的那些数据）以及覆盖到这些数据的治理和这些数据被发送到的目标。

所有数据都被视为客户的财产，只能应您的请求进行维护、加密、分发或销毁。Adobe 仅充当您的受托人，对您的数据绝对没有任何权利。

您可以利用 [!DNL Journey Optimizer] 的数据灵活性，来满足与数据保留、存档或删除相关的特定要求：

* **数据提取/导出**：您可以随时通过数据访问 API 启动源数据提取，不会有任何负担或延迟。此[数据访问 API](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/data-access/api){target="_blank"} 为用户提供 RESTful 接口，该接口侧重于在 [!DNL Adobe Experience Platform] 中摄取的数据集的可发现性和可访问性。<!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  请注意，无法通过上述 API 或目标方法提取历程或营销活动中使用的内容。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除和归档机制**：可以在 [!DNL Adobe Journey Optimizer] 中自由定义和自动清除数据和存档以实现数据保留策略的自动化。可以为不同的数据实体定义不同的过期策略。还可以定义导出机制，以便在清除或存档过期数据之前自动导出该数据。

  “数据卫生”工作区允许您创建和监视各种数据卫生任务，包括删除消费者标识和计划数据集过期。此工作区随 Security &amp; Privacy Shield 和 Healthcare Shield 提供。请参阅[此页面](../privacy/data-hygiene.md)以了解详情。

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **参与终止/退出时的数据提取**：合同终止时，您的数据将被从 Adobe 的存储空间中完全移除。此外，您还可以在终止协议之前提取完整的用户档案。此功能无需额外付费。这项操作可以随时进行，而不仅仅是在终止时。

上述方法在 Adobe 与您在合作开始时达成的数据处理协议 (DPA) 中以合同形式定义并详细列出。Adobe 应用程序，包括 [!DNL Journey Optimizer]，其设计原则是将每个客户的数据都视为该客户的专有数据资产。
