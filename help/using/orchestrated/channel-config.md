---
solution: Journey Optimizer
product: journey optimizer
title: 配置渠道配置
description: 了解如何配置渠道配置
version: Campaign Orchestration
source-git-commit: 2bdabace34546bd27c2e3c19a3aee3c8a3eae5f2
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# 配置渠道配置 {#channel-configuration}

在设置[Target Dimension](target-dimension.md)后，您需要配置&#x200B;**[!UICONTROL 渠道配置]**&#x200B;并定义相应的&#x200B;**[!UICONTROL 执行详细信息]**。 这允许您定义：

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

## URL跟踪参数 {#url-tracking}

配置渠道配置时，您可以定义URL跟踪参数，通过将元数据附加到跟踪链接来监控电子邮件促销活动的性能 — 用于分析和报告目的。

为此，可以使用`{{context.system.source.*}}`语法访问特定于编排的营销活动的上下文属性：

* **`context.system.source.id`**：编排的营销活动ID
* **`context.system.source.name`**：编排的营销活动名称
* **`context.system.source.versionId`**：编排的活动版本ID
* **`context.system.source.actionId`**：渠道操作节点ID
* **`context.system.source.actionName`**：渠道操作节点名称
* **`context.system.source.channel`**：渠道类型（电子邮件、短信、推送）
* **`context.system.IdentityNamespace`**：使用了身份命名空间

例如：

```
www.YourLandingURL.com?utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content={{context.system.source.actionName}}
```

在[本节](../email/url-tracking.md)中了解有关URL跟踪参数的更多信息。
