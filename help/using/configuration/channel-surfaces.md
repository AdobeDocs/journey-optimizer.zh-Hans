---
title: 设置渠道平面
description: 了解如何配置和监视通道表面
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# 设置渠道平面 {#set-up-channel-surfaces}

使用 [!DNL Journey Optimizer]，您可以设置渠道曲面（即消息预设），以定义消息所需的所有技术参数：电子邮件类型、发件人电子邮件和名称、移动应用程序、短信配置等。

>[!CAUTION]
>
> * 要创建、编辑和删除通道曲面，您必须具有 [管理渠道表面](../administration/high-low-permissions.md#manage-channel-surface) 权限。
>
> * 您必须执行 [电子邮件配置](#configure-email-settings), [推送配置](../configuration/push-configuration.md) 和 [短信配置](../configuration/sms-configuration.md) 创建通道曲面之前的步骤。


配置渠道表面后，您将能够在从历程创建消息时选择渠道表面。

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## 创建通道曲面 {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="通道表面设置"
>abstract="在设置渠道表面时，选择渠道并定义其应用到的渠道，以及定义消息所需的所有技术参数，例如电子邮件类型、子域、发件人名称、移动应用程序、短信配置等。"

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="通道表面设置"
>abstract="在设置渠道表面时，选择渠道并定义消息所需的所有技术参数，例如电子邮件类型、发件人名称、移动应用程序、短信配置等。"

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

在 **[!UICONTROL 最近更新]** 屏幕中，您可以查看更新状态和请求更改的列表等信息。

<!--![](assets/preset-recent-update-screen.png)-->

### 更新状态 {#update-statuses}

渠道曲面更新可以具有以下状态：

* **[!UICONTROL 处理]**:已提交通道表面更新，并正在执行多个验证步骤。
* **[!UICONTROL 成功]**:已验证更新的通道表面，并可选择该表面以创建消息。
* **[!UICONTROL 失败]**:在通道表面更新验证期间，一个或多个检查失败。

下面详细介绍了每种状态。

#### 处理时间 {#surface-processing}

将执行多项投放能力检查，以验证表面是否已正确更新。

>[!NOTE]
>
>如果您仅编辑 **[!UICONTROL 描述]**, **[!UICONTROL 电子邮件类型]** 和/或 **[!UICONTROL 电子邮件重试参数]** 字段中，更新是即时的。

处理时间可能需要 **3小时**. 了解有关在 [此部分](#create-channel-surface).

如果编辑已处于活动状态的曲面：

* 其地位仍然 **[!UICONTROL 活动]** 验证过程进行中。

* 的 **[!UICONTROL 最近更新]** 图标在“通道曲面”(channel surfaces)列表中曲面的名称旁边显示。

* 在验证过程中，使用此曲面配置的消息仍使用该曲面的旧版本。

>[!NOTE]
>
>在进行更新时，无法修改通道曲面。 您仍可以单击其名称，但所有字段都呈灰显状态。 更新成功后，才会反映更改。

#### 成功 {#success}

验证过程成功后，新版曲面将自动用于使用该曲面的所有消息。 但是，您可能必须等待：
* 在被单一报文使用前几分钟，
* 直到下一批表面在批处理消息中生效。

#### 失败 {#failed}

如果验证过程失败，仍将使用较旧版本的曲面。

详细了解 [此部分](#monitor-channel-surfaces).

更新失败后，曲面将再次变得可编辑。 您可以单击其名称并更新需要修复的设置。

## 停用通道曲面 {#deactivate-a-surface}

要 **[!UICONTROL 活动]** 渠道表面无法创建新消息，您可以将其停用。 但是，当前使用此表面的历程消息将不会受到影响，并将继续工作。

>[!NOTE]
>
>在处理更新时，不能停用通道曲面。 您必须等到更新成功或失败。 了解详情 [编辑通道曲面](#edit-channel-surface) 和 [更新状态](#update-statuses).

1. 访问通道曲面列表。

1. 对于所选的活动曲面，单击 **[!UICONTROL 更多操作]** 按钮。

1. 选择 **[!UICONTROL 停用]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>无法删除已停用的渠道表面，以避免在使用这些表面发送消息的历程中出现任何问题。

不能直接编辑已停用的通道曲面。 但是，您可以复制并编辑副本以创建新版本，以用于创建新消息。 您还可以再次激活它，然后等到更新成功后才对其进行编辑。

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
