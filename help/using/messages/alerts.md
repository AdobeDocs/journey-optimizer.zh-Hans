---
title: 消息中的警报
description: 了解如何检查消息内容验证和疑难解答
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 3c8c059e5e3953807b9fc2d8d0eded0d00e49003
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 检查邮件警报 {#publish-manage-messages}

## 发布前检查 {#message-alerting}

创建消息时，当您需要在发布消息之前采取重要操作时，会发出警告。

警报显示在屏幕的右上方，如下所示：

![](assets/message-alerts.png)

>[!NOTE]
>
>如果看不到此按钮，则未检测到任何警报。

可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 例如，如果缺少选择退出链接，则会显示一条消息。

* **错误** 阻止您发布消息，但前提是这些消息未得到解析。 例如，将显示一条消息，警告您主题行缺失。

详细列出了所有可能的警告和错误 [下面](#alerts-and-warnings).

>[!CAUTION]
>
> 您需要解决所有 **错误** 发布前警报。

## 警告和错误列表 {#alerts-and-warnings}

系统检查的设置和元素如下所示。 您还将找到有关如何调整配置以解决相应问题的信息。

**警告**:

* **[!UICONTROL Opt out link not present in the email body]**:最佳做法是向电子邮件正文中添加退订链接。 了解如何在 [此部分](consent.md).

* **[!UICONTROL Text version of html is empty]**:请不要忘记定义电子邮件正文的文本版本，因为当HTML内容无法显示时，会使用该文本版本。 了解如何在中创建文本版本 [此部分](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body]**:检查电子邮件中的所有链接是否正确。 了解如何在 [此部分](create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:为获得最佳投放，请确保电子邮件的大小不超过100KB。 了解如何在 [此部分](create-email-content.md).

**错误**:

* **[!UICONTROL Subject Line Not Present]**:电子邮件主题行是必填项。 了解如何在中定义和个性化 [此部分](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**:当推送通知正文或标题缺失时，将显示此错误。 了解如何在 [此部分](create-push.md).

* **[!UICONTROL Email Variant is empty]**:未配置电子邮件内容时，会显示此错误。 了解如何在 [此部分](design-emails.md).

* **[!UICONTROL Preset doesn’t exist]**:如果在消息创建后删除了所选的预设，则无法发布消息。 如果发生此错误，请在消息中选择其他预设 **[!UICONTROL Properties]**. 在中了解有关品牌策略的更多信息 [此部分](../configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推送通知大小不能超过4KB。 要遵守此限制，请尽量减少使用图像或表情符号。 了解如何在 [此部分](create-push.md).

>[!CAUTION]
>
> 要发布消息，您需要解析所有 **错误** 警报。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
