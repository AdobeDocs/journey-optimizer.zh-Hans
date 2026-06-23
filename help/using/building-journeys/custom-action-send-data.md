---
solution: Journey Optimizer
product: journey optimizer
title: 将数据发送到AEP
description: 了解如何将数据发送到AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 历程，用例
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 3%

---

# 用例：创建自定义操作以将数据发送到[!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用具有用户档案上限条件的Optimize活动构建逐渐增加电子邮件量的历程，以预热您的IP并保护发件人信誉。

>[!ENDSHADEBOX]

如果您最近已移至其他电子邮件服务提供商、IP地址或电子邮件域或子域，请建立您作为发件人的声誉。 否则，可能会阻止投放或将其移至收件人的垃圾邮件文件夹。 有关指导，请参阅[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans){target="_blank"}。

要预热您的IP，您可以逐渐增加投放的数量。 阅读有关[在Journey Optimizer](../reports/deliverability.md)中优化可投放性的更多信息。

此用例的目的是创建历程以加快电子邮件投放。 要配置此历程，请执行以下步骤：

1. 创建旅程。 [了解详情](journey-gs.md)。

1. 向历程添加&#x200B;**[!UICONTROL 优化]**&#x200B;活动。 [了解详情](optimize.md)。

1. 在&#x200B;**[!UICONTROL 条件]**&#x200B;活动设置中，设置投放的最大收件人数：

   1. 在&#x200B;**[!UICONTROL 优化]**&#x200B;活动设置中，选择&#x200B;**[!UICONTROL 条件]**&#x200B;方法并将&#x200B;**[!UICONTROL 类型]**&#x200B;字段设置为&#x200B;**[!UICONTROL 配置文件上限]**。 [了解详情](conditions.md#profile_cap)。

   1. 将&#x200B;**[!UICONTROL Limit]**&#x200B;字段设置为此投放的最大收件人数。

   ![用于控制自定义操作执行卷的配置文件上限条件](assets/profile-cap-condition.png)

   您可以逐渐提高此限制，直至达到订阅者的总数。

1. 在&#x200B;**[!UICONTROL 条件]**&#x200B;活动之后，将&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动添加到名义路径。

   ![使用自定义操作历程以将数据发送到外部系统](assets/ramp-up-deliveries-message.png)

   当历程运行时，将向输入的配置文件发送消息，发送数量最多为您指定的最大配置文件数。 当达到此限制时，输入的用户档案将采用替代路径。

1. 使用您选择的活动完成历程。

在IP预热后，您可以删除此条件。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍了基于旅程的IP预热用例，该用例使用用户档案上限条件逐渐增加电子邮件投放量，以保护发件人信誉。

**意图：**

* 构建IP预热历程，逐步增加电子邮件发送量
* 配置用户档案上限条件以限制每次投放的收件人数量
* 向名义历程路径添加电子邮件操作活动
* IP预热完成后，删除配置文件上限条件

**术语表：**

* **IP预热**：从新IP地址逐渐增加电子邮件发送量以建立发件人信誉的过程&#x200B;*（产品特定）*
* **配置文件上限**： Journey Optimizer中的条件类型，用于限制可以采用特定历程路径&#x200B;*（产品特定）*&#x200B;的最大配置文件数
* **名义路径**：当满足条件时，配置文件遵循的历程的主要分支&#x200B;*（产品特定）*

**护栏：**

* 必须在“条件”活动上设置用户档案上限条件，以控制IP预热期间的投放量。
* 超出上限的轮廓将被布线到替代路径。
* 必须在IP预热完成后重新创建或修改历程，以删除上限条件。

**术语：**

* 规范名称：IP warming — 首字母缩略词：n/a — 变体：IP热身、发件人信誉热身
* 同义词：“配置文件上限”=“收件人限制条件”
* 请勿混淆：“IP预热”≠“电子邮件身份验证”（SPF/DKIM/DMARC设置是分开的）

**常见问题解答：**

* **问：为什么我需要预热我的IP？**  — 新的IP地址没有发送历史记录，因此邮箱提供商可能会阻止或垃圾邮件文件夹邮件，直到建立信誉为止。
* **问：超出配置文件上限的配置文件会发生什么情况？**  — 它们采用在Condition活动中定义的替代路径。
* **问：如何随时间增加上限？**  — 编辑Condition活动设置中的Limit字段，并逐渐将其提高到订阅者总数。
* **问：何时可以移除配置文件上限条件？**  — 当IP具有足够的发送历史记录和可投放性指标稳定后，您可以从历程中删除条件。

+++
