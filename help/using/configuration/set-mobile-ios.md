---
solution: Journey Optimizer
product: journey optimizer
title: 设置iOS mobile
description: 了解如何配置和监控iOS移动渠道
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 通道，表面，技术，参数，优化器
hide: true
hidefromtoc: true
source-git-commit: 4a089308cfc2fa90cc4c0a6baa15a89598e8edd6
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 2%

---

# 设置iOS移动设备配置 {#set-mobile-ios}

>[!IMPORTANT]
>
>为确保兼容性和最佳性能，请确保使用以下SDK版本：
>
> * 核心SDK：5.2.0或更高版本
> * 消息SDK：5.1.1或更高版本

此iOS设置简化了营销渠道的快速配置，使所有基本资源都可以在Experience Platform、Journey Optimizer和数据收集应用程序中随时使用。 这允许您的营销团队快速开始创建活动和历程。

## 创建新的iOS设置 {#new-setup-ios}

1. 在Journey Optimizer主页上，从&#x200B;**[!UICONTROL 设置移动和Web渠道]**&#x200B;信息卡中单击&#x200B;**[!UICONTROL 开始]**。

   ![](assets/guided-setup-config-1.png)

1. 创建&#x200B;**[!UICONTROL 新]**&#x200B;配置。

   如果已有配置，则可以选择选择一个配置，或创建新配置。

   ![](assets/guided-setup-config-2.png)

1. 输入新配置的&#x200B;**[!UICONTROL 名称]**，然后选择或创建您的&#x200B;**[!UICONTROL 数据流]**。 此&#x200B;**[!UICONTROL 名称]**&#x200B;将用于每个自动创建的资源。

1. 如果您的组织有多个数据流，请从现有选项中选择一个。 如果您没有数据流，则将自动为您创建一个数据流。

1. 选择iOS平台并单击&#x200B;**[!UICONTROL 自动创建资源]**。

   ![](assets/guided-setup-config-3.png)

1. 为了简化设置过程，系统会自动创建必要的资源来帮助您入门。 这包括创建新的&#x200B;**[!UICONTROL 移动标记属性]**&#x200B;以及安装扩展。

   以下是自动生成的所有资源的完整列表：

+++ 已创建资源

   <table>
    <thead>
    <tr>
    <th><strong>解决方案</strong></th>
    <th><strong>自动创建的资源</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>
    <p>Journey Optimizer</p>
    </td>
    <td>
    <ul>
    <li>渠道配置</li>
    <li>推送凭据（仅限移动设备推送消息）</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>标记</p>
    </td>
    <td>
    <ul>
    <li>移动标记属性</li>
    <li>规则</li>
    <li>数据元素</li>
    <li>库</li>
    <li>环境（暂存、生产、开发）</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>标记扩展</p>
    </td>
    <td>
    <ul>
    <li>Adobe Experience PlatformEdge Network</li>
    <li>Adobe Journey Optimizer</li>
    <li>AEP保证</li>
    <li>同意（已启用默认同意策略）</li>
    <li>标识（使用默认ECID，使用默认拼接规则）</li>
    <li>移动核心</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Assurance</p>
    </td>
    <td>
    <p>保证会话</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>数据流</p>
    </td>
    <td>
    <p>使用服务的数据流</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Experience Platform</p>
    </td>
    <td>
    <ul>
    <li>数据集</li>
    <li>架构</li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

+++

1. 资源生成完成后，单击&#x200B;**[!UICONTROL 设置]**&#x200B;以开始配置SDK。

   ![](assets/guided-setup-config-ios-1.png)

1. 首先需要按照用户界面中的说明添加和导入依赖项。 [了解详情](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks)。

1. 将初始化代码插入应用程序的`onCreate()`方法中。 此测试代码允许您在移至生产环境之前连接到Assurance并验证您的应用程序设置。

   ![](assets/guided-setup-config-ios-2.png){zoomable="yes"}

1. 要直接在移动应用程序上验证您的SDK，只需打开您的移动应用程序并允许访问[Adobe保证](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home)即可。 “保证”是一款功能强大的工具，可让您彻底测试和验证实施，确保一切正常运行。

   连接后，您的设备将被自动检测并列在&#x200B;**[!UICONTROL 可用设备]**&#x200B;下拉菜单中，从而允许您实时无缝地监视和排除设置故障。

   ![](assets/guided-setup-config-ios-3.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 连接]**。

   ![](assets/guided-setup-config-ios-4.png){zoomable="yes"}

