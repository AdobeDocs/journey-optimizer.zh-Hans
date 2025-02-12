---
solution: Journey Optimizer
product: journey optimizer
title: AEM内容片段
description: 了解如何访问和管理AEM内容片段
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 2%

---

# Adobe Experience Manager 内容片段 {#aem-fragments}

通过将Adobe Experience Manager与Adobe Journey Optimizer集成，您现在可以将AEM内容片段无缝地合并到Journey Optimizer电子邮件内容中。 这种简化的连接简化了访问和利用AEM内容的流程，从而能够创建个性化的动态营销活动和历程。

要了解有关AEM内容片段的更多信息，请参阅[Experience Manager文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments)。

## 限制 {#limitations}

* 仅适用于电子邮件渠道。

* 用户当前无法切换他们连接到的AEM实例，因为每个沙盒仅限于一个实例。

* 建议限制有权发布内容片段的用户的数量，以降低电子邮件中意外错误的风险。

* 对于多语言内容，仅支持手动流程。

* 当前不支持变体。

* 您需要专门为Journey Optimizer创建标记。

+++ 了解如何创建Journey Optimizer标记

   1. 访问您的&#x200B;**Experience Manager**&#x200B;环境。

   1. 从&#x200B;**工具**&#x200B;菜单中，导航到&#x200B;**常规**&#x200B;选项卡，然后选择&#x200B;**标记**。

   1. 单击&#x200B;**创建新标记**。

   1. 确保ID遵循以下语法： `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`。

   1. 单击&#x200B;**创建**。

  您现在可以将此Journey Optimizer标记分配给您的内容片段。
+++

## 添加AEM内容片段 {#aem-add}

创建并个性化您的[AEM内容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments)后，您现在可以将其导入历程优化器促销活动或历程。

1. 使用电子邮件操作创建[Campaign](../email/create-email.md)或[历程](../email/create-email.md)后，访问电子邮件设计器以配置电子邮件内容。 [了解详情](../email/get-started-email-design.md)

1. 单击文本块内部或主题行，然后从上下文工具栏中选择&#x200B;**[!UICONTROL 添加Personalization]**。

   ![](assets/aem_campaign_2.png)

1. 从左窗格中的&#x200B;**[!UICONTROL AEM内容片段]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 打开AEM CF选择器]**。

   ![](assets/aem_campaign_3.png)

1. 从可用列表中选择一个&#x200B;**[!UICONTROL 内容片段]**&#x200B;以导入到您的Journey Optimizer内容中。

1. 单击&#x200B;**[!UICONTROL 显示筛选器]**&#x200B;以优化您的内容片段列表。

   默认情况下，内容片段过滤器预设为仅显示批准的内容。

   ![](assets/aem_campaign_4.png)

1. 选择您的&#x200B;**[!UICONTROL 内容片段]**&#x200B;后，单击&#x200B;**[!UICONTROL 选择]**&#x200B;以将其打开。

   ![](assets/aem_campaign_5.png)

1. 从&#x200B;**[!UICONTROL 内容片段]**&#x200B;中选择要添加到内容的所需字段。 您可以添加内容或复制其值。

   请注意，如果您选择复制该值，则将来对&#x200B;**[!UICONTROL 内容片段]**&#x200B;进行的任何更新将不会反映在您的营销活动或历程中。

   ![](assets/aem_campaign_6.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;并在预览中查看您的消息。 您现在可以测试和检查您的邮件内容，如[此部分](../content-management/preview.md)中所详述。

执行测试并验证内容后，即可使用[促销活动](../campaigns/review-activate-campaign.md)或[历程](../building-journeys/publishing-the-journey.md)向受众发送电子邮件。
