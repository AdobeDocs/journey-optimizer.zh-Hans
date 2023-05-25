---
solution: Journey Optimizer
product: journey optimizer
title: 管理选择退出机制
description: 了解如何管理选择退出机制和隐私
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 43%

---

# 管理选择退出机制 {#consent}

向收件人提供取消订阅以停止从品牌接收通信的功能是一项法律要求，同时确保遵循此选择。 在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hans#regulations){target="_blank"}中进一步了解适用的法规。

**为什么这很重要？**

* 未能遵守这些法规会为您的品牌带来法律监管风险。
* 它有助于避免向收件人发送未经请求的通信，这种通信可能会使他们将您的消息标记为垃圾邮件并损害您的声誉。

## 管理历程和营销活动中的退订 {#opt-out-ajo}

在从历程或活动发送消息时，必须始终确保客户可以取消订阅未来的通信。取消订阅后，用户档案将自动从未来营销消息的受众中删除。

虽然 **[!DNL Journey Optimizer]** 提供了在电子邮件和短信消息中管理选择退出的方法，但推送通知不需要您采取任何操作，因为收件人可以通过其设备自行取消订阅。例如，在下载或使用应用程序时，用户可以选择停止发送通知。同样，他们可以通过移动操作系统更改通知设置。

要了解如何在 Journey Optimizer 电子邮件和短信消息中管理选择退出，请参阅以下部分：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="潜在客户" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>电子邮件选择退出管理</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="不频繁" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>短信选择退出管理</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>在 [!DNL Journey Optimizer] 中，同意由 Experience Platform [同意模式](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hans){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=zh-Hans#choice-values){target="_blank"}处理。

## 实施个性化同意 {#opt-out-personalization}

您的客户还可以选择不向展示个性化内容。 一旦用户档案选择退出个性化，您需要确保其数据不被用于个性化，并且您必须使用回退变体替换任何个性化内容。

### 在决策管理中

利用优惠时，个性化首选项不会自动在中实施 [决策范围](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) 使用自 [决策](../offers/api-reference/offer-delivery-api/decisioning-api.md) API请求或 [边缘决策](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) api请求。 在这种情况下，您需要手动强制执行个性化同意。 为此，请执行以下步骤。

>[!NOTE]
>
>中使用的决策范围 [!DNL Journey Optimizer] 创作渠道从它们所属的历程或营销活动中满足此要求。



1. 创建 [Adobe Experience Platform区段](../segment/about-segments.md) 使用配置文件属性，例如： *&quot;同意个性化= True&quot;* 定位同意个性化的用户。

1. 创建时 [决策](../offers/offer-activities/create-offer-activities.md)，添加决策范围，并根据此区段为包含个性化优惠的每个评估标准集合定义资格约束。

1. 创建 [后备优惠](../offers/offer-library/creating-fallback-offers.md) 不包括个性化内容。

1. [分配](../offers/offer-activities/create-offer-activities.md#add-fallback) 决策的非个性化后备优惠。

1. [查看并保存](../offers/offer-activities/create-offer-activities.md#review) 决定。

如果用户具有：

* 同意进行个性化，决策范围将确定适用于该配置文件的最佳选件。

* 未经同意进行个性化，则相应的用户档案将不符合评估标准中的任何选件的条件，因此将收到非个性化的后备选件。

>[!NOTE]
>
>同意在中使用配置文件数据 [数据建模](../offers/ranking/ai-models.md) 尚不支持 [!DNL Journey Optimizer].

