---
title: 跟踪邮件
description: 了解如何添加链接和跟踪已发送的消息
feature: 监控
topic: 内容管理
role: User
level: Intermediate
source-git-commit: f5a6a9b6c786b39b492a177de0b19a54b81729f7
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 1%

---

# 添加链接和跟踪消息 {#tracking}

使用[!DNL Journey Optimizer]添加指向内容的链接并跟踪发送的消息，以监控收件人的行为。

## 启用跟踪 {#enable-tracking}

在[创建消息](create-message.md)时，可以通过检查&#x200B;**[!UICONTROL Open Tracking for email]**&#x200B;和/或&#x200B;**[!UICONTROL Click Tracking for email]**&#x200B;选项来启用消息级别的跟踪。

![](assets/message-tracking.png)

>[!NOTE]
>
>默认情况下，这两个选项均处于启用状态。

这样，您就可以通过以下方式跟踪收件人的行为：
* **[!UICONTROL Open Tracking for email]**:已打开的消息。
* **[!UICONTROL Click Tracking for email]**:单击电子邮件中的链接。

## 插入链接 {#insert-links}

在设计消息时，您可以添加指向内容的链接。

>[!NOTE]
>
>启用[跟踪后，将跟踪消息内容中包含的所有链接。](#enable-tracking)

要在电子邮件内容中插入链接，请执行以下步骤：

1. 选择一个元素，然后单击上下文工具栏中的&#x200B;**[!UICONTROL Insert link]**。

   ![](assets/message-tracking-insert-link.png)

1. 选择要创建的链接类型：

   * **[!UICONTROL External link]**:插入指向外部URL的链接。

   * **[!UICONTROL Unsubscription link]**:插入链接以取消订阅从您的品牌接收通信。在[此部分](consent.md#opt-out-management)中了解有关选择退出管理的更多信息。

   * **[!UICONTROL Mirror page]**:插入链接以在Web浏览器中显示电子邮件内容。在[此部分](#mirror-page)中了解详情。

   ![](assets/message-tracking-links.png)

1. 您只能使用简单的表达式对链接进行个性化。 在[此部分](personalization/personalization-syntax.md)中了解有关个性化的更多信息。

1. 保存更改。

1. 创建链接后，您仍可以从右侧的&#x200B;**[!UICONTROL Component settings]**&#x200B;窗格中对其进行修改。

   * 单击铅笔图标以编辑链接。
   * 您可以通过选中相应的选项来选择是否为链接添加下划线。

   ![](assets/message-tracking-link-settings.png)

## 链接到镜像页面 {#mirror-page}

镜像页面是可通过Web浏览器在线访问的HTML页面。 其内容与电子邮件的内容相同。

要在电子邮件中添加指向镜像页面的链接，请[插入链接](#insert-links)并选择&#x200B;**[!UICONTROL Mirror page]**&#x200B;作为链接类型。

![](assets/message-tracking-mirror-page.png)

将自动创建镜像页面。

>[!NOTE]
>
>您无法编辑自动生成的链接。

发送电子邮件后，当收件人单击镜像页面链接时，电子邮件的内容会显示在其默认的Web浏览器中。

>[!NOTE]
>
>在发送到测试用户档案的[proof](preview.md#send-proofs)中，指向镜像页面的链接不活动。 它仅在最终消息中激活。

镜像页面的保留期为60天。 延迟后，镜像页面将不再可用。

## 管理跟踪 {#manage-tracking}

[Email Designer](create-email-content.md)允许您管理跟踪的URL，如编辑每个链接的跟踪类型。

1. 单击左窗格中的&#x200B;**[!UICONTROL Links]**&#x200B;图标，以显示要跟踪的内容的所有URL的列表。

   利用此列表，可以集中查看并查找电子邮件内容中的每个URL。

1. 要编辑链接，请单击相应的铅笔图标。

   ![](assets/message-tracking-edit-links.png)

1. 如果需要，您可以修改&#x200B;**[!UICONTROL Tracking Type]**:


   ![](assets/message-tracking-edit-a-link.png)

   对于每个跟踪的URL，您可以将跟踪模式设置为以下值之一：

   * **[!UICONTROL Tracked]**:在此URL上激活跟踪。
   * **[!UICONTROL Opt out]**:将此URL视为选择退订或退订URL。
   * **[!UICONTROL Mirror page]**:将此URL视为镜像页面URL。
   * **[!UICONTROL Never]**:从不激活此URL的跟踪。  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

[执行选项卡](message-monitoring.md)中列出了已打开的消息数和已单击的链接数。

[电子邮件实时报表](reports/email-live-report.md)和[电子邮件全局报表](reports/email-global-report.md)中提供了有关开场次和点击次数的报告。


