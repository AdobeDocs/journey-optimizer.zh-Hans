---
title: 创建消息预设
description: 了解如何配置和监视消息预设
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: f52f73b1d7f2ad5a7ebd2e8b23b7c68c4dc99212
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---


# 创建消息预设

借助[!DNL Journey Optimizer]，您可以设置消息预设，以定义电子邮件和推送通知消息所需的所有技术参数：电子邮件类型、发件人电子邮件和名称、移动设备应用程序等。

>[!CAUTION]
>
> * 消息预设配置仅限历程管理员。 [了解详情](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 在创建消息预设之前，必须执行电子邮件和推送配置步骤。


配置消息预设后，在从&#x200B;**[!UICONTROL Presets]**&#x200B;列表创建消息时，可以选择这些预设。

➡️ [在此视频中了解如何创建和使用电子邮件预设](#video-presets)

## 创建消息预设 {#create-message-preset}

要创建消息预设，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Message presets]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL Create Message preset]**。

   ![](../assets/preset-create.png)

1. 为预设输入名称和描述（可选），然后选择要配置的渠道。

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`。

1. 配置&#x200B;**email**&#x200B;设置。

   ![](../assets/preset-email.png)

   * 选择将随预设一起发送的消息类型：**Transactional**&#x200B;或&#x200B;**Marketing**

      >[!CAUTION]
      >
      > **** 可向从营销通信中取消订阅的用户档案发送交易消息。这些消息只能在特定环境中发送，例如密码重置、顺序状态、投放通知。

   * 选择要用于发送电子邮件的子域。 [了解详情](about-subdomain-delegation.md)
   * 选择要与预设关联的IP池。 [了解详情](ip-pools.md)
   * 输入使用该预设发送的电子邮件的标题参数。

      >[!CAUTION]
      >
      >除&#x200B;**回复（转发电子邮件）**&#x200B;字段外，电子邮件地址域必须使用当前选定的[委派的子域](about-subdomain-delegation.md)。

      * **[!UICONTROL Sender name]**:发件人的名称，如您的品牌名称。

      * **[!UICONTROL Sender email]**:要用于通信的电子邮件地址。例如，如果委派的子域是&#x200B;*marketing.luma.com*，则可以使用&#x200B;*contact@marketing.luma.com*。

      * **[!UICONTROL Reply to (name)]**:收件人在其电子邮件客户端软件中单击“重 **** 复按钮”时将使用的名称。

      * **[!UICONTROL Reply to (email)]**:收件人在其电子邮件客户端软件中单击“重 **** 复”按钮时将使用的电子邮件地址。发送到此地址的电子邮件将转发到下面提供的&#x200B;**[!UICONTROL Reply to (forward email)]**&#x200B;地址。 您必须使用在委派的子域(例如&#x200B;*reply@marketing.luma.com*)上定义的地址，否则将删除电子邮件。

      * **[!UICONTROL Reply to (forward email)]**:接收的有关委派 [!DNL Journey Optimizer] 子域的所有电子邮件都将转发到此电子邮件地址。除了在委派的子域上定义的电子邮件地址之外，您可以指定任何地址。 例如，如果委派的子域为&#x200B;*marketing.luma.com*，则禁止使用任何地址，如&#x200B;*abc@marketing.luma.com*。

      * **[!UICONTROL Error email]**:收到ISP在收到几天邮件后（异步退回）生成的所有错误，均位于此地址。

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`。

   * 配置&#x200B;**电子邮件重试参数**。 默认情况下，[重试时间段](retries.md#retry-duration)设置为84小时，但您可以调整此设置以更好地满足您的需求。

      ![](../assets/preset-retry-paramaters.png)

      您必须在以下范围内输入整数值（以小时或分钟为单位）：
      * 对于营销电子邮件类型，最短重试时间为6小时。
      * 对于事务型电子邮件类型，最小重试周期为10分钟。
      * 对于这两种电子邮件类型，最大重试时间段为84小时（或5040分钟）。


1. 配置&#x200B;**推送通知**&#x200B;设置。

   ![](../assets/preset-push.png)

   * 至少选择一个平台：**iOS**&#x200B;和/或&#x200B;**Android**

   * 选择要用于每个平台的移动设备应用程序。

      有关如何配置环境以发送推送通知的更多信息，请参阅[此部分](../push-gs.md)。

