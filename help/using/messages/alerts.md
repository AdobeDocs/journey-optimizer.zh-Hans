---
title: 消息中的警报
description: 了解如何检查消息内容验证和疑难解答
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 3%

---

# 检查邮件警报 {#messages-alerts}

## 发送前检查 {#message-alerting}

在设计消息时，如果缺少键设置，则界面中会显示警报。

编辑消息内容时，屏幕的右上方会显示警报。

![](assets/alerts-details.png)

>[!NOTE]
>
>如果看不到此按钮，则未检测到任何警报。

可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 例如，如果缺少选择退出链接，则会显示一条消息。

* **错误** 阻止您测试或激活历程，但前提是这些历程未得到解决。 例如，将显示一条消息，警告您主题行缺失。

详细列出了所有可能的警告和错误 [下面](#alerts-and-warnings).

>[!CAUTION]
>
> 您需要解决所有 **错误** 警报，然后再使用消息测试或激活历程。

## 警告和错误列表 {#alerts-and-warnings}

系统检查的设置和元素如下所示。 您还将找到有关如何调整配置以解决相应问题的信息。

**警告**:

* **[!UICONTROL The opt-out link is not present in the email body]**:最佳做法是向电子邮件正文中添加退订链接。 了解如何在 [此部分](consent.md#opt-out-management).

   >[!NOTE]
   >
   >营销类型电子邮件必须包含选择退出链接，这对于事务型邮件不是必需的。消息类别(**[!UICONTROL Marketing]** 或 **[!UICONTROL Transactional]**) [通道表面](../configuration/message-presets.md#email-type) （即消息预设）级别和时间 [创建消息](get-started-content.md#create-new-message).

* **[!UICONTROL Text version of HTML is empty]**:请不要忘记定义电子邮件正文的文本版本，因为当HTML内容无法显示时，会使用该文本版本。 了解如何在中创建文本版本 [此部分](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body]**:检查电子邮件中的所有链接是否正确。 了解如何在 [此部分](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:为获得最佳投放，请确保电子邮件的大小不超过100KB。 了解如何在 [此部分](../design/create-email-content.md).

**错误**:

* **[!UICONTROL The subject line is missing]**:电子邮件主题行是必填项。 了解如何在中定义和个性化 [此部分](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**:当推送通知正文或标题缺失时，将显示此错误。 了解如何在 [此部分](create-push.md).

* **[!UICONTROL The email version of the message is empty]**:未配置电子邮件内容时，会显示此错误。 了解如何在 [此部分](../design/design-emails.md).

* **[!UICONTROL Surface doesn’t exist]**:如果在消息创建后删除了所选曲面，则无法使用消息。 如果出现此错误，请在消息中选择另一个曲面 **[!UICONTROL Properties]**. 了解有关 [此部分](../configuration/message-presets.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推送通知大小不能超过4KB。 要遵守此限制，请尽量减少使用图像或表情符号。 了解如何在 [此部分](create-push.md).

>[!CAUTION]
>
> 要能够使用您的消息，您需要解析所有 **错误** 警报。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
