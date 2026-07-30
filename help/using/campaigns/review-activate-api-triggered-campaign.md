---
solution: Journey Optimizer
product: journey optimizer
title: 审查和激活API触发的营销活动
description: 了解如何查看和激活API触发的营销活动。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: 561f1215-d13d-4ffc-b6f1-396ae67774c8
TQID: https://experienceleague.adobe.com/nP10Q8F2mo1JIcRiFOPRXqlrhRCDKKdtmgFJhRDOTAU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 345
ht-degree: 4%

---

# 审查和激活API触发的营销活动 {#api-review}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;在激活营销活动之前，请查看您的API触发的营销活动配置和内容以捕获错误，这样您就能够放心地让营销活动上线并准备通过API触发。

>[!ENDSHADEBOX]

配置API触发的营销活动后，您需要查看其参数和内容才能激活它。 为此，请执行以下步骤：

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送营销活动。 [了解详情](../test-approve/gs-approval.md)

1. 在营销活动配置屏幕中，单击&#x200B;**[!UICONTROL 查看以激活]**&#x200B;以显示营销活动摘要。

   ![](assets/campaign-review.png)

1. 系统会显示营销活动配置摘要，以便您检查是否有任何参数不正确或缺失，并在必要时修改营销活动。

   如果出现错误，则无法激活营销活动。 请先解决错误，然后再继续。

   ![](assets/create-campaign-alerts.png)

1. 当营销活动在其内容中使用[决策策略](../experience-decisioning/create-decision.md)时，您可以查看每个策略的结构并直接从营销活动摘要复制技术详细信息。 [了解如何操作](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

1. 检查营销活动是否正确配置，然后单击&#x200B;**[!UICONTROL 激活]**。

1. 营销活动已激活。 其状态为&#x200B;**[!UICONTROL 实时]**，或者&#x200B;**[!UICONTROL 已计划]**（如果您输入了开始日期）。

   **[!UICONTROL 已完成]**&#x200B;状态将在营销活动3天后自动分配给营销活动，如果营销活动定期执行，则会在营销活动的结束日期分配。 [了解有关营销活动状态的更多信息](manage-campaigns.md#statuses)。

   如果未指定结束日期，则营销活动会保持&#x200B;**[!UICONTROL 实时]**&#x200B;状态。 要更改此项，您需要手动停止营销活动。 [了解如何停止营销活动](manage-campaigns.md)

1. 激活营销策划后，您可以随时通过打开它来检查其信息。 利用该摘要，可获取有关定向的用户档案以及已投放和失败操作数的统计信息。

   通过单击&#x200B;**[!UICONTROL 报告]**&#x200B;按钮，您还可以在专用报告中获取其他统计信息。 [了解详情](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)

## 后续步骤 {#next}

一旦API触发的营销活动准备就绪，您即可使用API触发其执行。 [了解详情](trigger-campaigns.md)