1. 您现在可以配置[应用程序内](#inapp-channel)和/或[推送](#push-channel)渠道。

1. 完成配置后，与负责创建历程和营销活动的团队成员共享自动生成的&#x200B;**[!UICONTROL 渠道配置]**。

   **[!UICONTROL 渠道配置]**&#x200B;应在“营销活动”或“历程”界面中引用，以便在您的设置与针对受众执行目标历程和营销活动之间实现无缝连接。

   ![](assets/guided-setup-config-ios-8.png){zoomable="yes"}

## 修改现有配置 {#reconnect}

创建配置后，您可以随时轻松重新访问它以添加其他渠道或进一步调整以符合您的需求

1. 在Journey Optimizer主页上，从&#x200B;**[!UICONTROL 设置移动和Web渠道]**&#x200B;信息卡中单击&#x200B;**[!UICONTROL 开始]**。

   ![](assets/guided-setup-config-1.png)

1. 选择&#x200B;**[!UICONTROL Existing]**，然后从下拉列表中选择现有的&#x200B;**[!UICONTROL Tag属性]**。

   ![](assets/guided-setup-config-ios-9.png)

1. 访问现有配置时，您需要重新连接Adobe保证。 从SDK设置菜单中，单击&#x200B;**[!UICONTROL 重新连接]**。

   ![](assets/guided-setup-config-ios-10.png)

1. 从&#x200B;**[!UICONTROL 可用设备]**&#x200B;下拉列表中选择您的设备，然后单击&#x200B;**[!UICONTROL 连接]**。

   ![](assets/guided-setup-config-ios-11.png){zoomable="yes"}

1. 您现在可以根据需要更新配置。

## 设置应用程序内渠道 {#inapp-channel}

应用程序内渠道无需其他设置。 要验证您的配置是否正确，可以使用“保证”功能轻松发送测试消息。 这将即时反馈系统是否准备好有效投放应用程序内消息。

要执行此操作，只需单击&#x200B;**[!UICONTROL 显示应用程序内消息]**。

![](assets/guided-setup-config-ios-5.png){zoomable="yes"}

为了简化设置过程，系统会自动创建必要的资源来帮助您入门。 这包括创建渠道配置。

您现在可以使用之前配置的&#x200B;**[!UICONTROL 渠道配置]**&#x200B;发送应用程序内消息。 [了解如何创建应用程序内消息](../in-app/create-in-app.md)

## 设置推送渠道 {#push-channel}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_certificate"
>title="提供推送证书"
>abstract=".p8密钥文件包含一个私钥，用于向Apple服务器验证您的应用程序以获得安全推送通知。 您可以从开发人员帐户的Certificates、Identifiers和Profiles页面获取此密钥。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_key_id"
>title="密钥 ID"
>abstract="密钥ID是在创建p8身份验证密钥期间分配的10个字符的字符串，可在开发人员帐户的“证书、标识符和配置文件”页面上的&#x200B;**密钥**&#x200B;选项卡下找到。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_team_id"
>title="团队 ID"
>abstract="团队ID是用于识别团队的字符串值，它位于开发人员帐户的&#x200B;**成员资格**&#x200B;选项卡下。"

1. 配置移动SDK后，单击推送通知卡中的&#x200B;**[!UICONTROL 添加]**。

1. 首先，在`AppDelegate`的`didRegisterForRemoteNotificationsWithDeviceToken`方法中，添加以下代码以将设备的推送令牌与Adobe Experience Platform配置文件同步。

   ```
   MobileCore.setPushIdentifier(deviceToken)
   ```

1. 拖放您的.p8 Apple推送通知身份验证密钥文件。 此密钥可以从“证书、标识符和配置文件”页面获取。

1. 提供以下信息：

   * 密钥ID：在创建p8身份验证密钥期间分配的10个字符串。 可在“证书、标识符和配置文件”页面的“密钥”选项卡下找到它。

   * 团队ID：可在“成员资格”选项卡下找到的字符串值。

   ![](assets/guided-setup-config-ios-6.png){zoomable="yes"}

1. 要验证您的配置是否正确，可以使用“保证”功能轻松发送测试消息。 这将立即提供有关系统准备情况的反馈，以便有效地发送推送通知。

   要执行此操作，只需单击&#x200B;**[!UICONTROL 发送推送消息]**。

   ![](assets/guided-setup-config-ios-7.png){zoomable="yes"}

为了简化设置过程，系统会自动创建必要的资源来帮助您入门。 这包括创建&#x200B;**[!UICONTROL 渠道配置]**&#x200B;和&#x200B;**[!UICONTROL 推送凭据]**。

您现在可以使用之前配置的&#x200B;**[!UICONTROL 渠道配置]**&#x200B;发送推送通知。 [了解如何创建推送通知](../push/create-push.md)
