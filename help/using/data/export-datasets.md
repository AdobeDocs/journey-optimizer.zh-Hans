---
solution: Journey Optimizer
product: journey optimizer
title: 将数据集导出到云存储位置
description: 了解如何使用Adobe Experience Platform云存储目标导出数据集。
feature: Datasets
role: User
level: Beginner
keywords: 平台, 数据湖, 创建, 湖, 数据集, 用户档案
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: bb2272e6959d896fb6b3286cec2c16a545a9f671
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 6%

---

# 将数据集导出到云存储位置 {#export-datasets}

Journey Optimizer允许您与云存储位置建立实时连接，以导出数据集的内容。

通过定期导出数据，您可以确保拥有客户互动的完整和最新记录，以便随时用于报告、存档或数据分析。

## 可用的云存储目标 {#destinations}

您可以在&#x200B;**[!UICONTROL 目录]**&#x200B;选项卡中将数据集导出到6个可从&#x200B;**[!UICONTROL 目标]**&#x200B;菜单访问的云存储目标。

![](assets/dataset-export-setup.png)

有关每个目标的详细信息，请参阅Adobe Experience Platform文档：

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html?lang=zh-Hans){target="_blank"}
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html?lang=zh-Hans){target="_blank"}
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html?lang=zh-Hans){target="_blank"}
* [数据登陆区](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html?lang=zh-Hans){target="_blank"}
* [Google云存储](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html?lang=zh-Hans){target="_blank"}
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html?lang=zh-Hans){target="_blank"}。


## 先决条件 {#prerequisites}

要导出数据集，您需要下面列出的[访问控制权限](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hans#permissions){target="_blank"}。 阅读[访问控制概述](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html?lang=zh-Hans){target="_blank"}或联系您的产品管理员以获取所需的权限。

| 类别 | 权限 |
|--|--|
| 目标 | 管理和激活数据集目标 |
| 数据管理 | 查看数据集 |
| 目标 | 查看目标 |

## 导出数据集的关键步骤 {#main-steps}

将数据集导出到云存储位置的主要步骤如下：

![](assets/dataset-export-process.png)

有关每个步骤的详细信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=zh-Hans){target="_blank"}。

1. **设置您的云存储目标**。 如果您尚未这样做，请从目标目录连接到云存储目标。 请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=zh-Hans#setup){target="_blank"}以了解如何创建新的目标连接。

   <!--![](assets/dataset-export-setup.png)-->

1. **选择要导出数据集的云存储目标**。 在目标目录中，单击所需卡片上的&#x200B;**[!UICONTROL 导出数据集]**&#x200B;按钮，然后选择要使用的连接。

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >如果您使用Adobe Journey Optimizer以及实时客户档案，目标卡片将显示&#x200B;**激活**&#x200B;按钮，根据您启用的权限，允许您导出数据集并激活此目标的受众。

1. **选择要导出到选定目标的数据集**。 [了解有关可用于导出的Journey Optimizer数据集的更多信息](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **计划数据集的导出**。 指定导出应何时开始以及开始频率。

   <!--![](assets/dataset-export-schedule.png)-->

1. **检查配置结束时显示的摘要，以查看并确认导出**。

   <!--![](assets/dataset-export-review.png)-->

导出完成后，数据集的内容将根据您配置的计划存储在云存储位置。 [了解如何验证成功的数据集导出](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=zh-Hans#verify){target="_blank"}。

## 可用于导出的数据集 {#datasets}

从下表了解您可以导出哪些Journey Optimizer数据集。

| 数据集 | 描述 |
| ------- | ------- | 
| AJO密件抄送反馈事件数据集 | AJO密件抄送反馈事件数据集 |
| AJO分类数据集 | 用于从Journey Optimizer中摄取电子邮件和推送应用程序反馈事件的数据集。 通过SDK创建。 |
| AJO同意服务数据集 | 存储个人资料的同意信息。 |
| AJO电子邮件跟踪体验事件数据集 | 用于报告和受众创建的电子邮件渠道的交互日志。  |
| AJO实体数据集 | 用于存储发送给最终用户的消息的实体元数据的数据集。  |
| AJO入站活动事件数据集 | 用于交付和交互事件的Journey Optimizer Web和应用程序内渠道的数据集。 |
| AJO交互式消息配置文件数据集 | 存储为支持API触发的营销活动而创建的用户档案 |
| AJO消息反馈事件数据集 | 消息投放日志。 有关从 Journey Optimizer 执行用于报告和创建受众的所有消息投放的信息。此数据集中还记录了电子邮件 ISP 退回的反馈。 |
| AJO配置文件计数器扩展 | 保存包含counter_value和expiryDate的对象的映射，以counter_id作为键值 |
| AJO推送配置文件数据集 | 存储用户档案的推送令牌。 |
| AJO推送跟踪体验事件数据集 | 用于报表和受众创建的推送渠道的交互日志。  |
| AJO短信体验事件数据集 | 用于报告和受众创建的短信渠道的交互日志。  |
| AJO表面数据集 | 与Journey Optimizer入站表面架构相关的空数据集 |
| AoutputForUPSDataset | 包含要写回UPS的所有AO受众成员资格 |
| Audience Orchestration配置文件数据集 | 由受众组合受众的受众组合生成。 包含所有受众组合受众、其属性和扩充数据 |
| 决策对象存储库 — 活动 | 在用户界面中又称为“决策” 。 但是，这些是用户创建的对象，它们将所有的构建块放在一起，包括决策逻辑。 例如，对于特定投放位置（位置），应考虑哪些优惠（优惠收藏集），以及要对这些优惠使用什么排名方法。 |
| 决策对象存储库 — 后备优惠 | 这是用户创建的其他类型选件的存储库。 具体来说，如果他们没有查看个性化优惠的资格并且需要查看某些内容，那么他们至少将会看到后备优惠。 此数据集包含此类选件的属性 |
| 决策对象存储库 — 个性化优惠 | 这是用户创建的选件类型的存储库。 因此，此数据集包含有关此类选件的属性 |
| 决策对象存储库 — 投放位置 | 这是一个对象存储库，其中定义了需要显示选件的位置。 |
| 历程步骤事件 | 捕获从Journey Optimizer生成的要由报表等服务使用的所有历程步骤体验事件。 |
| 历程 | 元数据数据集存储历程中每个步骤的信息 |
| ODE DecisionEvents - prod decisioning | 无论我们何时根据请求做出决策，我们都会将其计为决策事件 |