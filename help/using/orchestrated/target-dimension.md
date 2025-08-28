---
solution: Journey Optimizer
product: journey optimizer
title: 创建定位维度
description: 了解如何将关系架构映射到客户配置文件
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---


# 配置定位维度 {#configuration}

利用&#x200B;**[!UICONTROL 协调的营销活动]**，您可以利用Adobe Experience Platform的关系架构功能，在实体级别设计和提供目标通信。 Experience Platform使用架构，以一致且可重用的方式描述数据结构。 当数据被摄取到Experience Platform中时，它会根据XDM架构进行构建。

尽管&#x200B;**[!UICONTROL 协调的营销活动]**&#x200B;的分段主要在关系架构上运行，但实际消息投放始终发生在&#x200B;**用户档案**&#x200B;级别。

在配置定位时，您可以定义两个关键方面：

* **可定位架构**

  您可以指定哪些关系架构符合定位条件。 默认情况下使用名为`Recipient`的架构，但您可以配置替代方案，如`Visitors`、`Customers`等。

  >[!IMPORTANT]
  >
  > 目标架构必须与:1架构具有1`Profile`关系。 例如，无法使用`Purchases`作为目标架构，因为它通常表示一对多关系。

* **个人资料链接**

  系统必须了解目标架构如何映射到`Profile`架构。 这是通过共享身份字段实现的 — 该字段存在于目标架构和`Profile`架构中，并配置为身份命名空间。

## 创建定位维度 {#targeting-dimension}

首先，通过将关系架构映射到客户配置文件来设置活动编排。

1. 从&#x200B;**[!UICONTROL 管理]**，访问&#x200B;**[!UICONTROL 配置]**&#x200B;菜单并选择&#x200B;**[!UICONTROL Campaign Target Dimension]**。

   ![](assets/target-dimension-1.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;开始创建您的&#x200B;**[!UICONTROL 定向维度]**。

1. 从下拉列表中选择您[之前配置&#x200B;的架构](gs-schemas.md)。

   虽然所有关系架构均可见，但只有与&#x200B;**配置文件**&#x200B;具有直接标识关系的架构才符合选择条件。

1. 选择表示要定位的实体的&#x200B;**[!UICONTROL 标识值]**。

   在此示例中，客户个人资料链接到多个订阅，每个订阅在`crmID`架构中由唯一的`Recipient`表示。 通过将&#x200B;**[!UICONTROL Target Dimension]**&#x200B;设置为使用`Recipient`架构及其`crmID`标识，您可以在订阅级别发送消息，而不是发送到主要客户个人资料，从而确保每个合同或行都会收到其自己的个性化消息。

   [在 Adobe Experience Platform 文档中了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/schema/composition#identity)。

   ![](assets/target-dimension-2.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以完成设置。 请注意，一旦创建，**[!UICONTROL Target维度]**&#x200B;便无法移除或编辑。

配置&#x200B;**[!UICONTROL 目标Dimension]**&#x200B;后，继续创建和设置您的&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。

## 配置渠道配置 {#channel-configuration}

在设置&#x200B;**[!UICONTROL Target Dimension]**&#x200B;后，您需要配置电子邮件或短信&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。 这允许您定义：

* **邮件传递的级别**：例如，为每个收件人发送一封邮件，例如为每个人发送一封电子邮件。

* **执行地址**：用于发送的特定联系人字段，如电子邮件地址或电话号码。

要配置渠道配置，请执行以下操作：

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

1. 如果您选择了&#x200B;**[!UICONTROL Target +辅助Dimension]**&#x200B;作为投放方法，请选择&#x200B;**[!UICONTROL 辅助Dimension]**&#x200B;以定义消息投放的上下文。

1. 在&#x200B;**[!UICONTROL 执行地址]**&#x200B;部分下，选择应使用哪个&#x200B;**[!UICONTROL Source]**&#x200B;获取投放地址，如电子邮件地址或电话号码：

   * **[!UICONTROL 配置文件]**：如果投放地址（如电子邮件）直接存储在主客户配置文件中，请选择此选项。

     在将消息发送到主客户而不是特定的关联实体时非常有用。

   * **[!UICONTROL 目标Dimension]**：如果投放地址存储在主实体（例如，收件人）中，请选择此选项。

     当每个收件人都有自己的投放地址（如不同的电子邮件或电话号码）时，此变量将非常有用。

   * **[!UICONTROL 辅助Dimension]**：使用&#x200B;**[!UICONTROL Target +辅助Dimension]**&#x200B;作为投放方法时，请选择您之前配置的相关&#x200B;**[!UICONTROL 辅助Dimension]**。

     例如，如果辅助维度表示预订或订阅，则可以从该级别获取执行地址，如电子邮件。 当用户档案在预订或订阅服务时使用了不同的联系人详细信息时，这一点非常有用。

1. 从&#x200B;**[!UICONTROL 传递地址]**&#x200B;字段中，单击![编辑图标](assets/do-not-localize/edit.svg)以选择要用于邮件传递的特定字段。

   ![](assets/target-dimension-4.png)

1. 配置完毕后，单击&#x200B;**[!UICONTROL 提交]**。

您的渠道现在可以与&#x200B;**协调的营销活动**&#x200B;一起使用，将根据所选的目标维度来投放消息。
