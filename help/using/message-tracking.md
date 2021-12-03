---
title: 跟踪邮件
description: 了解如何添加链接和跟踪已发送的消息
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 2879f460d4be4b570e47227b32fa3f979984cbbf
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 2%

---

# 添加链接和跟踪消息 {#tracking}

使用 [!DNL Journey Optimizer] 添加指向内容的链接并跟踪发送的消息，以监控收件人的行为。

## 启用跟踪 {#enable-tracking}

您可以通过检查 **[!UICONTROL Open Tracking for email]** 和/或 **[!UICONTROL Click Tracking for email]** 选项时间 [创建消息](create-message.md).

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
>When [跟踪已启用](#enable-tracking)，则会跟踪消息内容中包含的所有链接。

要在电子邮件内容中插入链接，请执行以下步骤：

1. 选择元素并单击 **[!UICONTROL Insert link]** 中。

   ![](assets/message-tracking-insert-link.png)

1. 选择要创建的链接类型：

   * **[!UICONTROL External link]**:插入指向外部URL的链接。

   * **[!UICONTROL Landing page]**:插入指向登陆页面的链接。 [在本节](landing-pages/get-started-lp.md)中了解详情

   * **[!UICONTROL Unsubscription link]**:插入链接以取消订阅从您的品牌接收通信。 在[此部分中](consent.md#opt-out-management)中了解有关选择退出管理的更多信息。

   * **[!UICONTROL Mirror page]**:插入链接以在Web浏览器中显示电子邮件内容。 在 [此部分](#mirror-page).

   * **[!UICONTROL Opt-out]**:插入链接，使用户能够快速退订您的通信，而无需确认选择退订。 在 [此部分](#one-click-opt-out-link).

   ![](assets/message-tracking-links.png)

1. 您可以个性化您的链接。 在中了解有关个性化URL的更多信息 [此部分](personalization/personalization-syntax.md#perso-urls).

1. 保存更改。

1. 创建链接后，您仍可以从 **[!UICONTROL Component settings]** 窗格。

   * 单击铅笔图标以编辑链接。
   * 您可以通过选中相应的选项来选择是否为链接添加下划线。

   ![](assets/message-tracking-link-settings.png)

## 链接到镜像页面 {#mirror-page}

镜像页面是可通过Web浏览器在线访问的HTML页面。 其内容与电子邮件的内容相同。

要在电子邮件中添加指向镜像页面的链接， [插入链接](#insert-links) 选择 **[!UICONTROL Mirror page]** 作为链接类型。

![](assets/message-tracking-mirror-page.png)

将自动创建镜像页面。

>[!NOTE]
>
>您无法编辑自动生成的链接。

发送电子邮件后，当收件人单击镜像页面链接时，电子邮件的内容会显示在其默认的Web浏览器中。

>[!NOTE]
>
>在 [验证](preview.md#send-proofs) 发送到测试用户档案时，指向镜像页面的链接不处于活动状态。 它仅在最终消息中激活。

镜像页面的保留期为60天。 延迟后，镜像页面将不再可用。

## 一键单击选择退出链接 {#one-click-opt-out-link}

要使收件人快速取消订阅从您的品牌接收通信，您可以在电子邮件内容中插入一键单击的选择退出链接。 此容量可防止用户被重定向到需要确认其选择的登陆页面，从而加快取消订阅过程。

要在电子邮件中添加选择退出链接，请执行以下步骤。

1. [插入链接](#insert-links) 选择 **[!UICONTROL Opt-out]** 作为链接类型。

   ![](assets/message-tracking-opt-out.png)

1. 选择您希望如何应用选择退出：在渠道、身份或订阅级别。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**:选择退出适用于将来发送到当前渠道用户档案目标（即电子邮件地址）的消息。 如果多个目标与某个用户档案关联，则选择退出将应用于该渠道配置文件中的所有目标（即电子邮件地址）。
   * **[!UICONTROL Identity]**:选择退出适用于发送给当前消息所使用的特定目标（即电子邮件地址）的将来消息。
   * **[!UICONTROL Subscription]**:选择退出适用于与特定订阅列表关联的未来消息。 仅当当前消息与订阅列表关联时，才能选择此选项。

1. 输入退订后用户将被重定向的登陆页面的URL。 此页面仅用于确认选择退出是否成功。

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以个性化您的链接。 在中了解有关个性化URL的更多信息 [此部分](personalization/personalization-syntax.md).

1. 保存更改。

发送消息后，如果收件人单击选择退出链接，则他们会立即选择退出。

## 管理跟踪 {#manage-tracking}

的 [Email Designer](create-email-content.md) 用于管理跟踪的URL，例如编辑每个链接的跟踪类型。

1. 单击 **[!UICONTROL Links]** 图标，以显示要跟踪的内容的所有URL的列表。

   利用此列表，可以集中查看并查找电子邮件内容中的每个URL。

1. 要编辑链接，请单击相应的铅笔图标。

   ![](assets/message-tracking-edit-links.png)

1. 您可以修改 **[!UICONTROL Tracking Type]** （如果需要）：


   ![](assets/message-tracking-edit-a-link.png)

   对于每个跟踪的URL，您可以将跟踪模式设置为以下值之一：

   * **[!UICONTROL Tracked]**:在此URL上激活跟踪。
   * **[!UICONTROL Opt out]**:将此URL视为选择退订或退订URL。
   * **[!UICONTROL Mirror page]**:将此URL视为镜像页面URL。
   * **[!UICONTROL Never]**:从不激活此URL的跟踪。 <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

已打开的消息数和已单击的链接数将列在 [“执行”选项卡](message-monitoring.md).

在 [电子邮件实时报表](reports/email-live-report.md) 和 [电子邮件全局报告](reports/email-global-report.md).
