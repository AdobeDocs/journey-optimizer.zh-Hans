---
solution: Journey Optimizer
product: journey optimizer
title: 管理选择退出
description: 了解如何管理选择禁用和隐私
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# 管理选择退出 {#consent}

## 关于选择退出管理 {#about}

法律规定，向收件人提供从品牌接收通信的取消订阅功能。 详细了解 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}。

**为什么这很重要？**

* 未能遵守这些法规会为您的品牌带来法律风险。
* 它有助于您避免向收件人发送未经请求的通信，这可能会使收件人将您的消息标记为垃圾邮件并损害您的声誉。

## Journey Optimizer中的选择退出管理 {#opt-out-ajo}

在从历程或营销活动发送消息时，必须始终确保客户可以取消订阅将来的通信。 取消订阅后，用户档案将自动从未来营销消息的受众中删除。

While **[!DNL Journey Optimizer]** 提供了管理电子邮件和短信消息中选择退订的方法，推送通知在您这边不需要采取任何操作，因为收件人自己可以通过其设备取消订阅。 例如，下载或使用应用程序时，用户可以选择停止通知。 同样，他们也可以通过移动设备操作系统更改通知设置。

在以下部分中了解如何管理Journey Optimizer电子邮件和短信消息中的选择退出：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="商机" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>电子邮件选择退出管理</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="不频繁" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>短信选择退出管理</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>在 [!DNL Journey Optimizer]，则同意由Experience Platform处理 [同意模式](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}。 默认情况下，同意字段的值为空，并被视为同意接收您的通信。 在载入列出的可能值之一时，您可以修改此默认值 [此处](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}。