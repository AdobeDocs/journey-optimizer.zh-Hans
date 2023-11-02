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
source-git-commit: b4fda6a0bd3e633811c16ef6dc3a3171b3b350c8
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 9%

---

# 禁止列表 {#suppression-list}

禁止列表包含要从投放中排除的地址和域，因为发送给这些联系人可能会损害您的发送信誉和投放率。

此 [!DNL Journey Optimizer] 禁止列表在您自己的环境级别进行管理，即对于给定的沙盒。

它在一个客户端环境中收集所有邮件中禁止显示的电子邮件地址和域，这意味着特定于与沙盒ID关联的组织ID。

>[!NOTE]
>
>Adobe会保留已证明对参与和邮件信誉有害的已知错误地址的更新列表，并确保不会向他们发送电子邮件。 在所有 Adobe 客户共有的一个全局禁止列表中管理此列表。全局禁止列表中包含的地址和域名被隐藏起来。在投递报告中仅指示被排除的收件人数量。

此外，您还可以利用Journey Optimizer **禁止显示REST API** 使用隐藏和允许列表控制传出消息。 [了解如何使用禁止REST API](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html)

## 为什么要使用禁止列表？ {#why-suppression-list}

为了控制收件箱所有者接收的电子邮件并确保他们仅接收他们想要的邮件，Internet服务提供商(ISP)和商业垃圾邮件过滤器拥有各自的算法，以根据电子邮件发件人使用的IP地址和发送域来跟踪他们的整体信誉。

如果您不接受他们的反馈（如垃圾邮件投诉、退回等） 考虑到这一点，他们会贬低你的声誉。 禁止列表可帮助您接受ISP的反馈。

电子邮件地址被禁止的收件人会自动从消息投放中排除。 这样可加快投放速度，因为错误率对投放速度有显著的影响。

## 禁止显示列表上有什么？ {#what-s-on-suppression-list}

地址将按如下方式添加到禁止显示列表中：

* 全部 **硬退回** 和 **垃圾邮件投诉数** 在出现一次后自动将相应的地址发送到禁止列表。

* **软退回** 不要立即向禁止列表发送地址，但它们会递增错误计数器。 多个 [重试](../configuration/retries.md) 然后执行，并且当错误计数器达到阈值时，将该地址添加到禁止列表。

* 您还可以 [**手动** 添加地址或域](../configuration/manage-suppression-list.md#add-addresses-and-domains) 添加到禁止显示列表。

了解更多有关硬退回和软退回的信息 [本节](#delivery-failures).

>[!NOTE]
>
>由于未订阅用户的电子邮件地址未从接收电子邮件，因此无法将其发送到禁止列表 [!DNL Journey Optimizer]. 他们的选择在Experience Platform级别处理。 详细了解 [选择退出](../privacy/opt-out.md).

对于每个地址，被抑制的基本原因和抑制类别（软、硬等） 将在禁止显示列表中显示。 在中了解有关访问和管理禁止列表的更多信息 [本节](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>具有的配置文件 **[!UICONTROL 已隐藏]** 在消息发送过程中排除状态。 因此，尽管 **历程报表** 将显示这些用户档案已在历程中移动([读取受众](../building-journeys/read-audience.md) 和 [消息活动](../building-journeys/journeys-message.md))，则 **电子邮件报表** 不会将它们包含在中 **[!UICONTROL 已发送]** 在发送电子邮件之前过滤掉的量度。
>
>了解更多关于 [实时报告](../reports/live-report.md) 和 [全局报告](../reports/global-report.md). 要了解所有排除案例的原因，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### 投放失败 {#delivery-failures}

投放失败时有两种类型的错误：

* **硬退回**. 硬退回表示电子邮件地址无效（即不存在电子邮件地址）。 这涉及到来自接收电子邮件服务器的退回消息，该消息明确指出地址无效。
* **软退回**. 这是对有效电子邮件地址发生的临时电子邮件退回。

A **硬退回** 自动将电子邮件地址添加到禁止显示列表。

A **软退回** <!--or an **ignored** error--> 如果发生次数过多，则在多次重试后将电子邮件地址发送到禁止列表。 [了解有关重试的详细信息](../configuration/retries.md)

如果您继续发送到这些地址，可能会影响您的投放率，因为它会告知ISP您可能没有遵循电子邮件地址列表维护最佳实践，因此您可能不是值得信赖的发件人。

### 垃圾邮件投诉次数 {#spam-complaints}

禁止列表会收集将您的邮件标记为垃圾邮件的电子邮件地址。 例如，如果有人写信给客户服务，请求绝不再收到您的邮件，那么该人的电子邮件地址将在您的实例中隐藏，您将无法再发送该地址。

在收件人提交垃圾邮件投诉后将其发送给收件人可能会对您的发送信誉产生巨大影响，因为它会通知ISP您可能会发送不需要的电子邮件，并且可能不会收听收件人的意见。

这可能会导致您的IP地址或发送域被阻止，如果这些地址位于禁止列表上，则可以避免这种情况。
