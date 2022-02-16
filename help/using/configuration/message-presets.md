---
title: 创建消息预设
description: 了解如何配置和监视消息预设
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 4a0b1ee220cc05e4dfc10724554b39bdfd0b6678
workflow-type: tm+mt
source-wordcount: '1694'
ht-degree: 2%

---

# 创建消息预设 {#message-presets-creation}

使用 [!DNL Journey Optimizer]，则可以设置消息预设，以定义电子邮件和推送通知消息所需的所有技术参数：电子邮件类型、发件人电子邮件和名称、移动设备应用程序等。

>[!CAUTION]
>
> * 消息预设配置仅限历程管理员。 [了解详情](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 您必须执行电子邮件配置和 [推送配置](../messages/push-configuration.md) 创建消息预设之前的步骤。


配置消息预设后，您便能够在从 **[!UICONTROL Presets]** 列表。

➡️ [在此视频中了解如何创建和使用电子邮件预设](#video-presets)

## 创建消息预设 {#create-message-preset}

要创建消息预设，请执行以下步骤：

1. 访问 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 菜单，然后单击 **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. 为预设输入名称和描述（可选），然后选择要配置的渠道。

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

1. 配置 **电子邮件** 设置。 [了解详情](#configure-email-settings)

1. 配置 **推送通知** 设置。 [了解详情](#configure-push-settings)

   <!--Configure SMS settings. [Learn more](#configure-sms-settings) -->

1. 配置所有参数后，单击 **[!UICONTROL Submit]** 确认。 您还可以将消息预设另存为草稿，稍后恢复其配置。

   ![](../assets/preset-submit.png)

1. 创建消息预设后，该消息预设会显示在列表中，其中 **[!UICONTROL Processing]** 状态。

   在此步骤中，将执行多项检查，以验证是否已正确配置。 处理时间在附近 **48h-72h**，并且 **7-10个工作日**.

   这些检查包括由Adobe团队执行的配置和技术测试：

   * SPF验证
   * DKIM验证
   * MX记录验证
   * 检查IP列入阻止列表
   * 主机检查
   * IP池验证
   * A/PTR记录， t/m/res子域验证

   >[!NOTE]
   >
   >如果检查失败，请在 [此部分](#monitor-message-presets).

1. 检查成功后，消息预设将获取 **[!UICONTROL Active]** 状态。 它已准备好用于投放消息。

   ![](../assets/preset-active.png)

## 配置电子邮件设置 {#configure-email-settings}

![](../assets/preset-email.png)

1. 选择将随预设一起发送的消息类型： **事务型** 或 **营销**.

   >[!CAUTION]
   >
   > **事务型** 消息可发送给从营销通信中取消订阅的用户档案。 这些消息只能在特定环境中发送，例如密码重置、顺序状态、投放通知。

1. 选择要用于发送电子邮件的子域。 [了解详情](about-subdomain-delegation.md)

1. 选择要与预设关联的IP池。 [了解详情](ip-pools.md)

1. 输入使用该预设发送的电子邮件的标题参数。

   >[!CAUTION]
   >
   >电子邮件地址必须使用当前选定的 [委派子域](about-subdomain-delegation.md).

   * **[!UICONTROL Sender name]**:发件人的名称，如您的品牌名称。

   * **[!UICONTROL Sender email]**:要用于通信的电子邮件地址。 例如，如果委派的子域为 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com*.

   * **[!UICONTROL Reply to (name)]**:收件人单击 **回复** 按钮。

   * **[!UICONTROL Reply to (email)]**:收件人单击 **回复** 按钮。 您必须使用在委派子域上定义的地址(例如， *reply@marketing.luma.com*)，否则将删除电子邮件。

   * **[!UICONTROL Error email]**:收到ISP在收到几天邮件后（异步退回）生成的所有错误，均位于此地址。
   >[!NOTE]
   >
   >从2021年10月版开始，无法再从 [!DNL Journey Optimizer] 用户界面。 如果您希望收到 [!DNL Journey Optimizer] 要将委派的子域转发到特定的电子邮件地址，请联系 [Adobe客户关怀支持团队](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

   ![](../assets/preset-header.png)

   >[!NOTE]
   >
   >名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

1. 配置 **电子邮件重试参数**. 默认情况下， [重试时段](retries.md#retry-duration) 设置为84小时，但您可以根据自己的需求调整此设置。

   ![](../assets/preset-retry-paramaters.png)

   您必须在以下范围内输入整数值（以小时或分钟为单位）：
   * 对于营销电子邮件类型，最短重试时间为6小时。
   * 对于事务型电子邮件类型，最小重试周期为10分钟。
   * 对于这两种电子邮件类型，最大重试时间段为84小时（或5040分钟）。

## 配置推送设置 {#configure-push-settings}

1. 至少选择一个平台： **iOS** 和/或 **Android**.

1. 选择要用于每个平台的移动设备应用程序。

![](../assets/preset-push.png)

有关如何配置环境以发送推送通知的更多信息，请参阅 [此部分](../messages/push-gs.md).

<!--
## Configure SMS settings {#configure-sms-settings}

1. Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**.

    ![](../assets/preset-sms.png)
    
1. Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
    For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

## 监视消息预设 {#monitor-message-presets}

所有消息预设都显示在 **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** 菜单。 过滤器可帮助您浏览列表（渠道类型、用户、状态）。

![](../assets/preset-filters.png)

消息预设可以具有以下状态：

* **[!UICONTROL Draft]**:消息预设已另存为草稿，但尚未提交。 打开它以恢复配置。
* **[!UICONTROL Processing]**:消息预设已提交，正在执行多个验证步骤。
* **[!UICONTROL Active]**:消息预设已验证，可选择该预设以创建消息。
* **[!UICONTROL Failed]**:在消息预设验证期间，一个或多个检查失败。
* **[!UICONTROL Deactivated]**:消息预设已停用。 它不能用于创建新消息。

如果消息预设创建失败，则下面将介绍每种可能失败原因的详细信息。

如果出现其中一个错误，请与 [Adobe客户关怀支持团队](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以获取帮助。

* **SPF验证失败**:SPF（发件人策略框架）是一种电子邮件身份验证协议，它允许指定能够从给定子域发送电子邮件的授权IP。 SPF验证失败意味着SPF记录中的IP地址与用于向邮箱提供程序发送电子邮件的IP地址不匹配。

* **DKIM验证失败**:DKIM（域名识别邮件）允许收件人服务器验证收到的消息是否由相关域的正版发件人发送，且原始消息的内容在发送过程中没有发生更改。 DKIM验证失败意味着接收邮件服务器无法验证邮件内容的真实性及其与发送域的关联。

* **MX记录验证失败**:MX（邮件交换）记录验证失败意味着负责代表给定子域接受入站电子邮件的邮件服务器未正确配置。

* **投放能力配置失败**:可投放性配置失败，原因如下：
   * 列入阻止列表已分配IP的管理
   * 无效 `helo` name
   * 从IP（而非相应预设的IP池中指定的IP）发送的电子邮件
   * 无法向Gmail和Yahoo等主要ISP的收件箱发送电子邮件

## 编辑消息预设 {#edit-message-preset}

要编辑消息预设，请执行以下步骤。

>[!NOTE]
>
>您无法编辑 **[!UICONTROL Push notification settings]**. 如果消息预设仅为推送通知渠道配置，则它不可编辑。

1. 在列表中，单击消息预设名称以将其打开。

   ![](../assets/preset-name.png)

1. 根据需要编辑其属性。

   >[!NOTE]
   >
   >如果消息预设具有 **[!UICONTROL Active]** 状态， **[!UICONTROL Name]**, **[!UICONTROL Select channel]** 和 **[!UICONTROL Subdomain]** 字段灰显，无法编辑。

1. 单击 **[!UICONTROL Submit]** 确认更改。

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >您还可以将消息预设另存为草稿，稍后继续更新。

提交更改后，消息预设将经过与原位置类似的验证周期(在 [创建预设](#create-message-preset).

>[!NOTE]
>
>如果您仅编辑 **[!UICONTROL Description]**, **[!UICONTROL Email type]** 和/或 **[!UICONTROL Email retry parameters]** 字段中，更新是即时的。

对于具有 **[!UICONTROL Active]** 状态，则可以检查更新的详细信息。 为实现此操作，请执行以下步骤：

* 单击 **[!UICONTROL Recent update]** 图标。

   ![](../assets/preset-recent-update-icon.png)

* 您还可以在更新进行时从活动消息预设访问更新详细信息。

   ![](../assets/preset-view-update-details.png)

在 **[!UICONTROL Recent update]** 屏幕中，您可以查看更新状态和请求更改的列表等信息。

![](../assets/preset-recent-update-screen.png)

### 更新状态 {#update-statuses}

消息预设更新可以具有以下状态：

* **[!UICONTROL Processing]**:消息预设更新已提交，正在执行多个验证步骤。
* **[!UICONTROL Success]**:已验证更新的消息预设，并可以选择该预设以创建消息。
* **[!UICONTROL Failed]**:在消息预设更新验证期间，一个或多个检查失败。

下面详细介绍了每种状态。

### 处理时间

将执行多项投放能力检查，以验证预设是否已正确更新。

>[!NOTE]
>
>如果您仅编辑 **[!UICONTROL Description]**, **[!UICONTROL Email type]** 和/或 **[!UICONTROL Email retry parameters]** 字段中，更新是即时的。

处理时间在附近 **48h-72h**，并且 **7-10个工作日**. 了解有关在 [此部分](#create-message-preset).

如果您编辑的预设已处于活动状态，请执行以下操作：

* 其地位仍然 **[!UICONTROL Active]** 验证过程进行中。

* 的 **[!UICONTROL Recent update]** 图标。

* 在验证过程中，使用此预设配置的消息仍使用旧版本的预设。

>[!NOTE]
>
>在更新过程中，您无法修改消息预设。 您仍可以单击其名称，但所有字段都呈灰显状态。 更新成功后，才会反映更改。

### 成功 {#success}

验证过程成功后，使用此预设的所有消息中都会自动使用新版本的预设。 但是，您可能必须等待：
* 在被单一报文使用前几分钟，
* 直到预设的下一批次在批处理消息中生效。

### 失败 {#failed}

如果验证过程失败，则仍会使用旧版本的预设。

详细了解 [此部分](#monitor-message-presets).

更新失败后，预设将再次变为可编辑状态。 您可以单击其名称并更新需要修复的设置。

## 停用消息预设 {#deactivate-preset}

要 **[!UICONTROL Active]** 消息预设无法创建新消息，您可以将其停用。 但是，使用此预设发布的消息将不会受到影响，并将继续工作。

>[!NOTE]
>
>无法在处理更新时停用消息预设。 您必须等到更新成功或失败。 了解详情 [编辑消息预设](#edit-message-preset) 和 [更新状态](#update-statuses).

1. 访问消息预设列表。

1. 对于所选的活动预设，单击 **[!UICONTROL More actions]** 按钮。

1. 选择 **[!UICONTROL Deactivate]**。

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>无法删除已停用的消息预设，以避免在使用这些预设发送消息的历程中出现任何问题。

您无法直接编辑已停用的消息预设。 但是，您可以复制并编辑副本以创建新版本，以用于创建新消息。 您还可以再次激活它，然后等到更新成功后才对其进行编辑。

![](../assets/preset-activate.png)

## 操作方法视频{#video-presets}

了解如何创建消息预设、如何使用这些预设以及如何委派子域和创建IP池。

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
