---
solution: Journey Optimizer
product: journey optimizer
title: 禁止列表
description: 了解如何使用禁止显示列表
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 11%

---

# 禁止列表 {#suppression-list}

禁止列表包含要从投放中排除的地址和域，因为发送给这些联系人可能会损害您的发送信誉和投放率。

[!DNL Journey Optimizer]禁止列表在您自己的环境级别（即对于给定的沙盒）进行管理。

它在一个客户端环境中收集所有邮件中禁止显示的电子邮件地址和域，这意味着特定于与沙盒ID关联的组织ID。

>[!NOTE]
>
>Adobe会保留已证明对参与和邮件信誉有害的已知错误地址的更新列表，并确保不会向他们发送电子邮件。 在所有 Adobe 客户共有的一个全局禁止列表中管理此列表。全局禁止列表中包含的地址和域名被隐藏起来。在投递报告中仅指示被排除的收件人数量。

此外，您还可以利用 Journey Optimizer **禁止 REST API** 来使用禁止和允许列表控制传出消息。[了解如何使用禁止 REST API](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## 为什么要使用禁止列表？ {#why-suppression-list}

为了控制收件箱所有者接收的电子邮件并确保他们仅接收他们想要的邮件，Internet服务提供商(ISP)和商业垃圾邮件过滤器拥有各自的算法，以根据电子邮件发件人使用的IP地址和发送域来跟踪他们的整体信誉。

如果您不接受他们的反馈（如垃圾邮件投诉、退回等） 考虑到这一点，他们会贬低你的声誉。 禁止列表可帮助您接受ISP的反馈。

电子邮件地址被禁止的收件人会自动从消息投放中排除。 这样可加快投放速度，因为错误率对投放速度有显著的影响。

## 禁止显示列表上有什么？ {#what-s-on-suppression-list}

地址将按如下方式添加到禁止显示列表中：

* 所有&#x200B;**硬退回**&#x200B;和&#x200B;**垃圾邮件投诉**&#x200B;都会在单次出现后自动将相应地址发送到禁止列表。 在[本节](#spam-complaints)中了解有关垃圾邮件投诉的更多信息。

* **软退回**&#x200B;不会立即向禁止列表发送地址，但会增加错误计数。 然后执行多次[重试](../configuration/retries.md)，当错误计数器达到阈值时，地址将添加到禁止列表。

* 您也可以&#x200B;[**手动**&#x200B;将地址或域](../configuration/manage-suppression-list.md#add-addresses-and-domains)添加到禁止显示列表。

在[本节](#delivery-failures)中了解更多有关硬退回和软退回的信息。

>[!NOTE]
>
>无法向禁止列表发送取消订阅的用户地址，因为他们未接收来自[!DNL Journey Optimizer]的电子邮件。 他们的选择在Experience Platform级别处理。 了解有关[选择退出](../privacy/opt-out.md)的更多信息。

对于每个地址，被抑制的基本原因和抑制类别（软、硬等） 将在禁止显示列表中显示。 在[本节](../configuration/manage-suppression-list.md)中了解有关访问和管理禁止显示列表的详细信息。

>[!NOTE]
>
>在邮件发送过程中排除状态为&#x200B;**[!UICONTROL Suppressed]**&#x200B;的用户档案。 因此，虽然&#x200B;**历程报告**&#x200B;会显示这些用户档案在历程中移动（[读取受众](../building-journeys/read-audience.md)和[消息活动](../building-journeys/journeys-message.md)），但&#x200B;**电子邮件报告**&#x200B;不会将它们包含在&#x200B;**[!UICONTROL 已发送]**&#x200B;指标中，因为在发送电子邮件之前已将它们过滤掉。
>
>了解有关[实时报告](../reports/live-report.md)和[Customer Journey Analytics报告](../reports/report-gs-cja.md)的更多信息。 若要了解所有排除案例的原因，您可以使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}。

### 投放失败 {#delivery-failures}

投放失败时有两种类型的错误：

* **硬退回**。 硬退回表示电子邮件地址无效（即不存在电子邮件地址）。 这涉及到来自接收电子邮件服务器的退回消息，该消息明确指出地址无效。
* **软退回**。 这是对有效电子邮件地址发生的临时电子邮件退回。

**硬退回**&#x200B;会自动将电子邮件地址添加到禁止显示列表。

多次出现的&#x200B;**软退回** <!--or an **ignored** error-->也会在多次重试后将电子邮件地址发送到禁止列表。 [了解有关重试的详细信息](../configuration/retries.md)

如果您继续发送到这些地址，可能会影响您的投放率，因为它会告知ISP您可能没有遵循电子邮件地址列表维护最佳实践，因此您可能不是值得信赖的发件人。

### 垃圾邮件投诉 {#spam-complaints}

禁止列表会收集将您的邮件标记为垃圾邮件的电子邮件地址。 例如，如果有人写信给客户服务，请求绝不再收到您的邮件，那么该人的电子邮件地址将在您的实例中隐藏，您将无法再发送该地址。

在收件人提交垃圾邮件投诉后将其发送给收件人可能会对您的发送信誉产生巨大影响，因为它会通知ISP您可能会发送不需要的电子邮件，并且可能不会收听收件人的意见。

这可能会导致您的IP地址或发送域被阻止，如果这些地址位于禁止列表上，则可以避免这种情况。

某些ISP会提供反馈循环(FBL)，当收到电子邮件的用户选择将其标记为垃圾邮件时，该循环允许自动通知电子邮件发件人。 [了解详情](deliverability.md#feedback-loops)
