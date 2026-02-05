---
solution: Journey Optimizer
product: journey optimizer
title: 创建定位维度
description: 了解如何将关系架构映射到客户配置文件
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: f842142a985481004192c88af2973787912c85b3
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 1%

---


# 配置定位维度 {#configuration}

利用&#x200B;**[!UICONTROL 协调的营销活动]**，您可以利用Adobe Experience Platform的关系架构功能，在实体级别设计和提供目标通信。 Experience Platform使用架构，以一致且可重用的方式描述数据结构。 当数据被摄取到Experience Platform中时，它会根据XDM架构进行构建。

尽管&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;的分段主要在关系架构上运行，但实际消息投放始终发生在&#x200B;**用户档案**&#x200B;级别。

在配置定位时，您可以定义两个关键方面：

* **可定位架构**

  您可以指定哪些关系架构符合定位条件。 默认情况下使用名为`Recipient`的架构，但您可以配置替代方案，如`Visitors`、`Customers`等。

  >[!IMPORTANT]
  >
  > 协调的营销活动允许对与&#x200B;**Profile**&#x200B;架构具有直接或相关关系的任何架构进行定位。 虽然它的使用主要针对1:1关系，但它也支持1:N关系，如帐户`>`收件人，只要关系路径在数据模型中正确建模即可。 这样可基于帐户级别的数据启用定位，同时仍可解析消息投放的正确用户档案身份。

* **个人资料链接**

  系统必须了解目标架构如何映射到`Profile`架构。 这是通过共享身份字段实现的 — 该字段存在于目标架构和`Profile`架构中，并配置为身份命名空间。

➡️ [在Adobe Experience Platform文档中了解有关关系架构的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## 创建定位维度 {#targeting-dimension}

首先，通过将关系架构映射到客户配置文件来设置活动编排。

1. 从&#x200B;**[!UICONTROL 管理]**，访问&#x200B;**[!UICONTROL 配置]**&#x200B;菜单并选择&#x200B;**[!UICONTROL Campaign Target Dimension]**。

   ![](assets/target-dimension-1.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;开始创建您的&#x200B;**[!UICONTROL 定向维度]**。

1. 从下拉列表中选择您[之前配置&#x200B;的架构](gs-schemas.md)。

   虽然显示所有关系架构，但只有与&#x200B;**配置文件**&#x200B;具有直接标识关系的架构才符合选择条件。 避免选择非人员架构（例如购买），并选择与用户档案直接关联的架构。

1. 选择表示要定位的实体的&#x200B;**[!UICONTROL 标识值]**。

   在此示例中，客户个人资料链接到多个订阅，每个订阅在`crmID`架构中由唯一的`Recipient`表示。 通过将&#x200B;**[!UICONTROL Target Dimension]**&#x200B;设置为使用`Recipient`架构及其`crmID`标识，您可以在订阅级别发送消息，而不是发送到主要客户个人资料，从而确保每个合同或行都会收到其自己的个性化消息。

   [在 Adobe Experience Platform 文档中了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity)。

   ![](assets/target-dimension-2.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以完成设置。 请注意，一旦创建，**[!UICONTROL Target维度]**&#x200B;便无法移除或编辑。

配置&#x200B;**[!UICONTROL 目标Dimension]**&#x200B;后，继续创建和设置您的&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。