---
title: 禁止列表
description: 了解抑制列表的内容、用途和包含的内容。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 3%

---

# 禁止列表 {#suppression-list}

抑制列表包含要从投放中排除的电子邮件地址，因为向这些联系人发送可能会损害您的发送信誉和投放率。

的 [!DNL Journey Optimizer] 禁止列表由您自己的环境级别管理。

它会收集在单个客户端环境中禁止所有邮件的电子邮件地址和域，即特定于与沙盒ID关联的组织ID。

## 为什么要列禁名单？ {#why-suppression-list}

为了控制其收件箱所有者收到的电子邮件并确保他们仅接收他们想要的电子邮件，互联网服务提供商(ISP)和商业垃圾邮件过滤器使用其专有算法来根据他们使用的IP地址和发送域来跟踪电子邮件发送者的整体声誉。

如果您没有收到他们的反馈（例如垃圾邮件投诉、退回等） 因此，他们会降低你的声誉。 抑制列表可帮助您响应ISP的反馈。

电子邮件地址被禁止的收件人会自动从消息投放中排除。 这样可加快投放速度，因为错误率对投放速度有显著的影响。

## 禁止名单上有什么？ {#what-s-on-suppression-list}

电子邮件地址会按如下方式添加到禁止列表：

* 全部 **硬退回** 和 **垃圾邮件投诉** 在发生一次事件后自动将相应的电子邮件地址发送到抑制列表。

* **软退回** 请勿立即向抑制列表发送电子邮件地址，但会增加错误计数。 几个 [重试](../configuration/retries.md) 然后执行，当错误计数达到阈值时，地址将添加到禁止列表。

* 您还可以 [**手动** 添加地址或域](../configuration/manage-suppression-list.md#add-addresses-and-domains) 到禁止列表。

了解有关硬退回和软退回的更多信息(位于 [此部分](#delivery-failures).

>[!NOTE]
>
>未订阅用户的地址无法发送到抑制列表，因为他们未收到来自的电子邮件 [!DNL Journey Optimizer]. 他们的选择在Experience Platform级别处理。 了解详情 [选择退出](../messages/consent.md).

对于每个地址，被抑制的基本原因和抑制类别（软、硬等） 显示在抑制列表中。 了解有关访问和管理抑制列表的更多信息，请参阅 [此部分](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>具有 **[!UICONTROL Suppressed]** 在消息发送过程中，状态将被排除。 因此，当 **历程报表** 会将这些用户档案显示为已在历程([读取区段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) ) **电子邮件报表** 将不会在 **[!UICONTROL Sent]** 量度，因为在发送电子邮件之前，这些量度会被过滤掉。
>
>了解 [实时报表](../reports/live-report.md) 和 [全局报告](../reports/global-report.md). 要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。

### 投放失败 {#delivery-failures}

投放失败时有两种类型的错误：

* **硬退回**. 硬退回表示电子邮件地址无效（即电子邮件地址不存在）。 这涉及从接收电子邮件服务器发出的退回消息，该消息明确声明地址无效。
* **软退回**. 这是针对有效电子邮件地址发生的临时电子邮件退回。

A **硬退回** 自动将电子邮件地址添加到禁止列表。

A **软退回** <!--or an **ignored** error--> 多次重试后，也会向抑制列表发送电子邮件地址。 [了解有关重试的更多信息](../configuration/retries.md)

如果您继续向这些地址发送邮件，可能会影响您的投放率，因为它告知ISP您可能没有遵循电子邮件地址列表维护最佳实践，因此可能不是值得信赖的发件人。

### 垃圾邮件投诉 {#spam-complaints}

抑制列表会收集将您的消息标记为垃圾邮件的电子邮件地址。 例如，如果某人写信给客户服务部门，请求不再从您那里接收邮件，则该人的电子邮件地址将在您的实例中被禁止，您将无法再将邮件发送到该地址。

在收件人提交垃圾邮件投诉后向收件人发送邮件可能会对您的发送信誉产生重大影响，因为这会告知ISP您可能发送不需要的电子邮件，并且可能不会监听收件人。

这可能会导致您的IP地址或发送域被阻止，如果这些地址位于禁止列表中，则可以避免出现这种情况。