1. 配置完所有参数后，单击&#x200B;**[!UICONTROL Submit]**&#x200B;进行确认。 您还可以将消息预设另存为草稿，稍后恢复其配置。

   ![](../assets/preset-submit.png)

1. 创建消息预设后，该消息预设将显示在列表中，并且状态为&#x200B;**[!UICONTROL Processing]**。

   在此步骤中，将执行多项检查，以验证是否已正确配置。 处理时间在&#x200B;**48h-72h**&#x200B;左右，最长可达&#x200B;**7-10天**。

   这些检查包括由Adobe投放能力团队执行的投放能力测试：

   * SPF验证
   * DKIM验证
   * MX记录验证
   * 检查IP列入阻止列表
   * 主机检查
   * IP池验证
   * A/PTR记录， t/m/res子域验证

   >[!NOTE]
   >
   >如果检查失败，请在[此部分](#monitor-message-presets)中了解有关可能失败原因的更多信息。

1. 检查成功后，消息预设将获得&#x200B;**[!UICONTROL Active]**&#x200B;状态。 它已准备好用于投放消息。

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 监视消息预设 {#monitor-message-presets}

所有消息预设都显示在&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Message presets]**&#x200B;菜单中。 过滤器可帮助您浏览列表（渠道类型、用户、状态）。

![](../assets/preset-filters.png)

消息预设可以具有以下状态：

* **[!UICONTROL Draft]**:消息预设已另存为草稿，但尚未提交。打开它以恢复配置。
* **[!UICONTROL Processing]**:消息预设已提交，正在执行多个验证步骤。
* **[!UICONTROL Active]**:消息预设已验证，可选择该预设以创建消息。
* **[!UICONTROL Failed]**:在消息预设验证期间，一个或多个检查失败。
* **[!UICONTROL De-activated]**:消息预设已取消激活。它不能用于创建新消息。

如果消息预设创建失败，则下面将介绍每种可能失败原因的详细信息。

如果出现其中一个错误，请联系[Adobe客户关怀支持团队](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以获取帮助。

* **SPF验证失败**:SPF（发件人策略框架）是一种电子邮件身份验证协议，它允许指定能够从给定子域发送电子邮件的授权IP。SPF验证失败意味着SPF记录中的IP地址与用于向邮箱提供程序发送电子邮件的IP地址不匹配。

* **DKIM验证失败**:DKIM允许收件人服务器验证所收到的消息是否由关联域的正版发送者发送，以及原始消息的内容是否未在发送过程中发生更改。DKIM验证失败意味着接收邮件服务器无法验证邮件内容的真实性及其与发送域的关联。

* **MX记录验证失败**:MX记录验证失败意味着负责代表给定子域接受入站电子邮件的邮件服务器配置不正确。

* **投放能力配置失败**:可投放性配置失败，原因如下：
   * 列入阻止列表已分配IP的管理
   * `helo`名称无效
   * 从IP（而非相应预设的IP池中指定的IP）发送的电子邮件
   * 无法向Gmail和Yahoo等主要ISP的收件箱发送电子邮件

## 编辑消息预设

要编辑消息预设，您首先需要取消激活该预设，以使其无法创建新消息（使用此预设发布的消息将不受影响并将继续工作）。 然后，您需要复制消息预设，以创建将用于创建新消息的新版本：

1. 访问消息预设列表，然后取消激活要编辑的消息预设。

   ![](../assets/preset-deactivate.png)

1. 复制已取消激活的消息预设。 状态为&#x200B;**[!UICONTROL Draft]**&#x200B;的副本会自动添加到列表中。

   ![](../assets/preset-duplicated.png)

1. 打开复制的消息预设，根据需要对其进行修改，然后提交更改。 消息预设将完成与创建步骤[](#create-message-preset)期间相同的验证周期。

1. 验证后，系统会获得&#x200B;**[!UICONTROL Active]**&#x200B;状态，并准备好用于创建新消息。

   >[!NOTE]
   >
   >无法删除已取消激活的消息预设，以避免在使用这些预设发送消息的历程中出现任何问题。

## 操作方法视频{#video-presets}

了解如何创建消息预设、如何使用这些预设以及如何委派子域和创建IP池。

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
