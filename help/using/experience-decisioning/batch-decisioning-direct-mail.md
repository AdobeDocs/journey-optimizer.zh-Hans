---
title: 直邮中的批量决策
description: 使用Experience Decisioning使直邮提取文件个性化或导出决策数据以用于下游系统
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: 批量决策、直邮、决策
source-git-commit: c8d0f67628d61c05c2b062831f382156fd212e7b
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# 直邮中的批量决策 {#batch-decisioning-direct-mail}

使用批量决策，Decisioning会为每个用户档案选择一个或多个最佳决策项，并将这些结果包含在直邮提取文件中。 配置决策策略时，通过设置&#x200B;**[!UICONTROL 项目数]**，您可以为每个配置文件返回多个项目。 导出的文件可用于直接邮件个性化，也可用于将用户档案和决策属性导出到其他系统的批量用例。

直邮中的批量决策支持两个主要用例：

* **带决策的直邮** — 个性化每个收件人的实体邮件。 例如，使用资格规则和排名（优先级或公式）为每个用户档案选择最佳图像或选件。 提取文件包括用户档案数据以及您直邮提供商的选定决策项目或项目（例如，优惠图像URL）的属性。
* **批量导出下游系统** — 导出用户档案及其决策结果（例如，选件ID、属性）以用于其他系统。 您可以运行批量决策并将文件导出到您的服务器；下游工具（例如，第三方电子邮件服务提供商）会将这些数据用于其自己的营销策划或流程。

>[!NOTE]
>
>本页面重点介绍直接邮件批量决策的特定方面。 有关设置和使用直邮渠道的完整详细信息（包括文件路由、渠道配置和提取文件设置），请参阅[直邮入门](../direct-mail/get-started-direct-mail.md)和[创建直邮消息](../direct-mail/create-direct-mail.md)。

## 工作流概述 {#workflow}

1. **创建直邮营销活动或历程**：创建历程或营销活动，选择&#x200B;**[!UICONTROL 直邮]**&#x200B;操作，选择直邮配置并定义受众。

   ➡️ [了解如何创建直邮消息](../direct-mail/create-direct-mail.md)

1. **添加决策策略**：

   1. 单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以配置提取文件。
   1. 向提取文件添加列，并使用![](assets/do-no-localize/editor-icon.svg)图标打开个性化编辑器。

      ![](assets/decision-policy-dm-add.png)

   1. 导航到&#x200B;**[!UICONTROL 决策]**&#x200B;菜单以创建决策策略。 在策略配置中，如果每个配置文件需要多个决策项，请设置&#x200B;**[!UICONTROL 项数]**，然后配置选择策略和可选的回退。

      ![](assets/decision-policy-dm-create.png)

   ➡️ [了解如何在直邮中添加和配置决策策略](create-decision-policy.md#add)

1. **使用决策属性个性化直邮文件**：对于应包含决策结果的列，请打开Personalization编辑器，导航到&#x200B;**[!UICONTROL 决策策略]**，然后选择&#x200B;**[!UICONTROL 插入策略]**&#x200B;以添加决策策略的代码。

   使用返回的决策项目属性，以便所选优惠信息包含在每个用户档案的提取文件中。 当返回多个项目时，使用策略`#each`循环映射列中每个项目的属性。

   ➡️ [了解如何在邮件中使用决策策略 — 直邮选项卡](use-decision-policy.md)

1. 使用带有测试配置文件的&#x200B;**[!UICONTROL 模拟内容]**&#x200B;来预览导出的行（包括决策值）。

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [了解如何预览和测试您的内容](../content-management/preview-test.md)

1. 激活营销活动或发布历程，以生成文件（CSV或文本分隔）并将其导出到您配置的服务器。

   ➡️ [了解如何查看和激活营销活动](../campaigns/review-activate-campaign.md) | [了解如何发布历程](../building-journeys/publish-journey.md)

## 直邮+决策示例 {#example-direct-mail}

示例： fitness retailer会向每位客户发送一张个性化的明信片，其中包含十个可能的图像之一。 他们使用Decisioning为每个用户档案选取最佳图像。

1. 创建10个决策项（每个图像一个），每个决策项都具有资格规则（例如，年龄、性别）。
2. 将它们添加到收藏集，并使用排名方法创建选择策略（例如，手动优先级或公式）。
3. 在直邮营销活动或历程中，启用决策并添加使用此选择策略的决策策略。
4. 在提取文件中，添加一列，该列的数据是用于保存所选图像的决策项属性（例如，选件图像URL）。 其他列可以是全名、地址、州/省、zip文件等。
5. 在营销活动运行时，每个用户档案在导出中都会有一行是该用户档案的选定图像。 直邮提供商使用此文件生成物理邮件。

您可以将&#x200B;**[!UICONTROL 模拟内容]**&#x200B;与测试配置文件一起使用，以查看将为该配置文件导出的决策结果（例如，图像）。

## 批量导出（中间件）用例 {#example-batch-export}

某些客户使用批量决策来导出用户档案及其决策结果，以供在其他系统（例如，CRM或电子邮件服务提供商）中使用。 其流程为：

1. 如上所述配置直邮（文件路由+渠道配置）。
2. 创建直邮营销活动或历程并添加决策策略。
3. 为导出中所需的配置文件字段和决策项目属性添加列。
4. 激活营销活动。 文件将导出到您的服务器（例如，Amazon S3或SFTP）。
5. 您的下游系统检索文件，并将用户档案和决策数据用于其自己的营销策划或流程。

这支持通过直邮渠道使用Experience Decisioning批量决策用例。

## 相关文档 {#related}

* [创建直邮邮件](../direct-mail/create-direct-mail.md) — 配置提取文件并启用决策
* [创建决策策略](create-decision-policy.md#add) — 在“直邮”选项卡中添加决策策略
* [直邮配置](../direct-mail/direct-mail-configuration.md) — 文件路由和渠道配置
* [开始使用Decisioning](gs-experience-decisioning.md) — 概念和护栏
