---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用 [!DNL Journey Optimizer]
description: 了解如何在 [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 开始使用 [!DNL Journey Optimizer] {#about-data}

最终客户数据的丰富性和覆盖范围决定了任何客户体验解决方案的优势和成功；并且此数据是神圣的，对任何给定客户都具有最高价值。 技术选择现在内置于内部，并对数据管理能力进行严格评估。

借助Adobe Journey Optimizer，您可以轻松管理、保留此数据并将其导出到技术堆栈中所包含的平台或系统。

**我的数据、规则** - Journey Optimizer不断（实时）创建丰富的客户用户档案数据集，以及其运营固有的所有历程数据和选件数据。 从数据库中摄取的用户数据的草图版本会得到扩充，并转化为具有覆盖范围和深度的高价值数据。 您希望此数据安全无所不在，同时无处不在，以便您能够在整个IT生态系统中利用其价值。

总的来说，您希望从数据中获得三倍的灵活性：


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <img alt="目标" src="assets/do-not-localize/dest.png" />
    <br>
  </td>
  <td>
    <div>可在其他目标中使用 — 当Journey Optimizer协同化和集成数据以提供超个性化的客户体验时，您希望在总体技术环境中的其他系统中使用此数据，同时您还希望通过其他方法来利用此数据。 <a href="../start/ajo-integrations.md">了解详情</a>&lt;</div>
    <br>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="保留" src="assets/do-not-localize/retention.png" />
  </td>
  <td>
    <div>保留的期限 — 行业或地区法规（如GDPR或CCPA）或内部数据管理政策规定了在Adobe Experience Platform数据湖中维护或存档数据的时长或时长。 <a href="../privacy/get-started-privacy.md">了解详情</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="策略" src="assets/do-not-localize/policy.png" />
    <br>
  </td>
  <td>
    <div>根据商定的时间表或您的策略删除数据 — 数据删除是数据保护的一个关键方面，也是所有数据管理流程中的一个关键步骤。 Journey Optimizer可能会生成超出要求的数据。 此外，您还希望最大限度地关注在数据集所需持续时间之后所发生的情况 — 无论是因为实用程序还是法规的原因。 您需要的控制是删除任何给定时间点的数据。</div>
  </td>
</tr>
</table>

Adobe Experience Platform是Journey Optimizer的构建基础，在参与期间以及参与结束期间为您提供最高级别的数据控制。 在Journey Optimizer中，您可以完全控制数据(即Journey Optimizer中引入或生成的数据)、覆盖到该数据的管理以及将该数据发送到的目标。

所有数据都被视为客户的属性，只能根据您的请求进行维护、加密、分发或销毁。 Adobe充当您的受信人，绝对无权访问您的数据。

您可以使用Journey Optimizer的数据灵活性来满足与数据保留、存档或删除相关的特定要求：

* **数据提取/导出**:您可以随时通过数据访问API启动源数据提取，而不会受到任何处罚或延迟。 的 [数据访问API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) 为用户提供一个RESTful界面，重点关注在Experience Platform内摄取的数据集的发现性和可访问性。 <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   请注意，无法通过上述API或目标方法提取历程或营销活动中使用的内容。

* **配置文件服务数据保留**:对于附加到任何配置文件的行为和时间系列数据，您可以选择使用Journey Optimizer的默认设置，即从其添加到配置文件之日起，或直到您选择的替代时间段，将此数据保留多达30天。 Adobe保留此数据的时间因合同而异，在组织的数据保留策略中进行了概述。

* **清除和归档机制**:在Journey Optimizer中，可以自由定义和自动清除数据和存档，以自动执行数据保留策略。 可以为不同的数据实体定义不同的老化策略。 还可以定义导出机制，以在清除或存档老化数据之前自动导出老化数据。

* **数据湖和删除**:存储在数据湖中的客户数据可以由Journey Optimizer保留：

   * 7天，以便于将客户数据载入用户档案服务，之后可永久删除或
   * 直到您选择删除

* **参与终止/退出时数据提取**:合同终止后，您的数据将从Adobe的存储空间中完全删除。 此外，您还可以在终止协议之前提取完整的用户档案提取。 此功能不需要额外付费。 这可以随时执行，而不只是在终止时执行。

上述方法由合同规定，并在数据处理协议(DPA)中详细规定，Adobe在合同开始时与您相互同意。 Adobe应用程序(包括Journey Optimizer)的设计遵循了将每个客户的数据视为该客户专有数据资产的原则。
