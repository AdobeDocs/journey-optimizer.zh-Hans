---
title: 禁止列表
description: 了解抑制列表的内容、用途和包含的内容。
feature: 可投放性
topic: 内容管理
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 4%

---

# 抑制列表{#suppression-list}

抑制列表包含要从投放中排除的电子邮件地址，因为向这些联系人发送可能会损害您的发送信誉和投放率。

[!DNL Journey Optimizer]禁止列表在您自己的环境级别进行管理。

它会收集在单个客户端环境中禁止所有邮件的电子邮件地址和域，即特定于与沙盒ID关联的IMS组织ID。

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## 为什么要列禁名单？{#why-suppression-list}

为了控制其收件箱所有者收到的电子邮件并确保他们仅接收他们想要的电子邮件，互联网服务提供商(ISP)和商业垃圾邮件过滤器使用其专有算法来根据他们使用的IP地址和发送域来跟踪电子邮件发送者的整体声誉。

如果您没有收到他们的反馈（例如垃圾邮件投诉、退回等） 因此，他们会降低你的声誉。 抑制列表可帮助您响应ISP的反馈。

电子邮件地址被禁止的收件人会自动从消息投放中排除。 这样可加快投放速度，因为错误率对投放速度有显著的影响。

## 禁止名单上有什么？{#what-s-on-suppression-list}

电子邮件地址会按如下方式添加到禁止列表：

* 所有&#x200B;**硬退回**&#x200B;和&#x200B;**垃圾邮件投诉**&#x200B;在发生一次事件后会自动将相应的电子邮件地址发送到抑制列表。

* **软退** 件和临时 **** 忽略错误不会立即向禁止列表发送电子邮件地址，但会增加错误计数。然后执行多次重试，当错误计数达到阈值时，地址将添加到抑制列表。 了解有关[retries](configuration/retries.md)的更多信息。

<!--You can also manually add an address to the suppression list. Manual category will be available when ability to manually add an address to the suppression list (via API) is released.-->

>[!NOTE]
>
>未订阅用户的地址无法发送到抑制列表，因为他们未收到[!DNL Journey Optimizer]的电子邮件。 他们的选择在Experience Platform级别处理。 了解有关[opting-out](../using/consent.md)的更多信息。
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

对于每个地址，被抑制的基本原因和抑制类别（软、硬等） 显示在抑制列表中。 在[此部分](configuration/manage-suppression-list.md)中了解有关访问和管理抑制列表的更多信息。

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

### 投放失败{#delivery-failures}

投放的失败，可能是因为三种类型的错误：

* **硬退回**。硬退回表示电子邮件地址无效（即电子邮件地址不存在）。 这涉及从接收电子邮件服务器发出的退回消息，该消息明确声明地址无效，如“未知用户”。
* **软退回**。这是针对有效电子邮件地址发生的临时电子邮件退回。
* **已忽略**。这是为有效电子邮件地址而发生但已知为临时电子邮件退回，例如连接尝试失败、与垃圾邮件相关的临时问题（电子邮件声誉）或临时技术问题。<!--does it exist in CJM?-->

**硬退件**&#x200B;会自动将电子邮件地址添加到禁止列表。

发生过多次的&#x200B;**软退件**&#x200B;或&#x200B;**ignored**&#x200B;错误也会在多次重试后将电子邮件地址发送到抑制列表。 [了解有关重试的更多信息](configuration/retries.md)

如果您继续向这些地址发送邮件，可能会影响您的投放率，因为它告知ISP您可能没有遵循电子邮件地址列表维护最佳实践，因此可能不是值得信赖的发件人。

### 垃圾邮件投诉{#spam-complaints}

抑制列表会收集将您的消息标记为垃圾邮件的电子邮件地址。 例如，如果某人写信给客户服务部门，请求不再从您那里接收邮件，则该人的电子邮件地址将在您的实例中被禁止，您将无法再将邮件发送到该地址。

在收件人提交垃圾邮件投诉后向收件人发送邮件可能会对您的发送信誉产生重大影响，因为这会告知ISP您可能发送不需要的电子邮件，并且可能不会监听收件人。

这可能会导致您的IP地址或发送域被阻止，如果这些地址位于禁止列表中，则可以避免出现这种情况。

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
