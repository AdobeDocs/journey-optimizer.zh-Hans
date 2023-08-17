---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer中的数据入门
description: 了解如何在Journey Optimizer中使用数据
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 数据，管理，平台
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 数据管理入门 [!DNL Journey Optimizer] {#about-data}

最终客户数据的丰富性和覆盖范围决定了任何客户体验解决方案的实力和成功；这些数据是神圣的，对于任何给定客户而言都是最高价值的。 技术选择现在内置在对数据管理能力进行严格评估的内置。

替换为 [!DNL Adobe Journey Optimizer]中，您可以轻松管理、保留此数据，并将其导出到技术栈栈中的平台或系统。

**我的数据，我的规则** - [!DNL Adobe Journey Optimizer] 除了所有历程数据及其操作固有的数据之外，还连续（实时）创建一组丰富的客户档案数据。 从您的数据库中摄取的用户数据的草人版本可以被丰富并转换为具有覆盖范围和深度的高价值数据。 您既希望这些数据安全，又希望这些数据无处不在，以便能够在您的整个IT生态系统中利用它的价值。

从广义上讲，您希望从数据中获得的灵活性是：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="目标" src="assets/do-not-localize/dest.png" /> 
    <br>在其他目标中可用 — 同时 [!DNL Adobe Journey Optimizer] 协同和集成数据以实现超个性化的客户体验，您希望这些数据存在于您整个技术环境中的其他系统中，同时您会寻找其他方法来利用此数据。
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
    <br>根据商定的时间表或您的策略删除数据 — 数据删除是数据保护的一个关键方面，也是所有数据治理流程中的一个关键步骤。 [!DNL Adobe Journey Optimizer] 生成的数据可能多于所需数据。 此外，无论是由于实用性还是法规原因，您都希望最大限度地关注数据集在所需持续时间之后发生的情况。 您需要的控制是在任意给定时间点删除数据。 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">了解详情</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform]，其中 [!DNL Adobe Journey Optimizer] 构建，在项目期间以及项目结束时为您提供最高级别的数据控制。 范围 [!DNL Journey Optimizer]，则您可以完全控制由引入的数据， [!DNL Journey Optimizer])、覆盖到该数据的治理以及该数据发送到的目标。

所有数据都被视为客户的财产，只能应您的请求进行维护、加密、分发或销毁。 Adobe充当您的受托人，对您的数据绝对没有权限。

您可以使用 [!DNL Journey Optimizer]的数据灵活性，可满足您与数据保留、存档或删除相关的特定要求：

* **数据提取/导出**：您可以随时通过数据访问API启动源数据提取，不会受到任何处罚或延迟。 此 [数据访问API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} 为用户提供RESTful接口，该接口侧重于在中摄取的数据集的可发现性和可访问性 [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  请注意，无法通过上述API或目标方法提取历程或营销活动中使用的内容。

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **清除和归档机制**：可以在中自由定义和自动清除数据和存档 [!DNL Adobe Journey Optimizer] 自动化数据保留策略。 可以为不同的数据实体定义不同的老化策略。 还可以定义导出机制，以便在清除或存档老化数据之前自动导出该数据。

  数据卫生工作区允许您创建和监视各种数据卫生任务，包括删除消费者身份和计划数据集过期。 此工作区随Security &amp; Privacy Shield和Healthcare Shield提供。 请参阅[此页面](../privacy/data-hygiene.md)以了解详情。

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **项目终止/退出时的数据提取**：合同终止时，您的数据将从Adobe的存储空间中完全删除。 此外，您还可以在终止协议之前提取完整的配置文件提取。 此功能无需额外付费。 这可以随时完成，而不仅仅是在终止时。

上述方法由合同定义，并在数据处理协议(DPA)中详细阐述，Adobe在合同开始时与您相互一致。 Adobe应用程序，包括 [!DNL Journey Optimizer]，其设计原则是将每个客户的数据都视为该客户的专有数据资产。
