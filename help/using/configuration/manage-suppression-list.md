---
title: 管理抑制列表
description: '了解如何访问和管理Journey Optimizer抑制列表 '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: 应用程序设置
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---


# 管理抑制列表 {#manage-suppression-list}

通过[!DNL Journey Optimizer]，您可以监控历程中自动排除的所有电子邮件地址，例如：

* 无效（硬退回）或始终软退回的地址，如果您继续将这些地址包含在投放中，则这些地址可能会对您的电子邮件声誉造成不利影响。
* 针对您的某封电子邮件发出某种垃圾邮件投诉的收件人。

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

此类电子邮件地址会自动收集到Journey Optimizer **抑制列表**&#x200B;中。 在[此部分](../suppression-list.md)中了解详情。

## 访问禁止列表 {#access-suppression-list}

要访问排除的电子邮件地址的详细列表，请打开&#x200B;**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL View suppression lists]**&#x200B;链接。

![](../assets/suppression-list-link.png)

过滤器可帮助您浏览列表。

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## 抑制类别和原因 {#suppression-categories-and-reasons}

当消息未能发送到电子邮件地址时，Journey Optimizer会确定投放失败的原因，并将其与抑制类别关联。

抑制类别如下：

* **硬**:该电子邮件地址会立即发送到禁止列表。

* **软**:当错误计数达到限制阈值时，软错误会向抑制列表发送地址。[了解有关重试的更多信息](retries.md)

* **已忽略**:
   * 当有效电子邮件地址发生错误，但已知为临时（例如连接尝试失败或临时技术问题）时，一旦错误计数达到限制阈值，则会将电子邮件地址添加到禁止列表。 [了解有关重试的更多信息](retries.md)。
   * 当错误是垃圾邮件投诉的结果时，发出投诉的收件人的电子邮件地址会立即发送到抑制列表。

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>在[投放失败类型](../suppression-list.md#delivery-failures)部分中了解有关软退回和硬退回的更多信息。

对于列出的每个电子邮件地址，您还可以检查&#x200B;**[!UICONTROL Reason]**&#x200B;以排除该地址以及将其添加到禁止列表的日期/时间。

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

投放失败可能的原因有：

| 原因 | 描述 | 抑制类别 |
---------|----------|--------- |
| **[!UICONTROL Undetermined]** | 无法识别从收件人域消息传输代理(MTA)收到的退回原因。 | 已忽略 |
| **[!UICONTROL Invalid Recipient]** | 收件人无效或不存在。 | 硬 |
| **[!UICONTROL Soft Bounce]** | 消息软退件的原因不是此表中列出的软错误，例如，在通过ISP建议的允许速率发送时。 | 柔和 |
| **[!UICONTROL DNS Failure]** | 由于DNS失败而退回消息。 | 柔和 |
| **[!UICONTROL Mailbox Full]** | 由于收件人的邮箱已满，无法接受更多邮件，邮件已退回。 | 柔和 |
| **[!UICONTROL Too Large]** | 邮件已弹回，因为它对收件人而言太大。 [](retries.md) 将执行检索：您可以编辑消息大小并重新插入该大小以进行投放。 | 已忽略 |
| **[!UICONTROL Timeout]** | 消息超时，这意味着它已软退件，并达到消息重试限制（3.5天）。 | 已忽略 |
| **[!UICONTROL Admin Failure]** | 根据发送系统管理员配置的策略，消息失败。<!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | 已忽略 |
| **[!UICONTROL Generic Bounce: No RCPT]** | 无法确定消息的收件人。 | 已忽略 |
| **[!UICONTROL Generic Bounce]** | 由于未指定原因，消息失败。 | 已忽略 |
| **[!UICONTROL Mail Block]** | 接收者（即收件人MTA）阻止了该消息。 | 已忽略 |
| **[!UICONTROL Spam Block]** | 接收者阻止了来自已知垃圾邮件源的消息。 例如，它可以是发送IP块。 | 已忽略 |
| **[!UICONTROL Spam Content]** | 接收者（收件人MTA）将邮件内容作为垃圾信息阻止。 | 已忽略 |
| **[!UICONTROL Prohibited Attachment]** | 接收者阻止了该消息，因为它包含附件。 | 已忽略 |
| **[!UICONTROL Relaying Denied]** | 由于不允许中继，因此接收器阻止了该消息。 | 柔和 |
| **[!UICONTROL Auto-Reply]** | 邮件是自动回复/休假邮件。 | 已忽略 |
| **[!UICONTROL Transient Failure]** | 消息传输已暂时延迟。 | 已忽略 |
| **[!UICONTROL Challenge-Response]** | 这是一个挑战 — 响应调查。 | 柔和 |

>[!NOTE]
>
>未订阅用户未收到来自[!DNL Journey Optimizer]的电子邮件，因此其电子邮件地址无法发送到抑制列表。 他们的选择在Experience Platform级别处理。 了解有关[opting-out](../consent.md)的更多信息。

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


